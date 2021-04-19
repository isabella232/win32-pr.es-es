---
title: Funciones de prevención de pérdida de datos de punto de conexión
description: Funciones utilizadas por la característica de prevención de pérdida de datos del punto de conexión.
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: f8713a6a6051bf477b4f9c7f6f8a7430abf70a52
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495828"
---
# <a name="endpoint-data-loss-prevention-functions"></a>Funciones de prevención de pérdida de datos de punto de conexión

Funciones utilizadas por la característica de prevención de pérdida de datos del punto de conexión.



| Functions                                                       | Descripción                                                           |
|-------------------------------------------------------------------|-----------------------------------------------------------------------|
| [DlpNotifyCloseDocument](endpointdlp-dlpnotifyclosedocument.md)                       | Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del documento.                                  |
| [DlpNotifyCloseDocumentFile](endpointdlp-dlpnotifyclosedocumentfile.md)                       | Proporciona al sistema información sobre un documento antes de iniciar la operación de cierre del documento.                                  |
| [DlpNotifyEnterDropTarget](endpointdlp-dlpnotifyenterdroptarget.md)                       | Proporciona al sistema información sobre un documento cuando se introduce un destino de colocación.                                  |
| [DlpGetEnforcementApiVersion](endpointdlp-dlpgetenforcementapiversion.md)                       | Recupera la versión de la API de prevención de pérdida de datos (DLP) del punto de conexión en el dispositivo actual.                                  |
| [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md)                       | Notifica al sistema los modos de cumplimiento deseados para un conjunto de operaciones de prevención de pérdida de datos (DLP) de punto de conexión.                                  |
| [DlpMustPasteFromSystemClipboard](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | Determina si la aplicación debe extraer los datos del Portapapeles del sistema en lugar de tomar los datos de su caché interna.                                  |
| [DlpNotifyLeaveDropTarget](endpointdlp-dlpnotifyleavedroptarget.md)                       | Proporciona al sistema información sobre un documento cuando se sale de un destino de colocación.                                  |
| [DlpNotifyPostCopyToClipboard](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | Proporciona al sistema información sobre un documento una vez completada una operación de copia en el Portapapeles.  |
| [DlpNotifyPostDragDrop](endpointdlp-dlpnotifypostdragdrop.md)                         | Proporciona al sistema información sobre un documento una vez completada una operación de arrastrar y colocar.  |
| [DlpNotifyPostOpenDocument](endpointdlp-dlpnotifypostopendocument.md)                       | Proporciona al sistema información sobre un documento una vez completada la operación de apertura.                                  |
| [DlpNotifyPostOpenDocumentFile](endpointdlp-dlpnotifypostopendocumentfile.md)                       | Proporciona al sistema información sobre un documento una vez completada la operación de apertura.                                  |
| [DlpNotifyPostPasteFromClipboard](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | Proporciona al sistema información sobre un documento después de que se haya completado una operación de pegado del Portapapeles.                                  |
| [DlpNotifyPostPrint](endpointdlp-dlpnotifypostprint.md)                       | Proporciona al sistema información sobre un documento una vez completada una operación de impresión.                                  |
| [DlpNotifyPostSaveAsDocument](endpointdlp-dlpnotifypostsaveasdocument.md)                       | Proporciona al sistema información sobre un documento una vez completada la operación guardar como.                                  |
| [DlpNotifyPostStartPrint](endpointdlp-dlpnotifypoststartprint.md)                       | Proporciona al sistema información sobre un documento después de que se haya iniciado una operación de impresión.                                  |
| [DlpNotifyPostStashClipboard](endpointdlp-dlpnotifypoststashclipboard.md)                       | Proporciona al sistema información de estado una vez completada una operación de almacenamiento escalonado del Portapapeles.                                  |
| [DlpNotifyPreCopyToClipboard](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | Proporciona al sistema información sobre un documento antes de iniciar una operación de copia en el Portapapeles.  |
| [DlpNotifyPreDragDrop](endpointdlp-dlpnotifypredragdrop.md)                         | Proporciona al sistema información sobre un documento antes de iniciar una operación de arrastrar y colocar.  |
| [DlpNotifyPreOpenDocument](endpointdlp-dlpnotifypreopendocument.md)                         | Proporciona al sistema información sobre un documento antes de iniciar la operación de apertura.  |
| [DlpNotifyPreOpenDocumentFile](endpointdlp-dlpnotifypreopendocumentfile.md)                         | Proporciona al sistema información sobre un documento antes de iniciar la operación de apertura.  |
| [DlpNotifyPrePasteFromClipboard](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | Proporciona al sistema información sobre un documento antes de iniciar una operación de pegar desde el Portapapeles.  |
| [DlpNotifyPrePrint](endpointdlp-dlpnotifypreprint.md)                         | Proporciona al sistema información sobre un documento antes de iniciar una operación de impresión.  |
| [DlpNotifyPreSaveDocument](endpointdlp-dlpnotifypresaveasdocument.md)                       | Proporciona al sistema información sobre un documento antes de iniciar una operación de guardar como.                                  |
| [DlpNotifyPreStashClipboard](endpointdlp-dlpnotifyprestashclipboard.md)                       | Notifica al sistema antes de que se inicie una operación de almacenamiento escalonado en el Portapapeles.                                  |