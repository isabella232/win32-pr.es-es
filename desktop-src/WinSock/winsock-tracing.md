---
description: Seguimiento de Winsock
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803be6220d4d2d440811033786b0f043fab0ff9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715101"
---
# <a name="winsock-tracing"></a>Seguimiento de Winsock

## <a name="introduction"></a>Introducción

El seguimiento de Winsock es una característica de solución de problemas que se puede habilitar en los archivos binarios de venta directa para realizar un seguimiento de determinados eventos de Windows socket con una sobrecarga mínima. El objetivo de agregar el seguimiento comercial a Windows Sockets es permitir una mejor funcionalidad de diagnóstico para desarrolladores y soporte técnico. El seguimiento de eventos de red Winsock admite operaciones de socket de seguimiento para aplicaciones IPv4 e IPv6. El seguimiento de cambios del catálogo Winsock admite los cambios de seguimiento realizados en el catálogo Winsock por proveedores de servicios por capas (LSP). El seguimiento de Winsock es compatible con Windows Vista y versiones posteriores.

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

Cuando se produce un error inesperado en un socket, la pista principal para diagnosticar el problema es el código de error devuelto. Con mucha frecuencia, el código de error devuelto no explica por qué se produjo el error, especialmente cuando el transporte de red subyacente inicia el error. El seguimiento de Winsock proporciona un nivel de seguimiento más detallado que puede registrar información adicional para detectar daños en el búfer y aplicaciones mal escritas.

El seguimiento de Winsock usa el seguimiento de eventos para Windows (ETW), un servicio de seguimiento de alta velocidad y de uso general que proporciona el sistema operativo. Mediante el uso de un mecanismo de almacenamiento en búfer y registro implementado en el kernel, ETW proporciona un mecanismo de seguimiento para los eventos generados por las aplicaciones de modo de usuario y los controladores de dispositivos de modo kernel. Además, ETW ofrece la posibilidad de habilitar y deshabilitar el registro de forma dinámica, lo que facilita la realización de un seguimiento detallado en entornos de producción sin necesidad de reinicios o reinicios de aplicaciones. El mecanismo de registro utiliza búferes que un subproceso de escritura asincrónica escribe en el disco. Esto permite que las aplicaciones de servidor a gran escala escriban eventos con una perturbación mínima. ETW se presentó por primera vez en Windows 2000. Se ha agregado compatibilidad con el seguimiento de Winsock mediante ETW en Windows Vista y versiones posteriores. Para obtener información general sobre ETW, vea [mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

El seguimiento de Winsock solo se puede habilitar en el nivel de sistema operativo para todos los procesos y subprocesos que se ejecutan en un equipo. Actualmente no se puede habilitar el seguimiento de Winsock para un único proceso o subproceso. Cuando se habilita el seguimiento de eventos de red Winsock, se realiza un seguimiento de todas las aplicaciones de socket (IPv4 e IPv6) de un equipo.

En los temas siguientes se describe con más detalle el seguimiento de Winsock:

-   [Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
-   [Control de seguimiento de Winsock](control-of-winsock-tracing.md)
-   [Detalles de seguimiento de eventos de red Winsock](winsock-tracing-event-details.md)
-   [Detalles de seguimiento de cambios de catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Funciones de depuración y seguimiento](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
