---
description: 'Más información sobre: Macros de API de gabinete'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macros de API de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525ec84e3e857c4819b1689cade2ed0f7267dffbd8a0e0da02251a03f8d4a36a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668273"
---
# <a name="cabinet-api-macros"></a>Macros de API de gabinete

En esta sección se detallan las macros que usa Cabinet API:

## <a name="fci-macros"></a>FCI Macros

FCI usa las siguientes macros:



| Macro                                              | Descripción                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**FNFCIALLOC**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | Se usa para asignar memoria en un contexto de FCI.<br/>                                          |
| [**FNFCICLOSE**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | Se usa para cerrar un archivo.<br/>                                                               |
| [**FNFCIDELETE**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | Se usa para eliminar un archivo.<br/>                                                              |
| [**FNFCIFILEPLACED**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | Se usa para notificar cuándo se coloca un archivo en el archivador.<br/>                                |
| [**FNFCIFREE**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | Se usa para liberar memoria asignada previamente en un contexto de FCI.<br/>                         |
| [**FNFCIGETNEXTCABINET**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | Se usa para solicitar información para el siguiente gabinete.<br/>                                   |
| [**FNFCIGETOPENINFO**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | Se usa para abrir un archivo y recuperar la fecha, hora y atributos del archivo.<br/>                   |
| [**FNFCIGETTEMPFILE**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | Se usa para obtener un nombre de archivo temporal.<br/>                                               |
| [**FNFCIOPEN**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | Se usa para abrir un archivo en un contexto de FCI.<br/>                                              |
| [**FNFCIREAD**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | Se usa para leer datos de un archivo.<br/>                                                      |
| [**FNFCISEEK**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | Se usa para mover un puntero de archivo a una ubicación especificada.<br/>                                |
| [**FNFCISTATUS**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | Se usa para actualizar el usuario.<br/>                                                            |
| [**FNFCIWRITE**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | Se usa para escribir datos en un archivo.<br/>                                                       |
| [**TCOMPfromLZXWindow**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | Convierte el tamaño de windows en un valor TCOMP de LXZ [**para FCIAddFile.**](/windows/desktop/api/Fci/nf-fci-fciaddfile)<br/> |



 

## <a name="fdi-macros"></a>FDI Macros

FDI usa las macros siguientes:



| Macro                              | Descripción                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**FNALLOC**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | Se usa para asignar memoria en un contexto de FDI.<br/>                               |
| [**FNCLOSE**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | Se usa para cerrar un archivo en un contexto de FDI.<br/>                                  |
| [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | Se usa para actualizar la aplicación en el estado del descodificador.<br/>             |
| [**FNFREE**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | Se usa para liberar memoria asignada previamente en un contexto de FDI.<br/>              |
| [**FNOPEN**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | Se usa para abrir un archivo en un contexto de FDI.<br/>                                   |
| [**FNREAD**](/windows/desktop/api/fdi/nf-fdi-fnread)           | Se usa para leer datos de un archivo en un contexto de FDI.<br/>                         |
| [**FNSEEK**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | Se usa para mover un puntero de archivo a la ubicación especificada en un contexto de FDI.<br/> |
| [**FNWRITE**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | Se usa para escribir datos en un archivo en un contexto de FDI.<br/>                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de La API de Archivador](cabinet-api-reference.md)
</dt> <dt>

[Uso de Cabinet API](using-the-cabinet-api.md)
</dt> </dl>

 

 




