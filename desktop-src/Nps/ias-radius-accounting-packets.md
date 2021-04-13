---
title: Registro con servidor de directivas de redes
description: Registro con servidor de directivas de redes
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359208"
---
# <a name="logging-with-network-policy-server"></a>Registro con servidor de directivas de redes

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

En la tabla siguiente se describen solo los aspectos más importantes de los paquetes de cuentas RADIUS. El documento de solicitud de comentarios de cuentas de RADIUS ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) proporciona información detallada sobre estos paquetes.

Los paquetes de cuentas RADIUS se pueden dividir en las siguientes categorías.



| Paquete de cuentas  | Descripción                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Accounting-On      | Lo envía el servidor de acceso a la red (NAS) para indicar que se ha reiniciado.<br/> Contiene el identificador de NAS/IPAddress.<br/>                                                                                        |
| Accounting-Off     | Enviado por el NAS para indicar que se está cerrando.<br/> Contiene el identificador de NAS/IPAddress.<br/>                                                                                                            |
| Accounting-Start   | Enviado por el NAS, después de que el usuario se haya autenticado y autorizado, para indicar el inicio de una sesión de usuario. <br/> Contiene userid, NAS-Identifier/IPAddress, además de otra información recibida del NAS.<br/> |
| Accounting-Stop    | Enviado por el NAS para indicar el final de una sesión de usuario.<br/> Contiene userid, NAS-Identifier/IPAddress, además de otra información recibida del NAS.<br/>                                                      |
| Accounting-Interim | Se puede enviar periódicamente por el NAS para cada usuario que ha iniciado sesión en el NAS. <br/> Esta característica se admite generalmente en las versiones más recientes de NAS.<br/>                                                     |



 

Es importante tener en cuenta los siguientes problemas a la hora de recopilar información de cuentas disponible a través de RADIUS:

-   En raras ocasiones, es posible que los paquetes se pierdan durante la transmisión y que nunca lleguen al servidor RADIUS.
-   No se notifica al servidor RADIUS si el NAS se anula.
-   ISDN admite varias sesiones y cada sesión genera un par de paquetes de inicio y detención de cuentas. Hay un atributo de contabilidad denominado identificador de varias sesiones que identifica claramente estos paquetes de varias sesiones. Busque el identificador de varias sesiones además del identificador de sesión para calcular el número de sesiones.

## <a name="requests-logged-by-nps"></a>Solicitudes registradas por NPS

De forma predeterminada, NPS no registra ningún dato. NPS se puede configurar mediante la interfaz de usuario de NPS (NPS. msc) para registrar las siguientes solicitudes.



| Paquete registrado          | Descripción                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Solicitud de cuentas     | Cualquiera de los paquetes de cuentas descritos en la tabla anterior.<br/>                                                                    |
| Solicitud de autenticación | Enviado por el NAS en nombre del usuario que se conecta.<br/> Las entradas del registro solo contienen atributos entrantes.<br/>                    |
| Aceptación de autenticación  | Lo envía NPS para indicar que se debe aceptar la conexión de usuario.<br/> Las entradas del registro solo contienen atributos de salida.<br/> |
| Rechazo de autenticación  | Lo envía NPS para indicar que se debe rechazar la conexión de usuario.<br/> Las entradas del registro solo contienen atributos de salida.<br/> |



 

Los datos registrados por NPS pueden ir a un archivo de texto en el servidor NPS o a una base de datos SQL central. Para obtener más información sobre el registro de SQL de NPS, consulte [programación de SQL](sql-programmability.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de autenticación de Internet y servidor de directivas de redes](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[Autenticación, autorización y cuentas RADIUS](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Trabajar con un servidor de estado](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

