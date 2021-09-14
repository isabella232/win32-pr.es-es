---
description: En el diagrama siguiente se muestra la ruta de acceso tomada por las coordenadas de textura desde su origen, a través del procesamiento y al rasterizador.
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: Procesamiento de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a161d3675a5859702368a62719124aa029ee455
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358871"
---
# <a name="texture-coordinate-processing-direct3d-9"></a>Procesamiento de coordenadas de textura (Direct3D 9)

En el diagrama siguiente se muestra la ruta de acceso tomada por las coordenadas de textura desde su origen, a través del procesamiento y al rasterizador.

![diagrama de la ruta de acceso para las coordenadas de textura de un origen al rasterizador](images/tex-processing.png)

Hay dos orígenes a partir de los cuales el sistema puede dibujar coordenadas de textura. Para una fase de textura determinada, puede usar coordenadas de textura incluidas en el formato de vértice (D3DFVF TEX1 a D3DFVF TEX8), o puede usar coordenadas de textura generadas automáticamente por \_ \_ Direct3D. Para obtener más información sobre este último caso, vea Coordenadas de textura generadas [automáticamente (Direct3D 9).](automatically-generated-texture-coordinates.md) Si el estado de la fase de textura TEXTURETRANSFORMFLAGS de D3DTSS para la fase de textura actual se establece en \_ D3DTTFF DISABLE (la configuración predeterminada), las coordenadas de entrada no \_ se transforman. Si D3DTSS TEXTURETRANSFORMFLAGS> se establece en cualquier otro valor, la matriz de transformación de esa fase se aplica a las \_ coordenadas de entrada.

El [**tipo enumerado D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) define valores válidos para el estado de fase de textura TEXTURETRANSFORMFLAGS de D3DTSS. \_ A excepción de la marca DISABLE de D3DTTFF, que omite la transformación de coordenadas de textura, los valores definidos en esta enumeración configuran el número de coordenadas de salida que el sistema pasa al \_ rasterizador. Las marcas D3DTTFF COUNT1 a D3DTTFF COUNT4 indica al sistema que pase uno, dos, tres o cuatro elementos de las coordenadas de salida al \_ \_ rasterizador.

La marca PROJECTED de D3DTTFF es especial: indica al sistema que las coordenadas de textura son \_ para una textura proyectada. Combine la marca D3DTTFF PROJECTED con otro miembro de \_ [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) para indicar al rasterizador que divida todos los elementos por el último elemento antes de que se lleve a cabo la rasterización. Por ejemplo, cuando se usan explícitamente coordenadas de textura de tres elementos o cuando la transformación da como resultado una coordenada de textura de tres elementos, puede combinar las marcas D3DTTFF COUNT3 y D3DTTFF PROJECTED para hacer que el rasterizador divida los dos primeros elementos por el último, generando las coordenadas de textura 2D necesarias para abordar una textura \_ \_ 2D.

> [!Note]  
> A excepción de los mapas de entorno cúbica y las texturas de volumen, los rasterizadores no pueden dirigir las texturas mediante coordenadas de textura con más de dos elementos. Si especifica más elementos de los que se pueden usar para abordar la textura actual de esa fase, se omiten los elementos extraneous. Esto también se aplica cuando se usan coordenadas de textura 2D para una textura 1D.

 

En los temas siguientes se incluye información adicional.

-   [Coordenadas de textura generadas automáticamente (Direct3D 9)](automatically-generated-texture-coordinates.md)
-   [Transformaciones de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md)
-   [Efectos especiales (Direct3D 9)](special-effects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Coordenadas de textura](texture-coordinates.md)
</dt> </dl>

 

 
