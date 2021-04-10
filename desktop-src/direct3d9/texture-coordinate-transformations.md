---
description: Los dispositivos Direct3D pueden transformar las coordenadas de textura de los vértices aplicando una matriz 4x4.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Transformaciones de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45b8107f609348ae2367b1171ae7913797f4558
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152318"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Transformaciones de coordenadas de textura (Direct3D 9)

Los dispositivos Direct3D pueden transformar las coordenadas de textura de los vértices aplicando una matriz 4x4. El sistema aplica las transformaciones a las coordenadas de textura de la misma manera que la geometría. Cualquier transformación (escala, rotación, traslación, proyección, cizalla o cualquier combinación de estos) se puede realizar con una matriz 4x4.

> [!Note]  
> Direct3D no modifica los vértices transformados y iluminados. Como resultado, una aplicación que use vértices transformados y encendidos no puede usar Direct3D para transformar las coordenadas de textura de los vértices.

 

Los dispositivos que admiten operaciones de transformación y luz aceleradas por hardware (dispositivo HAL T&L) también aceleran la transformación de coordenadas de textura. Cuando no está disponible la aceleración de hardware de las transformaciones, las optimizaciones específicas de la plataforma de la canalización de geometría de Direct3D se aplican a las transformaciones de coordenadas de textura.

Las transformaciones de coordenadas de textura son útiles para producir efectos especiales, a la vez que evitan la necesidad de modificar directamente las coordenadas de textura de la geometría. Puede usar matrices simples de traslación o rotación para animar las texturas de un objeto, o puede transformar las coordenadas de textura generadas automáticamente por Direct3D para simplificar y quizás acelerar los efectos avanzados, como las texturas proyectadas y la asignación dinámica de luz. Además, puede usar transformaciones de coordenadas de textura para reutilizar un único conjunto de coordenadas de textura para varios propósitos, en varias fases de textura.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Establecimiento y recuperación de transformaciones de coordenadas de textura

Al igual que las matrices que usa la aplicación para la geometría, se establecen y recuperan las transformaciones de coordenadas de textura mediante una llamada a los métodos [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) y [**IDirect3DDevice9:: GetTransform**](/windows/desktop/api) . Estos métodos aceptan D3DTS \_ TEXTURE0 a través \_ de D3DTS TEXTURE7 miembros del tipo enumerado [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) para identificar las matrices de transformación para las fases de textura de 0 a 7, respectivamente.

El código siguiente establece una matriz que se aplica a las coordenadas de textura para la fase de textura 0.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Habilitar transformaciones de coordenadas de textura

El \_ Estado de la fase de textura de D3DTSS TEXTURETRANSFORMFLAGS controla la aplicación de transformaciones de coordenadas de textura. Los valores de este estado de fase de textura se definen mediante el tipo enumerado [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) .

Las transformaciones de coordenadas de textura se deshabilitan cuando D3DTSS \_ TEXTURETRANSFORMFLAGS se establece en D3DTTFF \_ Disable (el valor predeterminado). Suponiendo que las transformaciones de coordenadas de textura se habilitaron para la fase 0, el código siguiente las deshabilita.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Los demás valores definidos en [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) se usan para habilitar las transformaciones de coordenadas de textura y para controlar cuántos elementos de coordenadas de textura resultantes se pasan al rasterizador. Por ejemplo, tome el código siguiente.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



El \_ valor de COUNT2 de D3DTTFF indica al sistema que aplique el conjunto de matrices de transformación para la fase de textura 0 y, a continuación, pase los dos primeros elementos de las coordenadas de textura modificadas al rasterizador.

La \_ marca de transformación de textura proyectada D3DTTFF indica las coordenadas de una textura proyectada. Cuando se especifica esta marca, el rasterizador divide los elementos pasados en el último elemento. Tome el código siguiente, por ejemplo.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



Este ejemplo informa al sistema para que pase tres elementos de coordenadas de textura al rasterizador. El rasterizador divide los dos primeros elementos por el tercero, lo que genera las coordenadas de textura 2D necesarias para direccionar la textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procesamiento de coordenadas de textura](texture-coordinate-processing.md)
</dt> </dl>

 

 
