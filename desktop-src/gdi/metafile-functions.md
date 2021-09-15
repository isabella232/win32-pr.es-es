---
description: Las funciones siguientes se usan con metarchivos de formato mejorado.
ms.assetid: 93a17a8c-308b-4442-933e-fedc8b9a84b0
title: Funciones de metarchivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd137095fe0659871291ec4e8670054cc2899d10
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475944"
---
# <a name="metafile-functions"></a>Funciones de metarchivo

Las funciones siguientes se usan con metarchivos de formato mejorado.



| Función                                                             | Descripción                                                                                                            |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile)                         | Cierra un contexto de dispositivo de metarchivo mejorado.                                                                            |
| [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea)                           | Copia el contenido de un metarchivo de formato mejorado en un archivo especificado.                                                |
| [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)                       | Crea un contexto de dispositivo para un metarchivo de formato mejorado.                                                              |
| [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)                       | Elimina un metarchivo de formato mejorado o un identificador de metarchivo de formato mejorado.                                             |
| [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)                           | Función de devolución de llamada definida por la aplicación que se usa con la función EnumEnhMetaFile.                                       |
| [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile)                           | Enumera los registros dentro de un metarchivo de formato mejorado.                                                             |
| [**GdiComment**](/windows/desktop/api/Wingdi/nf-wingdi-gdicomment)                                     | Copia un comentario de un búfer en un metarchivo de formato mejorado especificado.                                              |
| [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea)                             | Crea un identificador que identifica el metarchivo de formato mejorado almacenado en el archivo especificado.                            |
| [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits)                     | Recupera el contenido del metarchivo de formato mejorado especificado y los copia en un búfer.                        |
| [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)       | Recupera una descripción de texto opcional de un metarchivo de formato mejorado y copia la cadena en el búfer especificado. |
| [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader)                 | Recupera el registro que contiene el encabezado del metarchivo de formato mejorado especificado.                                 |
| [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) | Recupera las entradas opcionales de la paleta del metarchivo mejorado especificado.                                               |
| [**GetMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilea)                                   | GetMetaFile ya no está disponible para su uso a partir Windows 2000. En su lugar, [**use GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea).  |
| [**GetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getwinmetafilebits)                     | Convierte los registros de formato mejorado de un metarchivo en Windows de formato predeterminado.                                      |
| [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile)                           | Muestra la imagen almacenada en el metarchivo de formato mejorado especificado.                                                 |
| [**PlayEnhMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafilerecord)               | Reproduce un registro de metarchivo mejorado mediante la ejecución de las funciones de interfaz de dispositivo gráfico (GDI) identificadas por el registro. |
| [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)                     | Crea un metarchivo de formato mejorado basado en memoria a partir de los datos especificados.                                               |
| [**SetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setwinmetafilebits)                     | Convierte un metarchivo del formato Windows anterior al nuevo formato mejorado.                                          |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

Las siguientes funciones están obsoletas. se proporcionan para la compatibilidad con Windows metarchivos con formato de archivo.

-   [**CloseMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closemetafile)
-   [**CopyMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copymetafilea)
-   [**CreateMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createmetafilea)
-   [**DeleteMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deletemetafile)
-   [**EnumMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enummetafile)
-   [**EnumMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-mfenumproc)
-   [**GetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilebitsex)
-   [**PlayMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafile)
-   [**PlayMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafilerecord)
-   [**SetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-setmetafilebitsex)

 

 
