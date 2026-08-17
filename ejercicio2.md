```mermaid
flowchart TD
    subgraph GestionClientes["Paquete: GestionClientes"]
        Cliente["<b>Cliente</b><hr/>+ingresarCliente()<br/>+registrarCliente()<br/>+login()<br/>+cambiarPassword()<br/>+actualizarDatos()"]
    end

    subgraph GestionTickets["Paquete: GestionTickets"]
        Ticket["<b>Ticket</b><hr/>+abrirTicket()<br/>+actualizarTicket()<br/>+consultarTicket()<br/>+borrarTicket()"]
        Auditoria["<b>Auditoria</b><hr/>+registrarAuditoria()"]
    end

    GestionTickets ..->|«use»| GestionClientes
