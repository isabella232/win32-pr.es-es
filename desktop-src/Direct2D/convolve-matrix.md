---
title: Efecto de matriz de convolución
description: Use el efecto de matriz de con@ para aplicar un kernel 2D arbitrario a una imagen. Puede usar este efecto para desenfocar, detectar bordes, grabar o enfocar una imagen.
ms.assetid: D9C23AC4-0090-4F16-AC59-B952FB616FA9
keywords:
- con@ (efecto de matriz)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27951f5b9145dc46188e6b3112892d1a61856236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104568857"
---
# <a name="convolve-matrix-effect"></a>Efecto de matriz de convolución

Use el efecto de matriz de con@ para aplicar un kernel 2D arbitrario a una imagen. Puede usar este efecto para desenfocar, detectar bordes, grabar o enfocar una imagen.

El CLSID para este efecto es CLSID \_ D2D1ConvolveMatrix.

-   [Imagen de ejemplo](#example-image)
-   [Propiedades del efecto](#effect-properties)
-   [Modos de escala](#scale-modes)
-   [Modos de borde](#border-modes)
-   [Mapa de bits de salida](#output-bitmap)
-   [Requisitos](#requirements)
-   [Temas relacionados](#related-topics)

## <a name="example-image"></a>Imagen de ejemplo

En el ejemplo siguiente se muestra la entrada y la salida del efecto de la matriz de configurary con un kernel 3 x 3.



| Antes                                                         |
|----------------------------------------------------------------|
| ![imagen anterior al efecto.](images/default-before.jpg)     |
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



## <a name="effect-properties"></a>Propiedades del efecto



| Enumeración de índice y nombre para mostrar                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KernelUnitLength<br/> Longitud de la \_ unidad de kernel de prop D2D1 CONVOLVEMATRIX \_ \_ \_ \_<br/> | Tamaño de una unidad en el kernel. Las unidades están en (DIP/unidad de kernel), donde una unidad de kernel es el tamaño del elemento en el kernel de circunvolución. Un valor de 1 (DIP/kernel Unit) corresponde a un píxel de una imagen a 96 ppp.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                   |
| ModoDeLaEscala<br/> \_Modo de \_ \_ escalado de propiedades \_ de D2D1 CONVOLVEMATRIX<br/>                 | El modo de interpolación que el efecto usa para escalar la imagen a la longitud de unidad de kernel correspondiente. Hay seis modos de escala que abarcan la calidad y la velocidad.<br/> El tipo es D2D1 \_ CONVOLVEMATRIX \_ Scale \_ mode.<br/> El valor predeterminado es D2D1 \_ CONVOLVEMATRIX en \_ modo de escala \_ \_ lineal.<br/>                                                                                                                                                                                                                     |
| KernelSizeX<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_ kernel \_ size \_ X<br/>           | Ancho de la matriz del kernel. Las unidades se especifican en unidades de kernel. El tipo es UINT32.<br/> El valor predeterminado es 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                        |
| KernelSizeY<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_ kernel \_ size \_ Y<br/>           | Alto de la matriz del kernel. Las unidades se especifican en unidades de kernel. El tipo es UINT32.<br/> El valor predeterminado es 3.<br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| KernelMatrix<br/> \_Matriz de \_ kernel de prop \_ \_ de D2D1 CONVOLVEMATRIX<br/>           | Matriz de kernel que se va a aplicar a la imagen. Los elementos de kernel no están enlazados y se especifican como flotantes.<br/> El primer conjunto de números de *KernelSizeX* en el Float \[ \] corresponde a la primera fila del kernel. El segundo conjunto de números de *KernelSizeX* se corresponde con la segunda fila y así sucesivamente hasta *KernelSizeY* filas.<br/> El tipo es FLOAT \[ \] .<br/> El valor predeterminado es {0.0 f, 0.0 f, 0.0 f, 0.0 f, 1,0 f, 0.0 f, 0.0 f, 0.0 f, 0.0 f}.<br/>                                                       |
| divisor<br/> Divisor de propiedades de D2D1 \_ CONVOLVEMATRIX \_ \_<br/>                       | La matriz de kernel se aplica a un píxel y, a continuación, el resultado se divide por este valor. <br/> 0 se comporta como un valor de Float épsilon.<br/> El tipo es FLOAT.<br/> El valor predeterminado es 1.0 f.<br/>                                                                                                                                                                                                                                                                                                           |
| Sesgo<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_<br/>                             | El efecto aplica la matriz de kernel, el divisor y, a continuación, la diferencia se agrega al resultado. El sesgo es ilimitado y sin unidades. El tipo es FLOAT.<br/> El valor predeterminado es 0.0 f.<br/>                                                                                                                                                                                                                                                                                                                              |
| KernelOffset<br/> \_ \_ \_ Desplazamiento del kernel de D2D1 CONVOLVEMATRIX prop \_<br/>           | Desplaza el kernel de circunvolución desde una posición centrada en el píxel de salida hasta la posición que especifique izquierda/derecha y hacia arriba o hacia abajo. El desplazamiento se define en unidades de kernel.<br/> Con algunos desplazamientos y tamaños de kernel, los ejemplos de kernel de circunvolución no se colocan en un centro de imágenes de píxeles. Los valores de píxeles para el ejemplo de kernel se calculan mediante la interpolación bilineal.<br/> El tipo es D2D1 \_ Vector \_ 2F.<br/> El valor predeterminado es {0.0 f, 0.0 f}.<br/>                                                          |
| PreserveAlpha<br/> D2D1 \_ CONVOLVEMATRIX \_ prop \_ conservar \_ alfa<br/>         | Especifica si el kernel de circunvolución se aplica al canal alfa o solo a los canales de color.<br/> Si se establece en **true** , el kernel de circunvolución solo se aplica a los canales de color.<br/> Si se establece en **false** , el kernel de circunvolución se aplica a todos los canales.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/>                                                                                                                                               |
| BorderMode<br/> D2D1 \_ CONVOLVEMATRIX \_ \_ modo de borde \_ de la Prop<br/>               | El modo que se usa para calcular el borde de la imagen, es decir, es flexible o difícil. Vea [modos de borde](https://www.bing.com/search?q=Border+modes) para obtener más información.<br/> El tipo es D2D1 \_ Border \_ mode.<br/> El valor predeterminado es D2D1 \_ Border \_ Mode \_ .<br/>                                                                                                                                                                                                                                                                                     |
| ClampOutput<br/> Salida de la abrazadera de D2D1 \_ CONVOLVEMATRIX \_ \_ \_<br/>             | Si el efecto fija los valores de color entre 0 y 1 antes de que el efecto pase los valores al siguiente efecto del gráfico. El efecto fija los valores antes de que premultiplique el alfa.<br/> Si establece este valor en TRUE, el efecto fijará los valores. Si se establece en FALSE, el efecto no fijará los valores de color, pero otros efectos y la superficie de salida pueden fijar los valores si no son de precisión lo suficientemente alta.<br/> El tipo es BOOL.<br/> El valor predeterminado es FALSE.<br/> |



 

## <a name="scale-modes"></a>Modos de escala



| Enumeración                                              | Descripción                                                                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ el \_ modo de escalado CONVOLVEMATRIX \_ \_ más cercano \_     | Muestrea el punto único más cercano y lo usa. Este modo utiliza menos tiempo de procesamiento, pero genera la imagen de menor calidad.                                                                           |
| \_Modo de \_ escala \_ \_ lineal de D2D1 CONVOLVEMATRIX                | Utiliza un ejemplo de cuatro puntos y una interpolación lineal. Este modo genera una imagen de mayor calidad que el modo vecino más próximo.                                                                              |
| D2D1 \_ \_ modo de escala CONVOLVEMATRIX \_ \_ cúbico                 | Usa un kernel cúbico de ejemplo 16 para la interpolación. Este modo utiliza la mayor parte del tiempo de procesamiento, pero genera una imagen de mayor calidad.                                                                        |
| D2D1 \_ CONVOLVEMATRIX en \_ modo de escala lineal de \_ \_ varios \_ ejemplos \_ | Usa 4 muestras lineales dentro de un solo píxel para el suavizado de contorno adecuado. Este modo es adecuado para reducir verticalmente en pequeñas cantidades de imágenes con pocos píxeles.                                              |
| \_Modo de \_ escala D2D1 CONVOLVEMATRIX \_ \_           | Utiliza el filtrado anisotrópico para muestrear un patrón según la forma transformada del mapa de bits.                                                                                                     |
| D2D1 \_ CONVOLVEMATRIX, \_ modo de escalado de \_ \_ alta \_ calidad \_ cúbico  | Usa un kernel cúbico de alta calidad de tamaño variable para realizar una downscale previa de la imagen si downscaling está implicado en la matriz de transformación. A continuación, usa el modo de interpolación cúbico para la salida final. |



 

> [!Note]  
> Si no selecciona un modo, el efecto tiene como valor predeterminado D2D1 \_ CONVOLVEMATRIX \_ modo de escala \_ \_ lineal.

 

## <a name="border-modes"></a>Modos de borde



| Nombre                     | Descripción                                                                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ modo de borde \_ \_ flexible | El efecto rellena la imagen de entrada con píxeles negros transparentes para muestras fuera de los límites de entrada cuando aplica el kernel de circunvolución. Esto crea un borde flexible para la imagen y, en el proceso, expande el mapa de bits de salida por el tamaño del kernel.<br/> |
| D2D1 \_ del \_ modo de borde \_ | El efecto extiende la imagen de entrada con una transformación de borde de tipo de reflejo para las muestras fuera de los límites de entrada. El tamaño del mapa de bits de salida es igual al tamaño del mapa de bits de entrada.<br/>                                                                       |



 

## <a name="output-bitmap"></a>Mapa de bits de salida

El tamaño del resultado del efecto depende del tamaño del kernel de circunvolución, el desplazamiento del kernel, la longitud de la unidad del kernel y la configuración del modo de borde.

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

 

