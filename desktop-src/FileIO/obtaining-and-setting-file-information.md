---
description: Funciones que se van a usar para obtener y establecer información de archivo.
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: Obtener y establecer información de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913530"
---
# <a name="obtaining-and-setting-file-information"></a>Obtener y establecer información de archivos

En los temas siguientes se describe cómo obtener y establecer información de archivo.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                             | Descripción                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recuperando información de tipo de archivo](retrieving-file-type-information.md)<br/>                               | La función [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) recupera el tipo de un archivo: disco, carácter (como una consola), canalización o desconocido.<br/>                                                                                                                                               |
| [Determinar el tamaño de un archivo](determining-the-size-of-a-file.md)<br/>                                   | La función [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera el tamaño de un archivo.<br/>                                                                                                                                                                                                      |
| [Buscar uno o varios archivos](searching-for-one-or-more-files.md)<br/>                                 | Una aplicación puede buscar en el directorio actual todos los nombres de archivo que coinciden con un patrón determinado mediante las funciones [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)y [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .<br/> |
| [Establecer y obtener la marca de tiempo de un archivo](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | Las aplicaciones pueden recuperar y establecer la fecha y la hora en que se crea un archivo, se modifica por última vez o se obtiene acceso por última vez mediante las funciones [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) y [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .<br/>                                                                         |
| [Determinar la página de códigos del juego de caracteres actual](determining-the-current-character-set-code-page.md)<br/> | La función [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) determina si las funciones de e/s de archivo usan la página de códigos del juego de caracteres ANSI o OEM.<br/>                                                                                                                               |



 

 

