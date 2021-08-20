---
description: Cómo determinar si un directorio especificado es una carpeta montada.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Determinar si un directorio es una carpeta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12c0af53a63f64164604a5f8f22532add3dded1a46d19d96354c0da37e12d4d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150598"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a>Determinar si un directorio es una carpeta montada

Resulta útil determinar si un directorio es una carpeta montada cuando, por ejemplo, usa una aplicación de copia de seguridad o de búsqueda que se limita a un volumen. Esta aplicación puede llegar a información sobre varios volúmenes si usa funciones como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para crear carpetas montadas para los demás volúmenes del volumen al que está limitada la aplicación. Para obtener más información, vea [Crear carpetas montadas.](mounting-and-dismounting-a-volume.md)

Para determinar si un directorio especificado es una carpeta montada, llame primero a la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) e inspeccione la marca **FILE ATTRIBUTE \_ \_ REPARSE \_ POINT** en el valor devuelto para ver si el directorio tiene un punto de análisis asociado. Si es así, use las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) para obtener la etiqueta reparse en el **miembro dwReserved0** de la estructura [**FIND DATA \_ \_ de WIN32.**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) Para determinar si el punto de análisis es una carpeta montada (y no otra forma de punto de análisis), pruebe si el valor de etiqueta es igual al valor **IO \_ REPARSE \_ TAG MOUNT \_ \_ POINT**. Para obtener más información, vea [Puntos de reanción.](reparse-points.md)

Para obtener el volumen de destino de una carpeta montada, use la [**función GetVolumeNameForVolumeMountPoint.**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw)

De forma similar, puede determinar si un punto de análisis es un vínculo simbólico mediante la prueba de si el valor de etiqueta es **IO \_ REPARSE \_ TAG \_ SYMLINK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de atributo de archivo**](file-attribute-constants.md)
</dt> </dl>

 

 



