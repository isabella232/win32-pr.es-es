---
title: Configuración de SAP y RPC
description: Los servidores de red de Novell NetWare usan el protocolo de anuncio de servicio (SAP) para difundir información acerca de los servicios disponibles en la red a otros dispositivos en red.
ms.assetid: 6d6ef481-fc09-4795-8954-33329912ff4f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385d60168a52cbe5d31368959ec4f21d52f9ad80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/15/2019
ms.locfileid: "104419230"
---
# <a name="configuring-sap-and-rpc"></a>Configuración de SAP y RPC

Los servidores de red de Novell NetWare usan el protocolo de anuncio de servicio (SAP) para difundir información acerca de los servicios disponibles en la red a otros dispositivos en red. Un servidor puede enviar una difusión de SAP cada 60 segundos para informar a otros dispositivos de red acerca de los servicios que ofrece. Las estaciones de trabajo usan SAP para encontrar los servicios que necesitan en la red.

Windows incluye un servicio del agente SAP para permitir que los servidores basados en Windows interactúen con servidores NetWare. El servicio SAP Agent escuchará las solicitudes de SAP de los clientes de red para los servicios basados en IPX que estén instalados y en ejecución en el servidor.

El software diseñado para anunciarse como servicio a través de la red por medio de una difusión de SAP emitirá los anuncios de SAP cada 60 segundos, sin tener instalado el agente de SAP. Sin embargo, para que los clientes de red puedan localizar rápidamente un servicio de red IPX, un servidor que mantenga una base de datos de servicio debe estar disponible en la red para responder a la solicitud de ubicación de servicio. Esta base de datos de servicio normalmente se mantiene mediante un servidor Novell NetWare o un servidor compatible con NetWare. Los servicios de impresión y archivos de Microsoft para NetWare también mantendrán una base de datos de servicio de red IPX.

En un equipo que ejecuta Windows Server, si están instalados los servicios de puerta de enlace para NetWare (GSNW), se difundirá un tipo de SAP 640 cada 60 segundos mediante el servicio llamada a procedimiento remoto (RPC). Esta difusión de SAP continuará incluso si el usuario deshabilita GSNW y el servicio agente de SAP.

El servicio RPC realizará la difusión de SAP si se instalan los servicios de cliente para NetWare (CSNW) y el servicio agente de SAP. Esta difusión de SAP continuará incluso si el usuario deshabilita el agente de SAP.

De forma predeterminada, el servicio RPC comprobará la presencia de servicios de puerta de enlace para NetWare y el servicio del agente SAP en el equipo en el que se ejecuta Windows Server. La instalación de servicios de archivos e impresión para NetWare instala un agente de SAP.

En el equipo que ejecuta una versión de cliente de Windows con CSNW, el servicio RPC comprueba el servicio agente de SAP. Si los servicios están presentes, RPC iniciará su propio subproceso que realizará el tipo de difusión de SAP 640 cada minuto.

> [!NOTE]
> Si no quiere que las difusiones de SAP en la red cada 60 segundos, puede deshabilitar las difusiones de SAP mediante el editor del registro. Se advierte de que el uso incorrecto del editor del registro puede provocar problemas graves que pueden requerir la reinstalación del sistema operativo. Microsoft no puede garantizar que puedan solucionarse los problemas derivados del uso incorrecto del Editor del Registro. Use el Editor del Registro bajo su propia responsabilidad. Debe realizar una copia de seguridad del registro antes de editarlo.

 

**Para configurar para SAP**

1.  Ejecute el editor del registro (Regedt32.exe) y vaya a la siguiente clave del registro:

    **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC**

2.  En el menú **edición** , haga clic en **Agregar valor** y use la siguiente entrada:
    1.  Nombre del valor: AdvertiseRpcService
    2.  Tipo de datos: REG \_ SZ
    3.  Cadena: no
3.  El uso de no para la cadena desactiva la difusión de SAP de RPC. Si se usa sí para la cadena, se activa la difusión de SAP de RPC.
4.  Reinicie el equipo para que el cambio en el registro surta efecto.
    > [!NOTE]
    > Si las difusiones de SAP continúan después de seguir estos pasos, puede que desee probar un paso de solución de problemas. Elimine el valor de la cadena **Ncacn \_ SPX** en la siguiente clave del registro:
    >
    > **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC \\ ServerProtocols\\**

     

> [!NOTE]  
> Solo se debe usar como paso de solución de problemas. Al eliminar este valor de cadena, se deshabilitan completamente las difusiones de SAP que algunos programas pueden necesitar para funcionar correctamente.