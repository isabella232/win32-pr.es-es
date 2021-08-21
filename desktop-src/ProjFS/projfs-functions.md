---
title: Funciones ProjFS
description: Las siguientes funciones se declaran en projectedfslib.h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 47e4371a7d00ca6564223f7415a69ee0308bf8757041b49f5df9f214e6c978b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792612"
---
# <a name="projfs-functions"></a>Funciones ProjFS

Las siguientes funciones se declaran en projectedfslib.h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**PrjAllocateAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | Asigna un búfer que cumple los requisitos de alineación de memoria del dispositivo de almacenamiento de la instancia de virtualización. |
| [**PrjClearNegativePathCache**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | Purga la caché de rutas de acceso negativas de la instancia de virtualización, si está activa. |
| [**PrjCompleteCommand**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | Indica que el proveedor ha completado el procesamiento de una devolución de llamada de la que había devuelto anteriormente HRESULT_FROM_WIN32(ERROR_IO_PENDING). |
| [**PrjDeleteFile**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | Permite a un proveedor eliminar un elemento que se ha almacenado en caché en el sistema de archivos local. |
| [**PrjDoesNameContainWildCards**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | Determina si un nombre contiene caracteres comodín. |
| [**PrjFileNameCompare**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | Compara dos nombres de archivo y devuelve un valor que indica su orden de intercalación relativo. |
| [**PrjFileNameMatch**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | Determina si un nombre de archivo coincide con un patrón de búsqueda. |
| [**PrjFillDirEntryBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | Proporciona información para un archivo o directorio a una enumeración. |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | Proporciona información para un archivo o directorio a una enumeración y permite al autor de la llamada especificar información extendida. |
| [**PrjFreeAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | Libera un búfer asignado. |
| [**PrjGetOnDiskFileState**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | Obtiene el estado del archivo en disco para un archivo o directorio. |
| [**PrjGetVirtualizationInstanceInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | Recupera información sobre la instancia de virtualización. |
| [**PrjMarkDirectoryAsPlaceholder**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | Convierte un directorio existente en un marcador de posición de directorio. |
| [**PrjStartVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | Configura una instancia de virtualización ProjFS y la inicia, lo que hace que esté disponible para la E/S de servicio e invoca devoluciones de llamada en el proveedor. |
| [**PrjStopVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | Detiene una instancia de virtualización ProjFS en ejecución, lo que hace que no esté disponible para la E/S de servicio o que implique devoluciones de llamada en el proveedor. |
| [**PrjUpdateFileIfNeeded**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | Permite a un proveedor actualizar un elemento que se ha almacenado en caché en el sistema de archivos local. |
| [**PrjWriteFileData**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | Envía el contenido del archivo a ProjFS. |
| [**PrjWritePlaceholderInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | Envía metadatos de archivo o directorio a ProjFS. |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | Envía metadatos de archivo o directorio a ProjFS y permite al autor de la llamada especificar información extendida. |
