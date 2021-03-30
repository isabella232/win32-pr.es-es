---
title: Subtipos de medios sin comprimir
description: Subtipos de medios sin comprimir
ms.assetid: 5586e62a-d0f5-45cc-a690-4efa244b3f32
keywords:
- Windows Media Format SDK, tipos de medios
- Advanced Systems Format (ASF), tipos de medios
- ASF (formato de sistemas avanzados), tipos de medios
- SDK de Windows Media Format, subtipos de medios sin comprimir
- Formato de sistemas avanzados (ASF), subtipos de medios sin comprimir
- ASF (formato de sistemas avanzados), subtipos de medios sin comprimir
- tipos de medios, subtipos de medios sin comprimir
- subtipos de medios sin comprimir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7ea730b480f738caa6e0eeccb8674f3cdc4c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775133"
---
# <a name="uncompressed-media-subtypes"></a>Subtipos de medios sin comprimir

En la tabla siguiente se enumeran los subtipos de medios no comprimidos. Estos son tipos que se usan como formatos de entrada y salida, y formatos para secuencias sin comprimir. No todos los tipos de las tablas siguientes se admiten de todas formas. Los tipos de formato de entrada y salida admitidos se pueden enumerar mediante códec en el escritor y en el lector sincrónico/asincrónico, respectivamente. Para obtener información sobre los tipos admitidos para las secuencias sin comprimir, consulte [uso de secuencias de audio y vídeo sin comprimir](using-uncompressed-audio-and-video-streams.md).

Los distintos tipos de vídeo RGB y de paleta RGB enumerados aquí definen los colores con el formato RGB, en el que cada color se representa mediante los valores de intensidad de los componentes rojo, verde y azul del píxel. Cada valor de intensidad puede oscilar entre 0 y 255, para unos 16.780.000 colores únicos. RGB se traduce fácilmente en los valores de color que se usan para los monitores de equipo, que utilizan fósforo rojo, verde y azul para mostrar el color. Los tipos de vídeo de paleta deben incluir información de la paleta directamente después de la estructura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) . Del mismo modo, el vídeo de 16 bits requiere información de campo de bits, que debe incluirse después de la estructura WMVIDEOINFOHEADER.

Algunos de los subtipos de medios de la tabla siguiente proporcionan menos colores de los que es capaz el sistema RGB, como se describe en la columna Descripción. En los tipos RGB con paleta, los colores de la paleta representan valores RGB, pero se especifican mediante un valor que indica la posición del color en la paleta.



| Subtipo de medios sin comprimir | Descripción                                                                                                                                                                                                              |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMMEDIASUBTYPE \_ RGB1       | Vídeo RGB de paleta con 1 bit de color que representa 2 colores. Normalmente se usa para las imágenes monocromáticas.                                                                                                                         |
| WMMEDIASUBTYPE \_ RGB4       | Vídeo RGB de paleta con 4 bits de color que representan 16 colores.                                                                                                                                                           |
| WMMEDIASUBTYPE \_ RGB8       | Vídeo RGB de paleta con 8 bits de color que representan 256 colores.                                                                                                                                                          |
| WMMEDIASUBTYPE \_ RGB565     | Vídeo RGB con 16 bits de color que representan 65.536 colores. Este formato utiliza 5 bits para rojo, 6 bits para verde y 5 bits para azul.                                                                                         |
| WMMEDIASUBTYPE \_ RGB555     | Vídeo RGB con 16 bits de color que representan 32.768 colores. Este formato utiliza 5 bits para cada color y omite el decimosexto bit.                                                                                           |
| WMMEDIASUBTYPE \_ RGB24      | Vídeo RGB con 24 bits de color que representan todos los 16.777.216 colores disponibles para el esquema de representación de color RGB. Este formato usa 8 bits para cada valor de intensidad de color.                                                |
| WMMEDIASUBTYPE \_ RGB32      | Vídeo RGB con 32 bits de color que representan todos los 16.777.216 colores disponibles para el esquema de representación de color RGB. Este formato usa 8 bits para cada color y reserva los 8 bits restantes para la información de transparencia. |
| WMMEDIASUBTYPE \_ i420       | Vídeo YUV almacenado en formato 4:2:0 plano, donde aparece el plano U primero, seguido del plano V.                                                                                                                      |
| WMMEDIASUBTYPE \_ IYUV       | Idéntico a i420.                                                                                                                                                                                                       |
| WMMEDIASUBTYPE \_ YV12       | Vídeo YUV almacenado en formato planar 4:2:0, donde aparece primero el plano V, seguido del plano U. YV12 es idéntico a i420, salvo que se cambian los planos de ti y V.                                               |
| WMMEDIASUBTYPE \_ YUY2       | Vídeo YUV almacenado en formato 4:2:2 empaquetado.                                                                                                                                                                                 |
| WMMEDIASUBTYPE \_ UYVY       | Vídeo YUV almacenado en formato 4:2:2 empaquetado. Similar a YUY2, pero con diferente orden de datos.                                                                                                                            |
| WMMEDIASUBTYPE \_ YVYU       | Vídeo YUV almacenado en formato 4:2:2 empaquetado. Similar a YUY2, pero con diferente orden de datos.                                                                                                                            |
| WMMEDIASUBTYPE \_ P422       | Vídeo YUV almacenado con un formato planar 4:2:2.                                                                                                                                                                            |
| WMMEDIASUBTYPE \_ YVU9       | Vídeo YUV almacenado en formato 16:1:1 plano.                                                                                                                                                                                |
| WMMEDIASUBTYPE \_ PCM        | Datos de audio sin comprimir almacenados mediante la modulación de código pulse.                                                                                                                                                              |
| DRM de WMMEDIASUBTYPE \_        | Datos de audio sin comprimir pero cifrados usados con la ruta de acceso de audio segura.                                                                                                                                                       |
| WMSCRIPTTYPE \_ TwoStrings   | Comandos de script que se componen de una cadena que contiene el tipo de comando y una cadena que contiene los datos del comando. Este es el único tipo de script admitido en el SDK de Windows Media Format.                                     |
| Webstream de WMMEDIASUBTYPE \_  | Datos de transferencia de archivos que contienen archivos HTML y componentes para la transmisión por secuencias Web.                                                                                                                                               |
| IMAGEN de videoWMMEDIASUBTYPE \_ | Tipo de entrada para el códec de imagen de Windows Media Video 9. Los ejemplos son una combinación de imágenes de mapa de bits y datos de transformación.                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Asignar formatos de salida**](assigning-output-formats.md)
</dt> <dt>

[**Subtipos de medios comprimidos**](compressed-media-subtypes.md)
</dt> <dt>

[**Identificadores de tipo de medio**](media-type-identifiers.md)
</dt> <dt>

[**Tipos de medios**](media-types.md)
</dt> <dt>

[**Para enumerar los formatos de entrada**](to-enumerate-input-formats.md)
</dt> </dl>

 

 




