---
description: En el diagrama siguiente se muestra la ruta de acceso tomada por las coordenadas de textura desde su origen, a través del procesamiento y al rasterizador.
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: Procesamiento de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5a002e7171f97ab60c0af3cd5e8228cb8222ba70b8e718f2d93c28cebf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044233"
---
# <a name="texture-coordinate-processing-direct3d-9"></a>Procesamiento de coordenadas de textura (Direct3D 9)

En el diagrama siguiente se muestra la ruta de acceso tomada por las coordenadas de textura desde su origen, a través del procesamiento y al rasterizador.

![diagrama de la ruta de acceso para las coordenadas de textura de un origen al rasterizador](images/tex-processing.png)

Hay dos orígenes a partir de los cuales el sistema puede dibujar coordenadas de textura. Para una fase de textura determinada, puede usar coordenadas de textura incluidas en el formato de vértice (D3DFVF TEX1 a D3DFVF TEXAS8), o bien puede usar coordenadas de textura generadas automáticamente por \_ \_ Direct3D. Para obtener más información sobre este último caso, vea Coordenadas de textura [generadas automáticamente (Direct3D 9).](automatically-generated-texture-coordinates.md) Si el estado de la fase de textura TEXTURETRANSFORMFLAGS de D3DTSS para la fase de textura actual se establece en \_ D3DTTFF DISABLE (la configuración predeterminada), las coordenadas de entrada no \_ se transforman. Si D3DTSS TEXTURETRANSFORMFLAGS> establece en cualquier otro valor, la matriz de transformación para esa fase se aplica a las \_ coordenadas de entrada.

El [**tipo enumerado D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) define valores válidos para el estado de la fase de textura DE D3DTSS \_ TEXTURETRANSFORMFLAGS. A excepción de la marca DISABLE de D3DTTFF, que omite la transformación de coordenadas de textura, los valores definidos en esta enumeración configuran el número de coordenadas de salida que el sistema pasa al \_ rasterizador. Las marcas D3DTTFF COUNT1 a D3DTTFF COUNT4 le piden al sistema que pase uno, dos, tres o cuatro elementos de las coordenadas de salida al \_ \_ rasterizador.

La marca D3DTTFF PROJECTED es especial: indica al sistema que las coordenadas de textura \_ son para una textura proyectada. Combine la marca D3DTTFF PROJECTED con otro miembro de \_ [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) para indicar al rasterizador que divida todos los elementos por el último elemento antes de que se lleve a cabo la rasterización. Por ejemplo, cuando se usan explícitamente coordenadas de textura de tres elementos o cuando la transformación da como resultado una coordenada de textura de tres elementos, puede combinar las marcas D3DTTFF COUNT3 y D3DTTFF PROJECTED para hacer que el rasterizador divida los dos primeros elementos por el último, generando coordenadas de textura 2D necesarias para abordar una textura \_ \_ 2D.

> [!Note]  
> A excepción de los mapas de entorno cúbica y las texturas de volumen, los rasterizadores no pueden abordar las texturas mediante coordenadas de textura con más de dos elementos. Si especifica más elementos de los que se pueden usar para abordar la textura actual de esa fase, se omiten los elementos extraneous. Esto también se aplica cuando se usan coordenadas de textura 2D para una textura 1D.

 

En los temas siguientes se incluye información adicional.

-   [Coordenadas de textura generadas automáticamente (Direct3D 9)](automatically-generated-texture-coordinates.md)
-   [Transformaciones de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md)
-   [Efectos especiales (Direct3D 9)](special-effects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Coordenadas de textura](texture-coordinates.md)
</dt> </dl>

 

 
