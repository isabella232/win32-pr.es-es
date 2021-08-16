---
title: Efecto de origen de mapa de bits
description: Use el efecto de origen de mapa de bits para generar un id2D1Image a partir de un IWICBitmapSource para usarlo como entrada en un gráfico de efectos.
ms.assetid: 86646111-208A-4E6D-A28C-7B23A1742D24
keywords:
- efecto de origen de mapa de bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19889372c7ebd4268f1b6fd8b77c360f290cc416631e9fb5e1cd3a0b0320844c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833334"
---
# <a name="bitmap-source-effect"></a>Efecto de origen de mapa de bits

Use el efecto de origen de mapa de bits para generar [**un id2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) a partir de [**un IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) para usarlo como entrada en un gráfico de efectos. Este efecto realiza el escalado y la rotación en la CPU. También puede generar opcionalmente un mapa mipmap de memoria del sistema, que puede ser una optimización del rendimiento para escalar activamente imágenes muy grandes a varias resoluciones reducidas.

> [!Note]  
> El efecto de origen del mapa de bits toma su entrada como una propiedad, no como una entrada de imagen. Debe usar el [**método SetValue,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) no [**el método SetInput.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) La *propiedad WicBitmapSource* es donde se especifican los datos de entrada de la imagen.

 

El CLSID para este efecto es CLSID \_ D2D1BitmapSource.

