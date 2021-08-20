---
title: Extensiones de nombre de archivo
description: Extensiones de nombre de archivo
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Windows Metarchivos multimedia, extensiones
- Windows Metarchivos multimedia, extensiones de nombre de archivo
- metafiles,extensions
- metarchivos, extensiones de nombre de archivo
- Windows Multimedia, metarchivos
- extensiones de nombre de archivo para Windows metarchivos multimedia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c69c36a5865b3496cf63e8cc08d73b9187f5107b14bf0bbb0d52b462e90c88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054993"
---
# <a name="file-name-extensions"></a>Extensiones de nombre de archivo

Hay directrices específicas para el uso de extensiones de nombre de archivo para Windows metarchivos multimedia. Windows Las extensiones de nombre de metarchivo multimedia se usan para identificar los distintos tipos de archivos Windows multimedia. Una extensión de nombre de archivo proporciona a un proveedor de software independiente (ISV) información sobre los requisitos de representación de una aplicación que usa una extensión determinada y permite a los autores de contenido dirigirse a tipos generales de reproductores multimedia.

Las instrucciones de extensión de nombre de archivo se enumeran en la tabla siguiente. Se recomienda usar el tipo MIME de un archivo, ubicado en el encabezado de archivo, para la identificación del tipo de archivo.



| Extensión de nombre de archivo | Tipo de MIME      | Contenido del archivo                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .wma                | audio/x-ms-wma | Windows Archivo multimedia solo con contenido de audio. Normalmente se usa para descargar y reproducir archivos o para transmitir contenido.                                                                             |
| .wmv                | video/x-ms-wmv | Windows Archivo multimedia con contenido de audio o vídeo. Normalmente se usa para descargar y reproducir archivos o para transmitir contenido.                                                                     |
| .asf                | video/x-ms-asf | Contenido heredado. Normalmente se usa para descargar y reproducir archivos o para transmitir contenido. Puede contener contenido de audio o vídeo. Normalmente se usa para descargar y reproducir archivos o para transmitir contenido. |
| .wm                 | video/x-ms-wm  | Reservada                                                                                                                                                                                |
| .desenlace                | audio/x-ms-suba | Metarchivos que hacen Windows archivos multimedia con extensiones de nombre de archivo .asf, .wma o .rchivo.                                                                                             |
| .wvx                | video/x-ms-wvx | Metarchivos que hacen referencia a Windows archivos multimedia con extensiones de nombre de archivo .wma, .wmv, .wvx o .rchivo.                                                                                       |
| .asx                | video/x-ms-asf | Metarchivos que hacen referencia Windows archivos multimedia con extensiones de nombre de archivo .wma, .wmv, .wvx, .asf o .asx.                                                                           |
| .wmx                | video/x-ms-wvx | Reservado.                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentarios

El scripting y la administración de derechos digitales (DRM) deben ser compatibles con cualquier aplicación que represente Windows multimedia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Windows Referencia de elementos de metarchivo multimedia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guía de metarchivo multimedia**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Referencia de metarchivo multimedia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




