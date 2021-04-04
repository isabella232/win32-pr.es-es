---
title: Instrucciones de extensión de metarchivo
description: Instrucciones de extensión de metarchivo
ms.assetid: 079fac31-7a6f-4775-a337-870ad25a56a0
keywords:
- Metaarchivos de Windows Media, extensiones
- Metaarchivos de Windows Media, extensiones de nombre de archivo
- metaarchivos, extensiones
- metaarchivos, extensiones de nombre de archivo
- Windows Media, metaarchivos
- extensiones de nombre de archivo para los metaarchivos de Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2793b19576e26096bc30c834666828cf9ed29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076296"
---
# <a name="metafile-extension-guidelines"></a>Instrucciones de extensión de metarchivo

Una extensión de nombre de archivo proporciona a un fabricante de software independiente (ISV) información sobre los requisitos de representación de una aplicación que usa la extensión, y permite a los autores de contenido dirigirse a tipos generales de reproductores.

Las extensiones de nombre de metarchivo de Windows Media se utilizan para identificar el formato de los archivos de Windows Media a los que hace referencia un metarchivo. Los metaarchivos de Windows Media con extensiones. Wax,. wvx o. ASX hacen referencia a archivos con extensiones. WMA,. WMV y. ASF, respectivamente. Todos los metaarchivos, independientemente de la extensión de nombre de archivo usada, tienen la etiqueta del elemento **ASX** al principio del archivo con el atributo de **versión** especificado.

En la tabla siguiente se muestran los tipos de archivos multimedia a los que hace referencia cada tipo de extensión de nombre de archivo de metarchivo. Las columnas enumeran las extensiones de nombre de archivo multimedia y las extensiones de nombre de metarchivo de lista de filas. Una X en una columna indica un tipo de archivo multimedia al que se puede hacer referencia mediante una extensión de nombre de archivo de metarchivo determinada.



| Extensión | .asf | .wma | .wmv |
|-----------|------|------|------|
| . wvx      | X    | X    | X    |
| . Wax      | X    | X    |      |
| .asx      | X    |      |      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Extensiones de nombre de archivo**](file-name-extensions.md)
</dt> <dt>

[**Listas de reproducción de metarchivos**](metafile-playlists.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




