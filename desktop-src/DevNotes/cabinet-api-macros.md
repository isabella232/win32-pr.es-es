---
description: 'Más información sobre: macros de API de archivo. cab'
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macros de API de archivo. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538302"
---
# <a name="cabinet-api-macros"></a>Macros de API de archivo. cab

En esta sección se detallan las macros usadas por la API del archivo. cab:

## <a name="fci-macros"></a>Macros FCI

Las siguientes macros las usa FCI:



| Macro                                              | Descripción                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**FNFCIALLOC**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | Se usa para asignar memoria en un contexto de FCI.<br/>                                          |
| [**FNFCICLOSE**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | Se utiliza para cerrar un archivo.<br/>                                                               |
| [**FNFCIDELETE**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | Se usa para eliminar un archivo.<br/>                                                              |
| [**FNFCIFILEPLACED**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | Se usa para notificar cuando se coloca un archivo en el archivo. cab.<br/>                                |
| [**FNFCIFREE**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | Se usa para liberar memoria asignada previamente en un contexto de FCI.<br/>                         |
| [**FNFCIGETNEXTCABINET**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | Se usa para solicitar información para el siguiente archivo. cab.<br/>                                   |
| [**FNFCIGETOPENINFO**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | Se usa para abrir un archivo y recuperar la fecha, la hora y los atributos del archivo.<br/>                   |
| [**FNFCIGETTEMPFILE**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | Se utiliza para obtener un nombre de archivo temporal.<br/>                                               |
| [**FNFCIOPEN**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | Se usa para abrir un archivo en un contexto de FCI.<br/>                                              |
| [**FNFCIREAD**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | Se utiliza para leer datos de un archivo.<br/>                                                      |
| [**FNFCISEEK**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | Se usa para trasladar un puntero de archivo a una ubicación especificada.<br/>                                |
| [**FNFCISTATUS**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | Se usa para actualizar el usuario.<br/>                                                            |
| [**FNFCIWRITE**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | Se utiliza para escribir datos en un archivo.<br/>                                                       |
| [**TCOMPfromLZXWindow**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | Convierte el tamaño de Windows en un valor de LXZ TCOMP para [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).<br/> |



 

## <a name="fdi-macros"></a>Macros FDI

FDI utiliza las siguientes macros:



| Macro                              | Descripción                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**FNALLOC**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | Se usa para asignar memoria en un contexto FDI.<br/>                               |
| [**FNCLOSE**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | Se utiliza para cerrar un archivo en un contexto FDI.<br/>                                  |
| [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | Se utiliza para actualizar la aplicación en el estado del descodificador.<br/>             |
| [**FNFREE**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | Se usa para liberar memoria asignada previamente en un contexto FDI.<br/>              |
| [**FNOPEN**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | Se usa para abrir un archivo en un contexto FDI.<br/>                                   |
| [**FNREAD**](/windows/desktop/api/fdi/nf-fdi-fnread)           | Se utiliza para leer datos de un archivo en un contexto FDI.<br/>                         |
| [**FNSEEK**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | Se usa para trasladar un puntero de archivo a la ubicación especificada en un contexto FDI.<br/> |
| [**FNWRITE**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | Se utiliza para escribir datos en un archivo en un contexto FDI.<br/>                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de contenedor](cabinet-api-reference.md)
</dt> <dt>

[Uso de la API de archivo. cab](using-the-cabinet-api.md)
</dt> </dl>

 

 




