---
description: Seguimiento de Winsock
ms.assetid: 0c430fc2-28e7-4537-a887-4c36d24fedee
title: Seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803be6220d4d2d440811033786b0f043fab0ff9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967211"
---
# <a name="winsock-tracing"></a>Seguimiento de Winsock

## <a name="introduction"></a>Introducción

El seguimiento de Winsock es una característica de solución de problemas que se puede habilitar en los archivos binarios comerciales para realizar un seguimiento de determinados eventos Windows socket con una sobrecarga mínima. El objetivo de agregar el seguimiento de minoristas a Windows Sockets es permitir mejores funcionalidades de diagnóstico para los desarrolladores y el soporte técnico del producto. El seguimiento de eventos de red de Winsock admite operaciones de socket de seguimiento para aplicaciones IPv4 e IPv6. El seguimiento de cambios del catálogo de Winsock admite el seguimiento de los cambios realizados en el catálogo de Winsock por proveedores de servicios por capas (LSP). El seguimiento de Winsock se admite en Windows Vista y versiones posteriores.

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows de filtrado.](../fwp/windows-filtering-platform-start-page.md)

 

Cuando se produce un error inesperado en un socket, la pista principal para diagnosticar el problema es el código de error devuelto. A menudo, el código de error devuelto no explica por qué se produjo el error, especialmente cuando el error lo inicia el transporte de red subyacente. El seguimiento de Winsock proporciona un nivel de seguimiento más detallado que puede registrar información adicional para detectar daños en el búfer y aplicaciones mal escritas.

El seguimiento de Winsock usa el seguimiento de eventos para Windows (ETW), una instalación de seguimiento de uso general y alta velocidad proporcionada por el sistema operativo. Mediante el uso de un mecanismo de almacenamiento en búfer y registro implementado en el kernel, ETW proporciona un mecanismo de seguimiento para los eventos producidos por las aplicaciones en modo de usuario y los controladores de dispositivo en modo kernel. Además, ETW ofrece la capacidad de habilitar y deshabilitar el registro dinámicamente, lo que facilita la realización de un seguimiento detallado en entornos de producción sin necesidad de reinicios ni reinicios de la aplicación. El mecanismo de registro usa búferes escritos en el disco por un subproceso de escritor asincrónico. Esto permite que las aplicaciones de servidor a gran escala escriban eventos con un mínimo de desorden. ETW se introdujo por primera vez Windows 2000. Se agregó compatibilidad con el seguimiento de Winsock mediante ETW en Windows Vista y versiones posteriores. Para obtener información general sobre ETW, vea Mejorar la depuración y el ajuste [del rendimiento con ETW.](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

El seguimiento de Winsock solo se puede habilitar en el nivel de sistema operativo para todos los procesos y subprocesos que se ejecutan en un equipo. Actualmente, el seguimiento de Winsock no se puede habilitar para un solo proceso o subproceso. Cuando el seguimiento de eventos de red de Winsock está habilitado, se hace un seguimiento de todas las aplicaciones de socket (IPv4 e IPv6) de un equipo.

En los temas siguientes se describe el seguimiento de Winsock con más detalle:

-   [Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
-   [Control del seguimiento de Winsock](control-of-winsock-tracing.md)
-   [Detalles del seguimiento de eventos de Winsock Network](winsock-tracing-event-details.md)
-   [Detalles del seguimiento de cambios del catálogo de Winsock](winsock-layered-service-provider-tracing-event-details.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Depuración y seguimiento de instalaciones](debug-and-trace-facilities-2.md)
</dt> </dl>

 

 
