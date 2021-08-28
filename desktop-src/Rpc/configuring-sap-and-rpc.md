---
title: Configuración de SAP y RPC
description: Los servidores de red Desconocidos de NetWare usan el Protocolo de publicidad de servicios (SAP) para difundir información sobre los servicios disponibles en la red a otros dispositivos en red.
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cf75a9ab45e97a66f1fc8d796b1d288367bb1c8d0e04b2ace4a90de7e21cbbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931688"
---
# <a name="configuring-sap-and-rpc"></a>Configuración de SAP y RPC

Los servidores de red Desconocidos de NetWare usan el Protocolo de publicidad de servicios (SAP) para difundir información sobre los servicios disponibles en la red a otros dispositivos en red. Un servidor puede enviar una difusión de SAP cada 60 segundos para informar a otros dispositivos de red sobre los servicios que ofrece. Las estaciones de trabajo usan LASP para buscar los servicios que necesitan en la red.

Windows incluye un servicio del Agente SAP para permitir que Windows servidores basados en aplicaciones interactúen con los servidores de NetWare. El servicio del Agente SAP escuchará las solicitudes de SAP de los clientes de red para los servicios basados en IPX que están instalados y ejecutándose en el servidor.

El software diseñado para anunciarse como servicio a través de la red mediante una difusión de SAP emitirá los anuncios de SAP cada 60 segundos, sin tener instalado el agente de SAP. Sin embargo, para que los clientes de red busquen rápidamente un servicio de red IPX, un servidor que mantiene una base de datos de servicio debe estar disponible en la red para responder a la solicitud de ubicación del servicio. Normalmente, esta base de datos de servicio la mantiene Un NetWare de Asíns o un servidor compatible con NetWare. Microsoft File and Print Services para NetWare también mantendrá una base de datos de servicio de red IPX.

En un equipo que ejecuta Windows Server, si está instalado Servicios de puerta de enlace para NetWare (GSNW), un tipo de SAP 640 se difundirá cada 60 segundos mediante el servicio de llamada a procedimiento remoto (RPC). Esta difusión de SAP continuará aunque el usuario deshabilite GSNW y el servicio de agente de SAP.

El servicio RPC realizará la difusión de SAP si están instalados los Servicios de cliente para NetWare (CSNW) y el servicio del Agente SAP. Esta difusión de SAP continuará incluso si el usuario deshabilita el agente de SAP.

De forma predeterminada, el servicio RPC comprobará la presencia de los Servicios de puerta de enlace para NetWare y el servicio del Agente SAP en el equipo que ejecuta Windows Server. Al instalar los servicios de archivo e impresión para NetWare, se instala un agente SAP.

En el equipo que ejecuta una versión de cliente Windows con CSNW, el servicio RPC comprueba el servicio del Agente SAP. Si los servicios están presentes, RPC iniciará su propio subproceso que realizará el tipo de difusión de SAP 640 cada minuto.

> [!NOTE]
> Si no desea difusión de SAP en la red cada 60 segundos, puede deshabilitar las difusión de SAP mediante el Editor del Registro. Tenga en cuenta que el uso incorrecto del Editor del Registro puede causar problemas graves que pueden requerir que vuelva a instalar el sistema operativo. Microsoft no puede garantizar que puedan solucionarse los problemas derivados del uso incorrecto del Editor del Registro. Use el Editor del Registro bajo su propia responsabilidad. Debe hacer una copia de seguridad del registro antes de editarlo.

 

**Para configurar para SAP**

1.  Ejecute el Editor del Registro (Regedt32.exe) y vaya a la clave siguiente en el Registro:

    **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ RPC**

2.  En el **menú Editar,** haga clic **en Agregar valor** y use la siguiente entrada:
    1.  Nombre del valor: AdvertiseRpcService
    2.  Tipo de datos: REG \_ SZ
    3.  Cadena: No
3.  El uso de No para la cadena desactiva la difusión de RPC de SAP. El uso de Sí para la cadena activa la difusión de RPC de SAP.
4.  Reinicie el equipo para que el cambio del Registro suba efecto.
    > [!NOTE]
    > Si las difusión de SAP continúan después de seguir estos pasos, puede que desee probar un paso de solución de problemas. Elimine el **valor de cadena del \_ spx Ncacn** en la siguiente clave del Registro:
    >
    > **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc \\ ServerProtocols\\**

     

> [!NOTE]  
> Esto solo se debe usar como paso de solución de problemas. Al eliminar este valor de cadena, se deshabilitan completamente las difusión de SAP que algunos programas pueden necesitar para funcionar correctamente.