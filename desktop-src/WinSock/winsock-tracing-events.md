---
description: Detalles de los eventos de seguimiento de Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Eventos de seguimiento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b2f36991a187d32359694956efcc7b7e3243ac17efd769db454848b5f87e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821989"
---
# <a name="winsock-tracing-events"></a>Eventos de seguimiento de Winsock

En esta sección se describe información detallada sobre detalles específicos de los eventos de seguimiento de Winsock.

El seguimiento de Winsock es una característica de solución de problemas que se puede habilitar en los archivos binarios comerciales para realizar un seguimiento de determinados eventos de socket de Windows con una sobrecarga mínima. Esta característica permite mejores funcionalidades de diagnóstico para desarrolladores y soporte técnico de productos. El seguimiento de eventos de red de Winsock admite operaciones de socket de seguimiento para aplicaciones IPv4 e IPv6. El seguimiento de cambios del catálogo de Winsock admite el seguimiento de los cambios realizados en el catálogo de Winsock por proveedores de servicios por capas (LSP).

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows filtering platform](../fwp/windows-filtering-platform-start-page.md).

 

El seguimiento de Winsock usa el seguimiento de eventos para Windows (ETW), una instalación de seguimiento de alta velocidad de uso general proporcionada por el sistema operativo. ETW proporciona un mecanismo de seguimiento para los eventos producidos por las aplicaciones en modo de usuario y los controladores de dispositivo en modo kernel. ETW puede habilitar y deshabilitar el registro dinámicamente, lo que facilita la realización de un seguimiento detallado en entornos de producción sin necesidad de reiniciar o reiniciar la aplicación. Se ha agregado compatibilidad con el seguimiento de Winsock mediante ETW en Windows Vista y versiones posteriores. Para obtener información general sobre ETW, vea [Mejorar la depuración y el ajuste del rendimiento con ETW.](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)

En la lista siguiente se proporciona información detallada para cada evento de seguimiento de Winsock. Para obtener información adicional sobre cualquier evento, haga clic en el nombre del evento.



| Nombre del evento                                                            | Descripción                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**AFD \_ EVENT \_ CREATE**](afd-event-create.md)                        | Evento de seguimiento de red winsock para una operación de creación de sockets.                            |
| [**AFD \_ EVENT \_ CLOSE**](afd-event-close.md)                          | Evento de seguimiento de red winsock para la operación de cierre de socket.                                 |
| [**INSTALACIÓN DE LSP DE WINSOCK \_ WS2HELP \_ \_**](winsock-ws2help-lsp-install.md) | Evento de cambio del catálogo de Winsock para una operación de instalación del proveedor de servicios por capas (LSP). |
| [**WINSOCK \_ WS2HELP \_ LSP \_ REMOVE**](winsock-ws2help-lsp-remove.md)   | Evento de cambio del catálogo de Winsock para una operación de eliminación del proveedor de servicios en capas (LSP).      |
| [**WINSOCK \_ WS2HELP \_ LSP \_ DISABLE**](winsock-ws2help-lsp-disable.md) | Evento de cambio del catálogo de Winsock para una operación de deshabilitación del proveedor de servicios en capas (LSP).      |
| [**WINSOCK \_ WS2HELP \_ LSP \_ RESET**](winsock-ws2help-lsp-reset.md)     | Evento de cambio del catálogo de Winsock para una operación de restablecimiento del catálogo de Winsock.                       |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar la depuración y el ajuste del rendimiento con ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Control del seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Detalles del seguimiento de eventos de Winsock Network](winsock-tracing-event-details.md)
</dt> <dt>

[Detalles del seguimiento de cambios del catálogo de Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
