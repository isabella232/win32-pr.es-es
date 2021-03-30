---
description: Detalles de eventos de seguimiento de Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Eventos de seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154239"
---
# <a name="winsock-tracing-events"></a>Eventos de seguimiento de Winsock

En esta sección se describe la información detallada sobre los detalles específicos de eventos de seguimiento de Winsock.

El seguimiento de Winsock es una característica de solución de problemas que se puede habilitar en los archivos binarios de venta directa para realizar un seguimiento de determinados eventos de Windows socket con una sobrecarga mínima. Esta característica permite mejorar las capacidades de diagnóstico de los desarrolladores y del soporte técnico. El seguimiento de eventos de red Winsock admite operaciones de socket de seguimiento para aplicaciones IPv4 e IPv6. El seguimiento de cambios del catálogo Winsock admite los cambios de seguimiento realizados en el catálogo Winsock por proveedores de servicios por capas (LSP).

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

El seguimiento de Winsock usa el seguimiento de eventos para Windows (ETW), un servicio de seguimiento de alta velocidad y de uso general que proporciona el sistema operativo. ETW proporciona un mecanismo de seguimiento para los eventos generados por las aplicaciones de modo de usuario y los controladores de dispositivos de modo kernel. ETW puede habilitar y deshabilitar el registro de forma dinámica, lo que facilita la realización de seguimientos detallados en entornos de producción sin necesidad de reinicios o reinicios de aplicaciones. Se ha agregado compatibilidad con el seguimiento de Winsock mediante ETW en Windows Vista y versiones posteriores. Para obtener información general sobre ETW, vea [mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).

La lista siguiente proporciona información detallada para cada evento de seguimiento de Winsock. Para obtener información adicional sobre cualquier evento, haga clic en el nombre del evento.



| Nombre del evento                                                            | Descripción                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_creación de eventos de AFD \_**](afd-event-create.md)                        | Evento de seguimiento de red Winsock para una operación de creación de Sockets.                            |
| [**\_cierre de evento de AFD \_**](afd-event-close.md)                          | Evento de seguimiento de red Winsock para la operación de cierre del socket.                                 |
| [**\_Instalación de WS2HELP de \_ LSP de Winsock \_**](winsock-ws2help-lsp-install.md) | Evento de cambio de catálogo Winsock para una operación de instalación de un proveedor de servicios por capas (LSP). |
| [**\_ \_ Quitar LSP de WS2HELP de Winsock \_**](winsock-ws2help-lsp-remove.md)   | Evento de cambio de catálogo Winsock para una operación de eliminación de un proveedor de servicios por capas (LSP).      |
| [**Deshabilitación de LSP de WINSOCK \_ WS2HELP \_ \_**](winsock-ws2help-lsp-disable.md) | Evento de cambio de catálogo Winsock para una operación de deshabilitación de un proveedor de servicios por capas (LSP).      |
| [**\_Restablecimiento de \_ LSP de WS2HELP de Winsock \_**](winsock-ws2help-lsp-reset.md)     | Evento de cambio de catálogo Winsock para una operación de restablecimiento del catálogo Winsock.                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Control de seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Detalles de seguimiento de eventos de red Winsock](winsock-tracing-event-details.md)
</dt> <dt>

[Detalles de seguimiento de cambios de catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