-   [Propiedades de efecto](#effect-properties)
-   [Modos de interpolación](#interpolation-modes)
-   [Orientación](#orientation)
-   [Modos alfa](#alpha-modes)
-   [Comentarios:](#remarks)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WicBitmapSource<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ WIC \_ BITMAP \_ SOURCE<br/>         | [IWICBitmapSource que](/windows/desktop/wic/-wic-imp-iwicbitmapsource) contiene los datos de imagen que se cargarán.<br/> El tipo es [IWICBitmapSource.](/windows/desktop/wic/-wic-imp-iwicbitmapsource)<br/> El valor predeterminado es NULL.<br/>                                                                                                                                                                                                                   |
| Escala<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ SCALE<br/>                                 | La cantidad de escala en la dirección X e Y. El efecto multiplica el ancho por el valor X y el alto por el valor Y. Esta propiedad es un vector D2D1 \_ \_ 2F definido como: (escala X, escala Y). Las cantidades de escala son FLOAT, sin unidad y deben ser positivas o 0.<br/> El tipo es D2D1 \_ VECTOR \_ 2F.<br/> El valor predeterminado es {1.0f, 1.0f}.<br/>                                                                           |
| InterpolationMode.<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ INTERPOLATION \_ MODE<br/>      | Modo de interpolación utilizado para escalar la imagen. Consulte [Modos de interpolación](#interpolation-modes) para obtener más información.<br/> Si el modo deshabilita el mapa mip, BitmapSouce almacenará en caché la imagen en la resolución determinada por las propiedades Scale y EnableDPICorrection.<br/> El tipo es D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE.<br/> El valor predeterminado es D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ LINEAR.<br/> |
| EnableDPICorrection<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ ENABLE \_ DPI \_ CORRECTION<br/> | Si establece esta opción en TRUE, el efecto escalará la imagen de entrada para convertir el PPP notificado por [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) en el valor de PPP del contexto del dispositivo. El efecto usa el modo de interpolación que se establece con la propiedad InterpolationMode. Si establece esta opción en FALSE, el efecto usa un valor de PPP de 96,0 para la imagen de salida.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>   |
| AlphaMode<br/> D2D1 \_ BITMAPSOURCE \_ PROP \_ ALPHA \_ MODE<br/>                       | Modo alfa de la salida. Puede ser premultiplicado o recta. Consulte [Modos alfa para](#alpha-modes) obtener más información.<br/> El tipo es D2D1 \_ BITMAPSOURCE \_ ALPHA \_ MODE.<br/> El valor predeterminado es D2D1 \_ BITMAPSOURCE \_ ALPHA MODE \_ \_ PREMULTIPLIED.<br/>                                                                                                                                                              |
| Orientación<br/> ORIENTACIÓN DE LA PROPIEDAD BITMAPSOURCE D2D1 \_ \_ \_<br/>                     | Una operación de volteo o rotación que se va a realizar en la imagen. Consulte [Orientación](#orientation) para obtener más información.<br/> El tipo es D2D1 \_ BITMAPSOURCE \_ ORIENTATION.<br/> El valor predeterminado es D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ DEFAULT.<br/>                                                                                                                                                                                 |



 

## <a name="interpolation-modes"></a>Modos de interpolación

El efecto interpola mediante este modo cuando escala una imagen o cuando corrige el ppp. Los modos de interpolación que usa este efecto se calculan mediante la CPU, no la GPU.



| Nombre                                                       | Descripción                                                                                                                                                                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ NEAREST \_ NEIGHBOR | Muestrea el punto más cercano y lo usa. No genera un mapa mip.                                                                                                                                                           |
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ LINEAR            | Usa una muestra de cuatro puntos y una interpolación lineal. No genera un mapa mip.                                                                                                                                                        |
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ CUBIC             | Usa un kernel cúbica de 16 muestras para la interpolación. No genera un mapa mip.                                                                                                                                                          |
| FANT DEL MODO \_ \_ DE INTERPOLACIÓN DE BITMAPSOURCE \_ D2D1 \_              | Usa la interpolación de ventilador wic, igual que la [**interfaz IWICBitmapScaler.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapscaler) No genera un mapa mip.                                                                                       |
| D2D1 \_ BITMAPSOURCE \_ INTERPOLATION \_ MODE \_ MIPMAP \_ LINEAR    | Genera la cadena mipmap en la memoria del sistema mediante la interpolación bilineal. Para cada mapa mip, el efecto se escala al múltiplo más cercano de 0,5 mediante la interpolación bilineal y, a continuación, escala la cantidad restante mediante la interpolación lineal. |



 

## <a name="orientation"></a>Orientación

La propiedad Orientation se puede usar para aplicar una marca de orientación EXIF incrustada dentro de una imagen.



| Nombre                                                                    | Descripción                                                        |
|-------------------------------------------------------------------------|--------------------------------------------------------------------|
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ DEFAULT                                | Predeterminada. El efecto no cambia la orientación de la entrada.   |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ FLIP \_ HORIZONTAL                       | Voltea la imagen horizontalmente.                                      |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE180                   | Gira la imagen en el sentido de las agujas del reloj 180 grados.                           |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE180 \_ FLIP \_ HORIZONTAL | Gira la imagen en el sentido de las agujas del reloj 180 grados y la voltea horizontalmente. |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE270 \_ FLIP \_ HORIZONTAL | Gira la imagen en el sentido de las agujas del reloj 270 grados y la voltea horizontalmente. |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE90                    | Gira la imagen en el sentido de las agujas del reloj 90 grados.                            |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE90 \_ FLIP \_ HORIZONTAL  | Gira la imagen en el sentido de las agujas del reloj 90 grados y la voltea horizontalmente.  |
| D2D1 \_ BITMAPSOURCE \_ ORIENTATION \_ ROTATE \_ CLOCKWISE270                   | Gira la imagen 270 grados en el sentido de las agujas del reloj.                           |



 

Este fragmento de código muestra cómo convertir valores de orientación EXIF (definidos en propkey.h) a valores DE \_ ORIENTACIÓN BITMAPSOURCE D2D1. \_


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
| D2D1 \_ BITMAPSOURCE \_ ALPHA \_ MODE \_ PREMULTIPLIED | La salida del efecto usa alfa premultiplicado.<br/> |
| MODO ALFA D2D1 \_ BITMAPSOURCE \_ \_ \_ STRAIGHT      | La salida del efecto usa alfa recta.<br/>      |



 

## <a name="remarks"></a>Comentarios

Para optimizar el rendimiento al usar WIC y [Direct2D](./direct2d-portal.md) juntos, debe usar [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) para convertir a un formato de píxel adecuado basado en el escenario de la aplicación y la precisión nativa de la imagen.

En la mayoría de los casos, la canalización de [Direct2D](./direct2d-portal.md) de la aplicación solo requiere 8 bits por canal (bpc) de precisión o la imagen solo proporciona una precisión de 8 bpc y, por tanto, debe convertir a \_ GUID WICPixelFormat32bppPBGRA. Sin embargo, si desea aprovechar la precisión adicional proporcionada por una imagen (por ejemplo, un JPEG-XR o TIFF almacenado con una precisión superior a 8 bpc), debe usar un formato de píxel basado en RGBA. En la tabla siguiente se proporcionan más detalles.



| Precisión deseada   | Precisión nativa de la imagen | Formato de píxel recomendado                |
|---------------------|-------------------------------|-----------------------------------------|
| 8 bits por canal  | <= 8 bits por canal      | GUID \_ WICPixelFormat32bppPBGRA          |
| Lo más alto posible | <= 8 bits por canal      | GUID \_ WICPixelFormat32bppPBGRA          |
| Lo más alto posible | > 8 bits por canal       | Orden del canal RGBA, alfa premultiplicado |



 

Dado que muchos formatos de imagen admiten varios niveles de precisión, debe usar [**IWICBitmapSource::GetPixelFormat**](/windows/desktop/wic/-wic-codec-iwicbitmapsource-getpixelformat-proxy) para obtener el formato de píxel nativo de la imagen y, a continuación, usar [**IWICPixelFormatInfo**](/windows/desktop/api/wincodec/nn-wincodec-iwicpixelformatinfo) para determinar cuántos bits por canal de precisión están disponibles para ese formato. Además, tenga en cuenta que no todo el hardware admite formatos de píxeles de alta precisión. En esos casos, es posible que la aplicación tenga que volver al dispositivo WARP para admitir la alta precisión.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| Windows Store\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

