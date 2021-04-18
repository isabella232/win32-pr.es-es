---
title: Funciones de ProjFS
description: Las siguientes funciones se declaran en projectedfslib. h.
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 40f3f2aec8e52d2caafdcf1554d0871e9bb185de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105720208"
---
# <a name="projfs-functions"></a>Funciones de ProjFS

Las siguientes funciones se declaran en projectedfslib. h.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**PrjAllocateAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjallocatealignedbuffer) | Asigna un búfer que cumple los requisitos de alineación de memoria del dispositivo de almacenamiento de la instancia de virtualización. |
| [**PrjClearNegativePathCache**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjclearnegativepathcache) | Purga la memoria caché de rutas de acceso negativa de la instancia de virtualización, si está activa. |
| [**PrjCompleteCommand**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjcompletecommand) | Indica que el proveedor ha finalizado el procesamiento de una devolución de llamada de la que se devolvió previamente HRESULT_FROM_WIN32 (ERROR_IO_PENDING). |
| [**PrjDeleteFile**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdeletefile) | Permite a un proveedor eliminar un elemento que se ha almacenado en la memoria caché del sistema de archivos local. |
| [**PrjDoesNameContainWildCards**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards) | Determina si un nombre contiene caracteres comodín. |
| [**PrjFileNameCompare**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare) | Compara dos nombres de archivo y devuelve un valor que indica su orden de intercalación relativa. |
| [**PrjFileNameMatch**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch) | Determina si un nombre de archivo coincide con un modelo de búsqueda. |
| [**PrjFillDirEntryBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer) | Proporciona información para un archivo o directorio a una enumeración. |
| [**PrjFillDirEntryBuffer2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2) | Proporciona información para un archivo o directorio a una enumeración y permite al llamador especificar información extendida. |
| [**PrjFreeAlignedBuffer**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfreealignedbuffer) | Libera un búfer asignado. |
| [**PrjGetOnDiskFileState**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetondiskfilestate) | Obtiene el estado del archivo en disco para un archivo o directorio. |
| [**PrjGetVirtualizationInstanceInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjgetvirtualizationinstanceinfo) | Recupera información sobre la instancia de virtualización. |
| [**PrjMarkDirectoryAsPlaceholder**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder) | Convierte un directorio existente en un marcador de posición de directorio. |
| [**PrjStartVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing) | Configura una instancia de virtualización de ProjFS y la inicia, para que esté disponible para la e/s de servicio e invoque devoluciones de llamada en el proveedor. |
| [**PrjStopVirtualizing**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing) | Detiene una instancia de virtualización de ProjFS en ejecución, lo que hace que no esté disponible para la e/s del servicio o implique devoluciones de llamada en el proveedor. |
| [**PrjUpdateFileIfNeeded**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded) | Permite a un proveedor actualizar un elemento que se ha almacenado en la memoria caché del sistema de archivos local. |
| [**PrjWriteFileData**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwritefiledata) | Envía el contenido del archivo a ProjFS. |
| [**PrjWritePlaceholderInfo**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo) | Envía metadatos de archivo o directorio a ProjFS. |
| [**PrjWritePlaceholderInfo2**](/windows/win32/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo2) | Envía metadatos de archivo o directorio a ProjFS y permite al llamador especificar información extendida. |
