---
description: Los dispositivos Direct3D pueden transformar las coordenadas de textura de los vértices aplicando una matriz de 4x4.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Transformaciones de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f45b8107f609348ae2367b1171ae7913797f4558
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358870"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Transformaciones de coordenadas de textura (Direct3D 9)

Los dispositivos Direct3D pueden transformar las coordenadas de textura de los vértices aplicando una matriz de 4x4. El sistema aplica transformaciones a las coordenadas de textura de la misma manera que la geometría. Cualquier transformación (escala, rotación, traducción, proyección, cizalla o cualquier combinación de estas) se puede realizar con una matriz de 4x4.

> [!Note]  
> Direct3D no modifica los vértices transformados ni encendidos. Como resultado, una aplicación que usa vértices transformados y encendidos no puede usar Direct3D para transformar las coordenadas de textura de los vértices.

 

Los dispositivos que admiten operaciones de iluminación y transformación acelerada por hardware (T&L XSL Device) también aceleran la transformación de las coordenadas de textura. Cuando la aceleración de hardware de transformaciones no está disponible, las optimizaciones específicas de la plataforma en la canalización de geometría de Direct3D se aplican a las transformaciones de coordenadas de textura.

Las transformaciones de coordenadas de textura son útiles para producir efectos especiales, a la vez que evitan la necesidad de modificar directamente las coordenadas de textura de la geometría. Puede usar matrices simples de traslación o rotación para animar texturas en un objeto, o bien puede transformar las coordenadas de textura generadas automáticamente por Direct3D para simplificar y quizás acelerar los efectos avanzados, como las texturas proyectadas y la asignación de luz dinámica. Además, puede usar transformaciones de coordenadas de textura para reutilizar un único conjunto de coordenadas de textura para varios propósitos, en varias fases de textura.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Establecer y recuperar transformaciones de coordenadas de textura

Al igual que las matrices que la aplicación usa para la geometría, puede establecer y recuperar transformaciones de coordenadas de textura mediante una llamada a los métodos [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) e [**IDirect3DDevice9::GetTransform.**](/windows/desktop/api) Estos métodos aceptan los miembros TEXTURE0 de D3DTS a D3DTS TEXTURE7 del tipo enumerado \_ \_ [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) para identificar las matrices de transformación de las fases de textura 0 a 7, respectivamente.

El código siguiente establece una matriz que se aplicará a las coordenadas de textura de la fase de textura 0.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Habilitar transformaciones de coordenadas de textura

El estado de la fase de textura TEXTURETRANSFORMFLAGS de D3DTSS controla la aplicación de transformaciones de coordenadas \_ de textura. Los valores para este estado de fase de textura se definen mediante el tipo enumerado [**D3DTEXTURETRANSFORMFLAGS.**](./d3dtexturetransformflags.md)

Las transformaciones de coordenadas de textura se deshabilitan cuando TEXTURETRANSFORMFLAGS de D3DTSS se establece \_ en D3DTTFF \_ DISABLE (el valor predeterminado). Suponiendo que las transformaciones de coordenadas de textura se habilitaron para la fase 0, el código siguiente las deshabilita.


```
// For this example, assume the d3dDevice variable contains a 
// valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_DISABLE );
```



Los demás valores definidos en [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) se usan para habilitar transformaciones de coordenadas de textura y para controlar cuántos elementos de coordenadas de textura resultantes se pasan al rasterizador. Por ejemplo, tome el código siguiente.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT2 );
```



El valor D3DTTFF COUNT2 indica al sistema que aplique la matriz de transformación establecida para la fase de textura 0 y, a continuación, pase los dos primeros elementos de las coordenadas de textura modificadas al \_ rasterizador.

La marca de transformación de textura D3DTTFF \_ PROJECTED indica las coordenadas de una textura proyectada. Cuando se especifica esta marca, el rasterizador divide los elementos pasados por el último elemento. Tome el código siguiente, por ejemplo.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



En este ejemplo se informa al sistema de que pase tres elementos de coordenadas de textura al rasterizador. El rasterizador divide los dos primeros elementos por el tercero, lo que genera las coordenadas de textura 2D necesarias para abordar la textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procesamiento de coordenadas de textura](texture-coordinate-processing.md)
</dt> </dl>

 

 
