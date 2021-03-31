---
title: YCbCr (efecto)
description: Convierte los datos de JPEG YCbCr de submuestreo plano y croma a RGB.
ms.assetid: E4492996-54DA-4C5F-B44C-8FBE97C8DD7D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c581effbadecc19c39161d2a2ec4af051d4195d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079589"
---
# <a name="ycbcr-effect"></a>YCbCr (efecto)

Convierte los datos de JPEG YC<sub>b</sub><sub>r r</sub> de submuestra plano y croma a RGB. Este efecto supone que los datos<sub>de</sub>C<sub>r</sub> de la YC tienen un formato conforme con el estándar JPEG. Los datos de las entradas se pueden obtener de IWICPlanarBitmapSourceTransform. El efecto YC<sub>b</sub>C<sub>r</sub> requiere dos entradas: el primero debe ser un mapa de bits de el formato de DXGI \_ \_ R8 que contenga datos de luminancia, y el segundo debe ser un mapa de bits de R8G8 de formato de dxgi \_ \_ que contenga datos de croma de submuestreo. Para obtener más información sobre el uso de este efecto, consulte [compatibilidad con JPEG YCbCr](/windows/desktop/wic/jpeg-ycbcr-support).

El CLSID para este efecto es CLSID \_ D2D1YCbCr.

-   [Propiedades del efecto](#effect-properties)
-   [Modos de submuestreo](#subsampling-modes)
-   [Modos de interpolación](#interpolation-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                          | Descripción                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ChromaSubsampling<br/> Submuestreo de croma D2D1 \_ YCbCr \_ \_<br/>    | Especifica el submuestreo de croma de la imagen de croma de entrada. <br/> El tipo es el \_ \_ submuestreo de croma D2D1 YCbCr \_ .<br/> El valor predeterminado es \_ \_ submuestreo de croma D2D1 YCbCr \_ \_ auto.<br/>                                                                                                |
| TransformMatrix <br/> \_Matriz de \_ transformación de propiedades \_ \_ de D2D1 YCbCr<br/> | [Matriz 3x2](/previous-versions/dotnet/netframework-3.0/ms750596(v=vs.85)) que especifica la transformación afín alineada por el eje de la imagen. Las transformaciones alineadas del eje incluyen giros de escala, volteo y 90 grados. <br/> El tipo es D2D1 \_ Matrix \_ 3x2 \_ F.<br/> El valor predeterminado es Matrix3x2F:: Identity ().<br/> |
| InterpolationMode<br/> D2D1 \_ \_ modo de interpolación YCbCr \_<br/>    | El modo de interpolación.<br/> El tipo es D2D1 \_ YCbCr \_ Interpolation \_ mode.<br/>                                                                                                                                                                                                             |



 

## <a name="subsampling-modes"></a>Modos de submuestreo



| Enumeración                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ Submuestreo automático de croma D2D1 YCbCr \_<br/> | Este modo intenta deducir el submuestreo de croma de los límites de las imágenes de entrada. Cuando se selecciona esta opción, el plano más pequeño se muestra al tamaño del plano más grande y este efecto s rectángulo de salida es la intersección de los dos planos. Al usar este modo, se debe tener cuidado al aplicar efectos a los planos de entrada que cambian los límites de la imagen, como la transformación de borde, de modo que se mantenga la relación de tamaño deseada entre los planos. <br/> |
| \_SUBmuestreo de croma D2D1 YCBCR \_ \_ \_ 420<br/>  | El plano de croma es submuestreado horizontalmente por y submuestreado verticalmente por. Cuando se selecciona esta opción, el plano de croma se muestrea horizontal y verticalmente por 2x y este efecto s rectángulo de salida es la intersección de los dos planos.<br/>                                                                                                                                                                                                                          |
| \_SUBmuestreo de croma D2D1 YCBCR \_ \_ \_ 422<br/>  | La submuestra horizontal del plano de croma. Cuando se selecciona esta opción, el plano de croma se muestrea horizontalmente en 2x y este efecto s rectángulo de salida es la intersección de los dos planos.<br/>                                                                                                                                                                                                                                                                        |
| \_SUBmuestreo de croma D2D1 YCBCR \_ \_ \_ 444<br/>  | No se muestra el plano de croma. Cuando se selecciona esta opción, el rectángulo de salida s es la intersección de los dos planos.<br/>                                                                                                                                                                                                                                                                                                                                            |
| \_SUBmuestreo de croma D2D1 YCBCR \_ \_ \_ 440<br/>  | El plano de croma es submuestreado verticalmente por. Cuando se selecciona esta opción, el plano de croma se muestrea verticalmente en 2x y este efecto s rectángulo de salida es la intersección de los dos planos.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="interpolation-modes"></a>Modos de interpolación



| Enumeración                                             | Descripción                                                                                                                                                                                          |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de interpolación YCbCr \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ \_ modo de interpolación YCbCr \_ \_ lineal                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo usa más tiempo de procesamiento que el modo vecino más cercano, pero genera una imagen de mayor calidad.                                           |
| D2D1 \_ \_ modo de interpolación YCbCr \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ el \_ modo de interpolación YCbCr \_ \_ lineal de varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| D2D1 \_ \_ modo de interpolación YCbCr \_ \_ anisotrópico           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ YCbCr \_ modo de interpolación de \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del mapa de bits de salida depende de la matriz de transformación que se aplica a la imagen.

El efecto realiza la operación de transformación y, a continuación, aplica un cuadro de límite alrededor del resultado. El mapa de bits de salida es el tamaño del cuadro de límite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------------------|
| Cliente mínimo compatible | Aplicaciones de la tienda Windows de Windows 8.1 \[ Desktop apps \|\]            |
| Servidor mínimo compatible | Aplicaciones de escritorio de Windows Server 2012 R2 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado                   | d2d1effects \_ 1. h                                              |
| Biblioteca                  | d2d1. lib, dxguid. lib                                          |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> <dt>

[Compatibilidad con JPEG YCbCr](/windows/desktop/wic/jpeg-ycbcr-support)
</dt> <dt>

[**IWICPlanarBitmapSourceTransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
</dt> </dl>

 

