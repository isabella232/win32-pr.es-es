---
title: Subtipos de medios sin comprimir
description: Subtipos de medios sin comprimir
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- Windows SDK de formato multimedia, tipos multimedia
- Formato de sistemas avanzados (ASF), tipos de medios
- ASF (formato de sistemas avanzados), tipos de medios
- Windows SDK de formato multimedia, subtipos multimedia sin comprimir
- Formato de sistemas avanzados (ASF), subtipos de medios sin comprimir
- ASF (formato de sistemas avanzados), subtipos de medios sin comprimir
- tipos de medios, subtipos de medios sin comprimir
- subtipos de medios sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdbd691a3b43a83656feffa1be114b5180d24cc5e29359b4168a4656d99fd03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807345"
---
# <a name="uncompressed-media-subtypes"></a>Subtipos de medios sin comprimir

En la tabla siguiente se enumeran los subtipos de medios sin comprimir. Se trata de tipos que se usan como formatos de entrada y salida, y formatos para secuencias sin comprimir. No todos los tipos de las tablas siguientes se admiten de todas formas. Los tipos de formato de entrada y salida admitidos se pueden enumerar por códec en el escritor y lector/lector sincrónico, respectivamente. Para obtener información sobre los tipos admitidos para secuencias sin comprimir, vea [Using Uncompressed Audio and Video Secuencias](using-uncompressed-audio-and-video-streams.md).

Los distintos tipos de vídeo RGB y RGB que se enumeran aquí definen colores con el formato RGB, en el que cada color se representa mediante los valores de intensidad de los componentes rojo, verde y azul del píxel. Cada valor de intensidad puede oscilar entre 0 y 255, para unos 16,78 millones de colores únicos. RGB se traduce fácilmente en valores de color que se usan para los monitores de equipo, que usan colores rojo, verde y azul para mostrar el color. Los tipos de vídeo con color verde deben incluir información de paleta directamente después de la [**estructura WMVIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) Del mismo modo, el vídeo de 16 bits requiere información de campo de bits, que debe incluirse después de la estructura WMVIDEOINFOHEADER.

Algunos de los subtipos de medios de la tabla siguiente proporcionan menos colores de los que el sistema RGB es capaz, como se describe en la columna Descripción. En los tipos RGB de color azulado, los colores de la paleta representan valores RGB, pero se especifican mediante un valor que indica la posición del color en la paleta.



| Subtipo de medio sin comprimir | Descripción                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ RGB1       | Vídeo RGB coloreado con 1 bit de color que representa 2 colores. Normalmente se usa para imágenes monocromáticas.                                                                                                                         |
| WMMEDIASUBTYPE \_ RGB4       | Vídeo RGB con 4 bits de color que representan 16 colores.                                                                                                                                                           |
| WMMEDIASUBTYPE \_ RGB8       | Vídeo RGB perfilado con 8 bits de color que representan 256 colores.                                                                                                                                                          |
| WMMEDIASUBTYPE \_ RGB565     | Vídeo RGB con 16 bits de color que representan 65 536 colores. Este formato usa 5 bits para rojo, 6 bits para verde y 5 bits para azul.                                                                                         |
| WMMEDIASUBTYPE \_ RGB555     | Vídeo RGB con 16 bits de color que representan 32 768 colores. Este formato usa 5 bits para cada color y omite el decimosexto bit.                                                                                           |
| WMMEDIASUBTYPE \_ RGB24      | Vídeo RGB con 24 bits de color que representan los 16 777 216 colores disponibles para el esquema de representación de color RGB. Este formato usa 8 bits para cada valor de intensidad de color.                                                |
| WMMEDIASUBTYPE \_ RGB32      | Vídeo RGB con 32 bits de color que representan los 16 777 216 colores disponibles para el esquema de representación de color RGB. Este formato usa 8 bits para cada color y reserva los 8 bits restantes para la información de transparencia. |
| WMMEDIASUBTYPE \_ I420       | Vídeo de YUV almacenado en formato planar 4:2:0, donde el plano U aparece primero, seguido del plano V.                                                                                                                      |
| WMMEDIASUBTYPE \_ IYUV       | Idéntico a I420.                                                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ YV12       | Vídeo de YUV almacenado en formato planar 4:2:0, donde el plano V aparece primero, seguido del plano U. YV12 es idéntico a I420, salvo que los planos usted y V se cambian.                                               |
| WMMEDIASUBTYPE \_ YUY2       | Vídeo de YUV almacenado en formato empaquetado 4:2:2.                                                                                                                                                                                 |
| WMMEDIASUBTYPE \_ UYVY       | Vídeo de YUV almacenado en formato empaquetado 4:2:2. Similar a YUY2, pero con una ordenación de datos diferente.                                                                                                                            |
| WMMEDIASUBTYPE \_ YVYU       | Vídeo de YUV almacenado en formato empaquetado 4:2:2. Similar a YUY2, pero con una ordenación de datos diferente.                                                                                                                            |
| WMMEDIASUBTYPE \_ P422       | Vídeo YUV almacenado con un formato planar 4:2:2.                                                                                                                                                                            |
| WMMEDIASUBTYPE \_ YVU9       | Vídeo de YUV almacenado en formato planar 16:1:1.                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ PCM        | Datos de audio sin comprimir almacenados mediante la compresión de código de pulso.                                                                                                                                                              |
| WMMEDIASUBTYPE \_ DRM        | Datos de audio sin comprimir pero cifrados que se usan con la ruta de acceso de audio segura.                                                                                                                                                       |
| WMSCRIPTTYPE \_ TwoStrings   | Comandos de script que constan de una cadena que contiene el tipo de comando y una cadena que contiene los datos del comando. Este es el único tipo de script admitido en el SDK Windows Media Format.                                     |
| WMMEDIASUBTYPE \_ WebStream  | Datos de transferencia de archivos que contienen archivos HTML y componentes para streaming web.                                                                                                                                               |
| WMMEDIASUBTYPE \_ VIDEOIMAGE | Tipo de entrada para el códec Windows imagen de Media Video 9. Los ejemplos son una combinación de imágenes de mapa de bits y datos de transformación.                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Asignación de formatos de salida**](assigning-output-formats.md)
</dt> <dt>

[**Subtipos de medios comprimidos**](compressed-media-subtypes.md)
</dt> <dt>

[**Identificadores de tipo de medio**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de medios**](media-types.md)
</dt> <dt>

[**Para enumerar los formatos de entrada**](to-enumerate-input-formats.md)
</dt> </dl>

 

 




