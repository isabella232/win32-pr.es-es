---
description: Los dispositivos Direct3D pueden transformar las coordenadas de textura de los vértices aplicando una matriz de 4x4.
ms.assetid: f36439de-e37a-457c-9485-a435847eb01e
title: Transformaciones de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755af38c6c58fc2f19297b056e3e9f35ce2559a6a7a2d52e8a23c94f93f4fbaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984795"
---
# <a name="texture-coordinate-transformations-direct3d-9"></a>Transformaciones de coordenadas de textura (Direct3D 9)

Los dispositivos Direct3D pueden transformar las coordenadas de textura de los vértices aplicando una matriz de 4x4. El sistema aplica transformaciones a las coordenadas de textura de la misma manera que la geometría. Cualquier transformación (escala, rotación, traducción, proyección, cizalla o cualquier combinación de estas) se puede realizar con una matriz de 4x4.

> [!Note]  
> Direct3D no modifica los vértices transformados ni encendidos. Como resultado, una aplicación que usa vértices transformados e encendidos no puede usar Direct3D para transformar las coordenadas de textura de los vértices.

 

Los dispositivos que admiten operaciones de iluminación y transformación acelerada por hardware (T&L XSL Device) también aceleran la transformación de las coordenadas de textura. Cuando la aceleración de hardware de transformaciones no está disponible, las optimizaciones específicas de la plataforma en la canalización de geometría de Direct3D se aplican a las transformaciones de coordenadas de textura.

Las transformaciones de coordenadas de textura son útiles para producir efectos especiales, a la vez que evitan la necesidad de modificar directamente las coordenadas de textura de la geometría. Puede usar matrices de traslación o rotación simples para animar texturas en un objeto, o bien puede transformar las coordenadas de textura generadas automáticamente por Direct3D para simplificar y quizás acelerar los efectos avanzados, como las texturas proyectadas y la asignación de luz dinámica. Además, puede usar transformaciones de coordenadas de textura para reutilizar un único conjunto de coordenadas de textura para varios propósitos, en varias fases de textura.

## <a name="setting-and-retrieving-texture-coordinate-transformations"></a>Establecer y recuperar transformaciones de coordenadas de textura

Al igual que las matrices que la aplicación usa para geometry, puede establecer y recuperar transformaciones de coordenadas de textura mediante una llamada a los métodos [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) e [**IDirect3DDevice9::GetTransform.**](/windows/desktop/api) Estos métodos aceptan los miembros TEXTURE0 de D3DTS a D3DTS TEXTURE7 del tipo enumerado \_ \_ [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) para identificar las matrices de transformación para las fases de textura 0 a 7, respectivamente.

El código siguiente establece una matriz que se aplicará a las coordenadas de textura para la fase de textura 0.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

D3DMATRIX matTrans = D3DXMatrixIdentity( NULL );

// Set up the matrix for the desired transformation.
d3dDevice->SetTransform( D3DTS_TEXTURE0, &matTrans );
```



## <a name="enabling-texture-coordinate-transformations"></a>Habilitar transformaciones de coordenadas de textura

El estado de la fase de textura TEXTURETRANSFORMFLAGS de D3DTSS controla la aplicación de transformaciones de coordenadas \_ de textura. El tipo enumerado [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) define los valores para este estado de fase de textura.

Las transformaciones de coordenadas de textura se deshabilitan cuando D3DTSS TEXTURETRANSFORMFLAGS se establece \_ en D3DTTFF \_ DISABLE (el valor predeterminado). Suponiendo que las transformaciones de coordenadas de textura se habilitaron para la fase 0, el código siguiente las deshabilita.


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



El valor D3DTTFF COUNT2 indica al sistema que aplique el conjunto de matrices de transformación para la fase de textura 0 y, a continuación, pase los dos primeros elementos de las coordenadas de textura modificadas al \_ rasterizador.

La marca de transformación de textura D3DTTFF \_ PROJECTED indica las coordenadas de una textura proyectada. Cuando se especifica esta marca, el rasterizador divide los elementos pasados por el último elemento. Tome el código siguiente, por ejemplo.


```
// For this example, assume the d3dDevice variable contains a 
//   valid pointer to an IDirect3DDevice9 interface.

d3dDevice->SetTextureStageState( 0, D3DTSS_TEXTURETRANSFORMFLAGS, 
                                 D3DTTFF_COUNT3 | D3DTTFF_PROJECTED );
```



En este ejemplo se informa al sistema de que pase tres elementos de coordenadas de textura al rasterizador. El rasterizador divide los dos primeros elementos por el tercero, generando las coordenadas de textura 2D necesarias para abordar la textura.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procesamiento de coordenadas de textura](texture-coordinate-processing.md)
</dt> </dl>

 

 
