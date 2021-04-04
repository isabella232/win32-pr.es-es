---
title: Efecto de origen de mapa de bits
description: Use el efecto de origen del mapa de bits para generar un ID2D1Image de un IWICBitmapSource para usarlo como entrada en un gráfico de efectos.
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- efecto de origen de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a439c94f0f520b318b3cb3511775dbec58b6e139
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905578"
---
# <a name="bitmap-source-effect"></a>Efecto de origen de mapa de bits

Use el efecto de origen del mapa de bits para generar un [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) de un [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) para usarlo como entrada en un gráfico de efectos. Este efecto realiza el ajuste de escala y la rotación en la CPU. Opcionalmente, también puede generar un mipmap de memoria del sistema, que puede ser una optimización del rendimiento para escalar activamente imágenes muy grandes a diferentes resoluciones reducidas.

> [!Note]  
> El efecto de origen del mapa de bits toma su entrada como una propiedad, no como una entrada de imagen. Debe usar el método [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) , no el método [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) . La propiedad *WicBitmapSource* es donde se especifican los datos de entrada de la imagen.

 

El CLSID para este efecto es CLSID \_ D2D1BitmapSource.

-   [Propiedades del efecto](#effect-properties)
-   [Modos de interpolación](#interpolation-modes)
-   [Orientación](#orientation)
-   [Modos alfa](#alpha-modes)
-   [Comentarios:](#remarks)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WicBitmapSource<br/> D2D1 \_ BITMAPSOURCE \_ prop \_ \_ código fuente de mapa de bits WIC \_<br/>         | Objeto [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) que contiene los datos de la imagen que se van a cargar.<br/> El tipo es [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource).<br/> El valor predeterminado es NULL.<br/>                                                                                                                                                                                                                   |
| Escala<br/> \_Escala D2D1 BITMAPSOURCE \_ prop \_<br/>                                 | La cantidad de escala en la dirección X e y. El efecto multiplica el ancho por el valor X y el alto por el valor Y. Esta propiedad es un vector D2D1 se \_ \_ define como: (escala X, escala y). Las cantidades de escala son FLOAT, sin unidades y deben ser positivas o 0.<br/> El tipo es D2D1 \_ Vector \_ 2F.<br/> El valor predeterminado es {1.0 f, 1.0 f}.<br/>                                                                           |
| InterpolationMode.<br/> D2D1 \_ BITMAPSOURCE \_ prop ( \_ modo de interpolación) \_<br/>      | El modo de interpolación usado para escalar la imagen. Vea [modos de interpolación](#interpolation-modes) para obtener más información.<br/> Si el modo deshabilita el mipmap, BitmapSouce almacenará en caché la imagen en la resolución determinada por las propiedades scale y EnableDPICorrection.<br/> El tipo es D2D1 \_ BITMAPSOURCE \_ Interpolation \_ mode.<br/> El valor predeterminado es D2D1 \_ BITMAPSOURCE \_ Interpolation \_ Mode \_ linear.<br/> |
| EnableDPICorrection<br/> D2D1 \_ BITMAPSOURCE \_ prop \_ habilitar \_ corrección de PPP \_<br/> | Si se establece en TRUE, el efecto escalará la imagen de entrada para convertir el valor de PPP indicado por [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) en el valor de PPP del contexto del dispositivo. El efecto usa el modo de interpolación que se establece con la propiedad InterpolationMode. Si se establece en FALSE, el efecto usa un valor de PPP de 96,0 para la imagen de salida.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>   |
| AlphaMode<br/> D2D1 \_ BITMAPSOURCE \_ prop \_ ( \_ modo alfa)<br/>                       | Modo alfa de la salida. Puede ser premultiplicado o recto. Vea [modos alfa](#alpha-modes) para obtener más información.<br/> El tipo es D2D1 \_ BITMAPSOURCE \_ alpha \_ mode.<br/> El valor predeterminado es D2D1 \_ BITMAPSOURCE \_ alpha \_ Mode \_ premultiplicado.<br/>                                                                                                                                                              |
| Orientación<br/> Orientación de D2D1 \_ BITMAPSOURCE \_ prop \_<br/>                     | Operación de giro y/o rotación que se va a realizar en la imagen. Vea [orientación](#orientation) para obtener más información.<br/> El tipo es D2D1 \_ BITMAPSOURCE \_ Orientation.<br/> El valor predeterminado es D2D1 \_ BITMAPSOURCE \_ Orientation \_ default.<br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a>Modos de interpolación

El efecto se interpola mediante este modo cuando escala una imagen o cuando corrige el PPP. La CPU calcula los modos de interpolación que usa este efecto, no la GPU.



| Nombre                                                       | Descripción                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de interpolación BITMAPSOURCE \_ \_ más cercano \_ | Muestrea el punto único más cercano y lo usa. No genera un mipmap.                                                                                                                                                           |
| \_Modo de \_ interpolación D2D1 BITMAPSOURCE \_ \_ lineal            | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. No genera un mipmap.                                                                                                                                                        |
| D2D1 \_ el \_ modo de interpolación BITMAPSOURCE \_ \_             | Usa un kernel cúbico de ejemplo 16 para la interpolación. No genera un mipmap.                                                                                                                                                          |
| D2D1 \_ \_ modo de interpolación BITMAPSOURCE \_ \_ fant              | Usa la interpolación fant de WIC, igual que la interfaz [**IWICBitmapScaler**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) . No genera un mipmap.                                                                                       |
| D2D1 \_ BITMAPSOURCE \_ modo de interpolación \_ \_ MIP \_ lineal    | Genera una cadena de mapas MIP en la memoria del sistema mediante la interpolación bilineal. Para cada mipmap, el efecto se escala al múltiplo más cercano de 0,5 mediante la interpolación bilineal y, a continuación, escala la cantidad restante mediante la interpolación lineal. |



 

## <a name="orientation"></a>Orientación

La propiedad Orientation se puede usar para aplicar una marca de orientación EXIF incrustada dentro de una imagen.



| Nombre                                                                    | Descripción                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| D2D1 \_ \_ valor predeterminado de orientación BITMAPSOURCE \_                                | Predeterminada. El efecto no cambia la orientación de la entrada.   |
| D2D1 \_ BITMAPSOURCE \_ orientación \_ horizontal voltear \_                       | Voltea la imagen horizontalmente.                                      |
| D2D1 \_ BITMAPSOURCE \_ orientación \_ \_ CLOCKWISE180                   | Gira la imagen a la derecha 180 grados.                           |
| D2D1 \_ BITMAPSOURCE \_ orientación \_ girar \_ CLOCKWISE180 \_ voltear \_ horizontalmente | Gira la imagen a la derecha 180 grados y la voltea horizontalmente. |
| D2D1 \_ BITMAPSOURCE \_ orientación \_ girar \_ CLOCKWISE270 \_ voltear \_ horizontalmente | Gira la imagen a la derecha 270 grados y la voltea horizontalmente. |
| D2D1 \_ BITMAPSOURCE \_ orientación \_ \_ CLOCKWISE90                    | Gira la imagen a la derecha 90 grados.                            |
| D2D1 \_ BITMAPSOURCE \_ orientación \_ girar \_ CLOCKWISE90 \_ voltear \_ horizontalmente  | Gira la imagen a la derecha 90 grados y la voltea horizontalmente.  |
| D2D1 \_ BITMAPSOURCE \_ orientación \_ \_ CLOCKWISE270                   | Gira la imagen a la derecha 270 grados.                           |



 

Este fragmento de código muestra cómo convertir los valores de orientación EXIF (definidos en propkey. h) en \_ valores de orientación de D2D1 BITMAPSOURCE \_ .


```C++
#include <propkey.h>
#include <d2d1effects.h>

D2D1_BITMAPSOURCE_ORIENTATION GetBitmapSourceOrientation(unsigned short PhotoOrientation)
{
       switch (PhotoOrientation)
       {
       case PHOTO_ORIENTATION_NORMAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       case PHOTO_ORIENTATION_FLIPHORIZONTAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE180:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180;
       case PHOTO_ORIENTATION_FLIPVERTICAL:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_TRANSPOSE: 
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE270:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90;
       case PHOTO_ORIENTATION_TRANSVERSE:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270_FLIP_HORIZONTAL;
       case PHOTO_ORIENTATION_ROTATE90:
              return D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270;
       default:
              return D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT;
       }
}
```



## <a name="alpha-modes"></a>Modos alfa



| Nombre                                           | Descripción                                            |
|------------------------------------------------|--------------------------------------------------------|
| Premultiplicado por el \_ \_ modo alfa D2D1 BITMAPSOURCE \_ \_ | La salida del efecto usa alfa premultiplicado.<br/> |
| D2D1 \_ BITMAPSOURCE \_ alpha \_ Mode \_ Straight      | La salida del efecto usa alfa recto.<br/>      |



 

## <a name="remarks"></a>Observaciones

Para optimizar el rendimiento al usar WIC y [Direct2D](./direct2d-portal.md) juntos, debe usar [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) para convertir a un formato de píxel adecuado en función del escenario de la aplicación y la precisión nativa de la imagen.

En la mayoría de los casos, la canalización de la aplicación s [Direct2D](./direct2d-portal.md) solo requiere 8 bits por canal (BPC) de precisión, o la imagen solo proporciona una precisión de 8 bpc y, por lo tanto, debe convertir a GUID \_ WICPixelFormat32bppPBGRA. Sin embargo, si desea aprovechar la precisión adicional que proporciona una imagen (por ejemplo, un archivo JPEG-XR o TIFF almacenado con una precisión superior a 8 bpc), debe usar un formato de píxel basado en RGBA. En la tabla siguiente se proporcionan más detalles.



| Precisión deseada   | Precisión nativa de la imagen | Formato de píxel recomendado                |
|---------------------|-------------------------------|-----------------------------------------|
| 8 bits por canal  | <= 8 bits por canal      | GUID \_ WICPixelFormat32bppPBGRA          |
| Lo más alto posible | <= 8 bits por canal      | GUID \_ WICPixelFormat32bppPBGRA          |
| Lo más alto posible | > 8 bits por canal       | Orden del canal RGBA, alfa premultiplicado |



 

Dado que muchos formatos de imagen admiten varios niveles de precisión, debe usar [**IWICBitmapSource:: GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) para obtener el formato de píxel nativo de la imagen y, a continuación, usar [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) para determinar cuántos bits por canal de precisión están disponibles para ese formato. Además, tenga en cuenta que no todo el hardware admite formatos de píxeles de alta precisión. En estos casos, es posible que la aplicación necesite revertir al dispositivo de ALABEo para admitir alta precisión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Servidor mínimo compatible | Windows 8 y actualización de la plataforma para aplicaciones de escritorio de Windows 7 aplicaciones de la \[ \| tienda Windows\] |
| Encabezado                   | d2d1effects. h                                                                      |
| Biblioteca                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

