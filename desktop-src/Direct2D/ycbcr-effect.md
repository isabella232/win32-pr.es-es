---
title: Efecto YCbCr
description: Convierte los datos planares y submuestreos JPEG YCbCr en RGB.
ms.assetid: E4492996-54DA-4C5F-B44C-8FBE97C8DD7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5302300cc539571fabb1c3d786686ffc514636133391e706fc5963002656764
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636095"
---
# <a name="ycbcr-effect"></a>Efecto YCbCr

Convierte los datos planares y de submuestreo JPEG YC<sub>b</sub>C<sub>r</sub> en RGB. Este efecto supone que los datos de YC<sub>b</sub>C<sub>r</sub> tienen el formato conforme al estándar JPEG. Los datos de las entradas se pueden obtener de IWICPlanarBitmapSourceTransform. El efecto YC<sub>b</sub>C<sub>r</sub> requiere dos entradas; El primero debe ser un mapa de bits DXGI FORMAT R8 que contenga datos luma y el segundo debe ser un mapa de bits \_ \_ DXGI FORMAT R8G8 que contenga datos \_ \_ submuestreados de color. Para obtener más información sobre el uso de este efecto, vea [JPEG YCbCr Support](/windows/desktop/wic/jpeg-ycbcr-support).

El CLSID para este efecto es CLSID \_ D2D1YCbCr.

-   [Propiedades de efecto](#effect-properties)
-   [Modos de submuestreo](#subsampling-modes)
-   [Modos de interpolación](#interpolation-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                          | Descripción                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Submuestreo desubsampling<br/> SUBMUESTREO DE YCBCR DE D2D1 \_ \_ \_ YCBCR: SUBMUESTREO<br/>    | Especifica el submuestreo de la capa de entrada. <br/> El tipo es D2D1 \_ YCBCR \_ UNA \_ SUBMUESTREO.<br/> El valor predeterminado es D2D1 \_ YCBCR \_ UNA \_ SUBSAMPLING \_ AUTO.<br/>                                                                                                |
| TransformMatrix <br/> D2D1 \_ YCBCR \_ PROP \_ TRANSFORM \_ MATRIX<br/> | Matriz [3x2 que](/previous-versions/dotnet/netframework-3.0/ms750596(v=vs.85)) especifica la transformación afín alineada con el eje de la imagen. Las transformaciones alineadas del eje incluyen Escala, Volteos y giros de 90 grados. <br/> El tipo es D2D1 \_ MATRIX \_ 3X2 \_ F.<br/> El valor predeterminado es Matrix3x2F::Identity().<br/> |
| InterpolationMode<br/> MODO DE \_ INTERPOLACIÓN D2D1 \_ \_ YCBCR<br/>    | Modo de interpolación.<br/> El tipo es D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE.<br/>                                                                                                                                                                                                             |



 

## <a name="subsampling-modes"></a>Modos de submuestreo



| Enumeración                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SUBSAMPLING AUTO de D2D1 \_ YCBCR \_ \_ LORÓN \_ AUTO<br/> | Este modo intenta deducir el submuestreo de los límites de las imágenes de entrada. Cuando se selecciona esta opción, el plano más pequeño se muestrea al tamaño del plano más grande y el rectángulo de salida de este efecto es la intersección de los dos planos. Al usar este modo, se debe tener cuidado al aplicar efectos a los planos de entrada que cambian los límites de la imagen, como la transformación de borde, para que se mantenga la relación de tamaño deseada entre los planos. <br/> |
| SUBSAMPLING 420 de D2D1 \_ YCBCR \_ \_ LORÓN \_ 420<br/>  | El plano de mosaico se submuestra horizontalmente por y se submuestrea verticalmente por . Cuando se selecciona esta opción, el plano del mosaico se eleva horizontal y verticalmente por 2 veces y el rectángulo de salida de este efecto es la intersección de los dos planos.<br/>                                                                                                                                                                                                                          |
| SUBSAMPLING 422 de D2D1 \_ YCBCR \_ \_ LORÓN \_ 422<br/>  | El plano de mosaico se submuestrea horizontalmente mediante . Cuando se selecciona esta opción, el plano del mosaico se escala horizontalmente por 2 veces y el rectángulo de salida de este efecto es la intersección de los dos planos.<br/>                                                                                                                                                                                                                                                                        |
| SUBSAMPLING 444 DE D2D1 \_ YCBCR \_ \_ LORCO \_ 444<br/>  | El plano de zona no se submuestrea. Cuando se selecciona esta opción, el rectángulo de salida de este efecto es la intersección de los dos planos.<br/>                                                                                                                                                                                                                                                                                                                                            |
| SUBSAMPLING 440 de D2D1 \_ YCBCR \_ \_ LORÓN \_ 440<br/>  | El plano del mosaico se submuestrea verticalmente mediante . Cuando se selecciona esta opción, el plano del mosaico se eleva verticalmente en dos veces y el rectángulo de salida de este efecto es la intersección de los dos planos.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                             | Descripción                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto único más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ LINEAR                | Usa una muestra de cuatro puntos e interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.                                           |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ CUBIC                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un buen suavizado de alias perimetral. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| MODO DE \_ INTERPOLACIÓN D2D1 YCBCR \_ \_ \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ YCBCR \_ INTERPOLATION \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escala hacia abajo está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida depende de la matriz de transformación que se aplica a la imagen.

El efecto realiza la operación de transformación y, a continuación, aplica un rectángulo delimitador alrededor del resultado. El mapa de bits de salida es el tamaño del cuadro de límite.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible | \[Windows 8.1 aplicaciones de escritorio \| Windows aplicaciones de la Tienda\]            |
| Servidor mínimo compatible | Windows Server 2012 Aplicaciones de escritorio de R2 \[ \| Windows store\] |
| Header                   | d2d1effects \_ 1.h                                              |
| Biblioteca                  | d2d1.lib, dxguid.lib                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> <dt>

[JPEG YCbCr Support](/windows/desktop/wic/jpeg-ycbcr-support)
</dt> <dt>

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
</dt> </dl>

 

