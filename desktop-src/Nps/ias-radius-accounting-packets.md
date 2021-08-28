---
title: Registro con el servidor de directivas de red
description: Registro con el servidor de directivas de red
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c6446a6ece75a8da8e51ecab3ed4b6ebf256360e8d9032a676922b83b664d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778075"
---
# <a name="logging-with-network-policy-server"></a>Registro con el servidor de directivas de red

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se cambió a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

En la tabla siguiente solo se describen los aspectos más importantes de los paquetes de contabilidad RADIUS. El documento Solicitud de comentarios de cuentas[RADIUS (RFC 2866)](https://www.ietf.org/rfc/rfc2866.txt)proporciona información detallada sobre estos paquetes.

Los paquetes de contabilidad RADIUS se pueden dividir en las siguientes categorías.



| Paquete de contabilidad  | Descripción                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | Enviado por el servidor de acceso a redes (NAS) para indicar que se ha reiniciado.<br/> Contiene nas-identifier/ipaddress.<br/>                                                                                        |
| Accounting-Off     | Enviado por el NAS para indicar que se está apagando.<br/> Contiene nas-identifier/ipaddress.<br/>                                                                                                            |
| Accounting-Start   | Enviado por el NAS, después de que el usuario se haya autenticado y autorizado, para indicar el inicio de una sesión de usuario. <br/> Contiene userid, nas-identifier/ipaddress, además de otra información recibida del NAS.<br/> |
| Accounting-Stop    | Enviado por el NAS para indicar el final de una sesión de usuario.<br/> Contiene userid, nas-identifier/ipaddress, además de otra información recibida del NAS.<br/>                                                      |
| Accounting-Interim | El NAS podría enviar periódicamente por cada usuario que haya iniciado sesión en el NAS. <br/> Esta característica suele ser compatible con las versiones más recientes de NAS.<br/>                                                     |



 

Los siguientes problemas son importantes a tener en cuenta al recopilar información de contabilidad disponible a través de RADIUS:

-   En raras ocasiones, los paquetes podrían perderse durante la transmisión y nunca pueden llegar al servidor RADIUS.
-   El servidor RADIUS no se notifica si el NAS se anula.
-   ISDN admite varias sesiones y cada sesión genera un par de paquetes Accounting-Start/-Stop. Hay un atributo de contabilidad denominado identificador de varias sesiones que identifica claramente estos paquetes de varias sesiones. Compruebe el identificador de varias sesiones además del identificador de sesión para calcular el número de sesiones.

## <a name="requests-logged-by-nps"></a>Solicitudes registradas por NPS

De forma predeterminada, NPS no registra ningún dato. NPS se puede configurar mediante la interfaz de usuario de NPS (nps.msc) para registrar las solicitudes siguientes.



| Paquete registrado          | Descripción                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Solicitud de contabilidad     | Cualquiera de los paquetes de contabilidad descritos en la tabla anterior.<br/>                                                                    |
| Solicitud de autenticación | Enviado por el NAS en nombre del usuario que se conecta.<br/> Las entradas de registro solo contienen atributos entrantes.<br/>                    |
| Aceptación de autenticación  | Nps lo envía para indicar que se debe aceptar la conexión de usuario.<br/> Las entradas de registro solo contienen atributos salientes.<br/> |
| Rechazo de autenticación  | NpS lo envía para indicar que se debe rechazar la conexión de usuario.<br/> Las entradas de registro solo contienen atributos salientes.<br/> |



 

Los datos registrados por NPS pueden ir a un archivo de texto en el servidor NPS o a una base de SQL central. Para obtener más información sobre el registro SQL NPS, [vea SQL Programmability](sql-programmability.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de autenticación de Internet y servidor de directivas de red](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Autenticación, autorización y contabilidad RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Trabajar con un servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

