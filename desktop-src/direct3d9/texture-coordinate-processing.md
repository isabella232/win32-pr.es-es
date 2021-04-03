---
description: En el diagrama siguiente se muestra la ruta de acceso tomada por las coordenadas de textura desde su origen, mediante el procesamiento y hasta el rasterizador.
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: Procesamiento de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a161d3675a5859702368a62719124aa029ee455
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104080046"
---
# <a name="texture-coordinate-processing-direct3d-9"></a>Procesamiento de coordenadas de textura (Direct3D 9)

En el diagrama siguiente se muestra la ruta de acceso tomada por las coordenadas de textura desde su origen, mediante el procesamiento y hasta el rasterizador.

![diagrama de la ruta de acceso para las coordenadas de textura de un origen al rasterizador](images/tex-processing.png)

Hay dos orígenes desde los que el sistema puede dibujar coordenadas de textura. En el caso de una fase de textura determinada, puede utilizar coordenadas de textura incluidas en el formato de vértice (D3DFVF \_ Tex1 a través de D3DFVF \_ TEX8), o puede usar coordenadas de textura generadas automáticamente por Direct3D. Para obtener más información sobre este último caso, consulte [coordenadas de textura generadas automáticamente (Direct3D 9)](automatically-generated-texture-coordinates.md). Si el \_ Estado de la fase de textura de D3DTSS TEXTURETRANSFORMFLAGS para la fase de textura actual se establece en D3DTTFF \_ Disable (el valor predeterminado), las coordenadas de entrada no se transforman. Si D3DTSS \_ TEXTURETRANSFORMFLAGS> está establecido en cualquier otro valor, la matriz de transformación para esa fase se aplica a las coordenadas de entrada.

El tipo enumerado [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) define los valores válidos para el \_ Estado D3DTSS TEXTURETRANSFORMFLAGS Texture-Stage. A excepción de la marca de \_ deshabilitación de D3DTTFF, que omite la transformación de coordenadas de textura, los valores definidos en esta enumeración configuran el número de coordenadas de salida que el sistema pasa al rasterizador. Las \_ marcas D3DTTFF COUNT1 a través de D3DTTFF \_ COUNT4 indican al sistema que pase uno, dos, tres o cuatro elementos de las coordenadas de salida al rasterizador.

La \_ marca proyectada D3DTTFF es especial: indica al sistema que las coordenadas de textura son para una textura proyectada. Combine la \_ marca proyectada D3DTTFF con otro miembro de [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) para indicar al rasterizador que divida todos los elementos por el último elemento antes de que tenga lugar la rasterización. Por ejemplo, cuando se usan explícitamente coordenadas de textura de tres elementos, o cuando la transformación da como resultado una coordenada de textura de tres elementos, se pueden combinar las \_ marcas proyectadas D3DTTFF COUNT3 y D3DTTFF \_ para que el rasterizador Divida los dos primeros elementos por el último, generando coordenadas de textura 2D necesarias para direccionar una textura 2D.

> [!Note]  
> Con la excepción de los mapas de entorno cúbico y las texturas de volumen, los rasterizadores no pueden direccionar texturas mediante coordenadas de textura con más de dos elementos. Si especifica más elementos de los que se pueden usar para direccionar la textura actual de esa fase, se omiten los elementos extraños. Esto también se aplica cuando se usan coordenadas de textura 2D para una textura 1D.

 

En los temas siguientes se incluye información adicional.

-   [Coordenadas de textura generadas automáticamente (Direct3D 9)](automatically-generated-texture-coordinates.md)
-   [Transformaciones de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md)
-   [Efectos especiales (Direct3D 9)](special-effects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Coordenadas de textura](texture-coordinates.md)
</dt> </dl>

 

 
