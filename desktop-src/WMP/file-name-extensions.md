---
title: Extensiones de nombre de archivo
description: Extensiones de nombre de archivo
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
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
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695440"
---
# <a name="file-name-extensions"></a>Extensiones de nombre de archivo

Existen directrices específicas para el uso de extensiones de nombre de archivo para los metaarchivos de Windows Media. Las extensiones de nombre de metarchivo de Windows Media se utilizan para identificar los distintos tipos de archivos de Windows Media. Una extensión de nombre de archivo proporciona a un fabricante de software independiente (ISV) información sobre los requisitos de representación de una aplicación que utiliza una extensión determinada, y permite a los autores de contenido dirigirse a tipos generales de reproductores multimedia.

En la tabla siguiente se enumeran las instrucciones de extensión de nombre de archivo. Se recomienda usar el tipo MIME de un archivo, situado en el encabezado del archivo, para la identificación del tipo de archivo.



| Extensión de nombre de archivo | Tipo de MIME      | Contenido del archivo                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .wma                | audio/x-MS-WMA | Archivo de Windows Media con contenido de audio únicamente. Normalmente se usa para descargar y reproducir archivos o para transmitir contenido.                                                                             |
| .wmv                | vídeo/x-MS-WMV | Archivo de Windows Media con contenido de audio o vídeo. Normalmente se usa para descargar y reproducir archivos o para transmitir contenido.                                                                     |
| .asf                | vídeo/x-MS-ASF | Contenido heredado. Normalmente se usa para descargar y reproducir archivos o para transmitir contenido. Puede contener contenido de audio o vídeo. Normalmente se usa para descargar y reproducir archivos o para transmitir contenido. |
| .wm                 | vídeo/x-MS-WM  | Reservado                                                                                                                                                                                |
| . Wax                | audio/x-MS-Wax | Metaarchivos que hacen referencia a archivos de Windows Media con las extensiones de nombre de archivo. ASF,. WMA o. Wax.                                                                                             |
| . wvx                | vídeo/x-MS-wvx | Metaarchivos que hacen referencia a archivos de Windows Media con las extensiones de nombre de archivo. WMA,. wmv,. wvx o. Wax.                                                                                       |
| .asx                | vídeo/x-MS-ASF | Metaarchivos que hacen referencia a archivos de Windows Media con las extensiones de nombre de archivo. WMA,. Wax,. wmv,. wvx,. ASF o. ASX.                                                                           |
| . WMX                | vídeo/x-MS-wvx | Reservado.                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

El scripting y la administración de derechos digitales (DRM) deben ser compatibles con cualquier aplicación que represente archivos de Windows Media.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de elementos de metarchivo de Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guía de metarchivo de Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Referencia de metarchivos de Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




