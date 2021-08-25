---
title: Efecto de matriz de convolución
description: Use el efecto de matriz convolve para aplicar un kernel 2D arbitrario a una imagen. Puede usar este efecto para desenfocar, detectar bordes, relieves o mejorar una imagen.
ms.assetid: D9C23AC4-0090-4F16-AC59-B952FB616FA9
keywords:
- efecto de matriz convolve
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3b988e0bd48fece4d767fad29b63fe021c82d49d07dae5ab3f1b10b3f9794f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833384"
---
# <a name="convolve-matrix-effect"></a>Efecto de matriz de convolución

Use el efecto de matriz convolve para aplicar un kernel 2D arbitrario a una imagen. Puede usar este efecto para desenfocar, detectar bordes, relieves o mejorar una imagen.

El CLSID para este efecto es CLSID \_ D2D1ConvolveMatrix.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades de efecto](#effect-properties)
-   [Modos de escalado](#scale-modes)
-   [Modos de borde](#border-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestra la entrada y salida del efecto de matriz convolve con un kernel de 3 x 3.



| Antes                                                         |
|----------------------------------------------------------------|
| ![la imagen antes del efecto.](images/default-before.jpg)     |
| Después                                                          |
| ![la imagen después de la transformación.](images/6-convolvematrix.png) |



 


```C++
ComPtr<ID2D1Effect> convolveMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ConvolveMatrix, &convolveMatrixEffect);

convolveMatrixEffect->SetInput(0, bitmap);
float matrix[9] = {-1, -1, -1, -1, 9, -1, -1, -1, -1};
convolveMatrixEffect->SetValue(D2D1_CONVOLVEMATRIX_PROP_KERNEL_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(convolveMatrixEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propiedades de efecto



| Enumeración de nombre para mostrar e índice                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KernelUnitLength<br/> LONGITUD DE UNIDAD DE KERNEL DE \_ PROP CONVOLVEMATRIX D2D1 \_ \_ \_ \_<br/> | Tamaño de una unidad en el kernel. Las unidades están en (DIP/unidad de kernel), donde una unidad de kernel es el tamaño del elemento en el kernel de convolución. Un valor de 1 (unidad DIP/kernel) corresponde a un píxel de una imagen a 96 PPP.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                   |
| Scalemode<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ SCALE \_ MODE<br/>                 | Modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que varían en calidad y velocidad.<br/> El tipo es D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE.<br/> El valor predeterminado es D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ LINEAR.<br/>                                                                                                                                                                                                                     |
| KernelSizeX<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ SIZE \_ X<br/>           | Ancho de la matriz del kernel. Las unidades se especifican en unidades de kernel. El tipo es UINT32.<br/> El valor predeterminado es 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| KernelSizeY<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ KERNEL \_ SIZE \_ Y<br/>           | Alto de la matriz del kernel. Las unidades se especifican en unidades de kernel. El tipo es UINT32.<br/> El valor predeterminado es 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| KernelMatrix<br/> MATRIZ DE KERNEL DE PROP DE D2D1 \_ CONVOLVEMATRIX \_ \_ \_<br/>           | Matriz del kernel que se va a aplicar a la imagen. Los elementos del kernel no están enlazados y se especifican como floats.<br/> El primer conjunto de *números kernelSizeX* en FLOAT \[ \] corresponde a la primera fila del kernel. El segundo conjunto de *números kernelSizeX corresponde* a la segunda fila, y así sucesivamente hasta *las filas kernelSizeY.*<br/> El tipo es \[ \] FLOAT.<br/> El valor predeterminado es {0.0f, 0.0f, 0.0f, 0.0f, 1.0f, 0.0f, 0.0f, 0.0f, 0.0f}.<br/>                                                       |
| divisor<br/> DIVISOR DE PROP D2D1 \_ CONVOLVEMATRIX \_ \_<br/>                       | La matriz del kernel se aplica a un píxel y, a continuación, el resultado se divide por este valor. <br/> 0 se comporta como un valor de float epsilon.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1,0f.<br/>                                                                                                                                                                                                                                                                                                           |
| Sesgo<br/> SESGO DE PROP DE D2D1 \_ CONVOLVEMATRIX \_ \_<br/>                             | El efecto aplica la matriz del kernel, el divisor y, a continuación, se agrega el sesgo al resultado. El sesgo es sin enlazar y sin unidad. El tipo es FLOAT.<br/> El valor predeterminado es 0,0f.<br/>                                                                                                                                                                                                                                                                                                                              |
| KernelOffset<br/> DESPLAZAMIENTO DEL KERNEL DE PROP DE D2D1 \_ CONVOLVEMATRIX \_ \_ \_<br/>           | Desplaza el kernel de convolución de una posición centrada en el píxel de salida a una posición que especifique a la izquierda,derecha y arriba/abajo. El desplazamiento se define en unidades de kernel.<br/> Con algunos desplazamientos y tamaños de kernel, los ejemplos del kernel de convolución no se establecerán en un centro de imágenes de píxeles. Los valores de píxel del ejemplo de kernel se calculan mediante interpolación bilineal.<br/> El tipo es D2D1 \_ VECTOR \_ 2F.<br/> El valor predeterminado es {0.0f, 0.0f}.<br/>                                                          |
| PreserveAlpha<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ PRESERVE \_ ALPHA<br/>         | Especifica si el kernel de convolución se aplica al canal alfa o solo a los canales de color.<br/> Si establece esta opción en **TRUE,** el kernel de convolución solo se aplica a los canales de color.<br/> Si establece esta opción en **FALSE,** el kernel de convolución se aplica a todos los canales.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                               |
| BorderMode<br/> D2D1 \_ CONVOLVEMATRIX \_ PROP \_ BORDER \_ MODE<br/>               | Modo que se usa para calcular el borde de la imagen, de forma flexible o dura. Consulte [Modos de borde](https://www.bing.com/search?q=Border+modes) para obtener más información.<br/> El tipo es D2D1 \_ BORDER \_ MODE.<br/> El valor predeterminado es D2D1 \_ BORDER \_ MODE \_ SOFT.<br/>                                                                                                                                                                                                                                                                                     |
| ClampOutput<br/> SALIDA DE LA FIJACIÓN DE PROP DE D2D1 \_ CONVOLVEMATRIX \_ \_ \_<br/>             | Si el efecto fija los valores de color a entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto en el gráfico. El efecto fija los valores antes de multiplicar previamente el alfa .<br/> Si establece esta opción en TRUE, el efecto fijará los valores. Si establece esta opción en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no tienen una precisión lo suficientemente alta.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/> |



 

## <a name="scale-modes"></a>Modos de escalado



| Enumeración                                              | Descripción                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ NEAREST \_ NEIGHBOR     | Muestrea el punto más cercano y lo usa. Este modo usa menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ LINEAR                | Usa una muestra de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el modo vecino más cercano.                                                                              |
| MODO DE ESCALA DE CONVOLVEMATRIX D2D1 \_ \_ \_ \_ CÚBICA                 | Usa un kernel cúbica de 16 muestras para la interpolación. Este modo usa el mayor tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ MULTI \_ SAMPLE \_ LINEAR | Usa 4 muestras lineales dentro de un solo píxel para un suavizado de alias de borde bueno. Este modo es bueno para reducir verticalmente en pequeñas cantidades en imágenes con pocos píxeles.                                              |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ ANISOTROPIC           | Usa el filtrado anisotropico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ HIGH \_ QUALITY \_ CUBIC  | Usa un kernel cúbica de alta calidad de tamaño variable para realizar una escala previa a la baja de la imagen si la escala hacia abajo está implicada en la matriz de transformación. A continuación, usa el modo de interpolación cúbica para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ CONVOLVEMATRIX \_ SCALE \_ MODE \_ LINEAR.

 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MODO DE BORDE D2D1 \_ \_ \_ SOFT | El efecto aplica un panel a la imagen de entrada con píxeles de color negro transparente para las muestras fuera de los límites de entrada cuando se aplica el kernel de convolución. Esto crea un borde flexible para la imagen y, en el proceso, expande el mapa de bits de salida según el tamaño del kernel.<br/> |
| D2D1 \_ BORDER \_ MODE \_ HARD | El efecto extiende la imagen de entrada con una transformación de borde de tipo reflejo para muestras fuera de los límites de entrada. El tamaño del mapa de bits de salida es igual al tamaño del mapa de bits de entrada.<br/>                                                                       |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño de la salida del efecto depende del tamaño del kernel de convolución, el desplazamiento del kernel, la longitud de la unidad del kernel y la configuración del modo de borde.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio Windows aplicaciones de la \| Tienda\] |
| Servidor mínimo compatible | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio Windows aplicaciones de la \| Tienda\] |
| Header                   | d2d1effects.h                                                                      |
| Biblioteca                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

