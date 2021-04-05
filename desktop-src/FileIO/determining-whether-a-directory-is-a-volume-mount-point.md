---
description: Cómo determinar si un directorio especificado es una carpeta montada.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Determinar si un directorio es una carpeta montada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912314"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a>Determinar si un directorio es una carpeta montada

Resulta útil para determinar si un directorio es una carpeta montada cuando, por ejemplo, se usa una aplicación de copia de seguridad o de búsqueda que está limitada a un volumen. Este tipo de aplicación puede obtener información sobre varios volúmenes si usa funciones como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para crear carpetas montadas para los demás volúmenes del volumen en el que la aplicación está limitada. Para obtener más información, vea [crear carpetas montadas](mounting-and-dismounting-a-volume.md).

Para determinar si un directorio especificado es una carpeta montada, llame primero a la función [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) e inspeccione la marca de **\_ \_ \_ punto de reanálisis del atributo de archivo** en el valor devuelto para ver si el directorio tiene un punto de análisis asociado. Si es así, utilice las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) y [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) para obtener la etiqueta de reanálisis en el miembro **dwReserved0** de la estructura de [**\_ \_ datos de búsqueda de Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) . Para determinar si el punto de reanálisis es una carpeta montada (y no otra forma de punto de análisis), compruebe si el valor de la etiqueta es igual al punto de montaje de la **\_ etiqueta de reanálisis \_ \_ \_ de e/s**. Para obtener más información, vea [puntos de reanálisis](reparse-points.md).

Para obtener el volumen de destino de una carpeta montada, utilice la función [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .

De forma similar, puede determinar si un punto de análisis es un vínculo simbólico comprobando si el valor de etiqueta es el **\_ \_ \_ SYMLINK de etiqueta de reanálisis de e/s**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de atributo de archivo**](file-attribute-constants.md)
</dt> </dl>

 

 



