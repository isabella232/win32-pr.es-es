---
description: Cuando el sistema realiza el sombreado de vértices, aplica cálculos de cálculo de cálculo en cada vértice de un polígono y, a continuación, interpola los resultados a través de la cara del polígono durante la rasterización.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Vértice de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76196ba0489ac58529bcb5c0500a269c8ee27b87040ec96f64ef228377dc8abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068985"
---
# <a name="vertex-fog-direct3d-9"></a>Vértice de vértice (Direct3D 9)

Cuando el sistema realiza el sombreado de vértices, aplica cálculos de cálculo de cálculo en cada vértice de un polígono y, a continuación, interpola los resultados a través de la cara del polígono durante la rasterización. Los efectos de vértices se calculan mediante el motor de iluminación y transformación de Direct3D. Para obtener más información, vea [Parámetros de Parámetros de parámetros de parámetros de Parámetros de parámetros (Direct3D 9)](fog-parameters.md).

Si la aplicación no usa Direct3D para la transformación y la iluminación, la aplicación debe realizar cálculos de cálculos de cálculo. En este caso, coloque el factor de curva que se calcula en el componente alfa del color especular para cada vértice. Puede usar las fórmulas que quiera: basadas en intervalos, volumétricas o de otro tipo. Direct3D usa el factor de depósito proporcionado para interpolar a través de la cara de cada polígono. Las aplicaciones que realizan su propia transformación e iluminación también deben realizar sus propios cálculos de vértices. Como resultado, esta aplicación solo necesita habilitar la mezcla de mezcla y establecer el color de fusión a través de los estados de representación asociados, como se describe en [Blending (Direct3D 9)](fog-blending.md) y Color de fusión [(Direct3D 9).](fog-color.md)

> [!Note]  
> Cuando se usa un sombreador de vértices, debe usar vértices de vértice. Esto se logra mediante el sombreador de vértices para escribir la intensidad de vértice en el registro de oFog. Una vez completado el sombreador de píxeles, los datos de oFog se usan para interpolar linealmente con el color de color blanco. Esta intensidad no está disponible en un sombreador de píxeles.

 

## <a name="range-based-fog"></a>Range-Based DescRange-Based

> [!Note]  
> Direct3D usa cálculos de cálculos de cálculo basados en intervalos solo cuando se usa el vértice con el motor de iluminación y transformación de Direct3D. Esto se debe a que el pixel se implementa en el controlador del dispositivo y actualmente no existe hardware para admitir el rango basado en píxeles. Si la aplicación realiza su propia transformación e iluminación, debe realizar sus propios cálculos de cálculo, basados en intervalos o de otro modo.

 

En ocasiones, el uso de los artefactos gráficos puede introducir artefactos gráficos que hacen que los objetos se combinen con el color de la paleta de maneras no inocuas. Por ejemplo, imagine una escena en la que hay dos objetos visibles: uno lo suficientemente lejano como para verse afectado por el desván y el otro lo suficientemente cerca como para no verse afectado. Si el área de visualización gira en su lugar, pueden cambiar los efectos aparentes de efecto, incluso si los objetos están estacionados. En el diagrama siguiente se muestra una vista de arriba abajo de este tipo de situación.

![diagrama de dos puntos de vista y cómo afectan a los efectos de dos objetos](images/artifog.png)

El sonido basado en intervalos es otra manera más precisa de determinar los efectos de las nubes. En intervalos basados en intervalos, Direct3D usa la distancia real desde el punto de vista hasta un vértice para sus cálculos de cálculos de cálculo. Direct3D aumenta el efecto de la flecha a medida que aumenta la distancia entre los dos puntos, en lugar de la profundidad del vértice dentro de la escena, lo que evita artefactos de rotación.

Si el dispositivo actual admite intervalos, establecerá el valor D3DPRASTERCAPS RANGE en el miembro \_ RasterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) al llamar al método [**IDirect3DDevice9::GetDeviceCaps.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) Para habilitar el intervalo basado en intervalos, establezca el estado de representación D3DRS \_ RANGEFOGENABLE en **TRUE.**

Direct3D calcula la frecuencia basada en intervalos durante la transformación y la iluminación. Las aplicaciones que no usan el motor de iluminación y transformación de Direct3D también deben realizar sus propios cálculos de vértices. En este caso, proporcione el factor de oscilación basado en intervalo en el componente alfa del componente especular para cada vértice.

## <a name="using-vertex-fog"></a>Uso de vértices de vértice

Siga estos pasos para habilitar vértices en la aplicación.

1.  Habilite la mezcla de mezcla estableciendo \_ D3DRSEVEENABLE en **TRUE.**
2.  Establezca el color de color de color azul en el estado de representación \_ D3DRSCOLORCOLOR.
3.  Elija la fórmula de fórmula deseada estableciendo el estado de representación D3DRSOGVERTEXMODE en un miembro del tipo \_ enumerado [**D3DFOGMODE.**](./d3dfogmode.md)
4.  Establezca los parámetros de los estados de representación según sea necesario para la fórmula de matriz seleccionada.

En el ejemplo siguiente, escrito en C++, se muestra el aspecto de estos pasos en el código.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupVertexFog(DWORD Color, DWORD Mode, BOOL UseRange, FLOAT Density)
{
    float Start = 0.5f,    // Linear fog distances
          End   = 0.8f;
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if(D3DFOG_LINEAR == Mode)
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGVERTEXMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }

    // Enable range-based fog if desired (only supported for
    //   vertex fog). For this example, it is assumed that UseRange
    //   is set to a nonzero value only if the driver exposes the 
    //   D3DPRASTERCAPS_FOGRANGE capability.
    // Note: This is slightly more performance intensive
    //   than non-range-based fog.
    if(UseRange)
        g_pDevice->SetRenderState(D3DRS_RANGEFOGENABLE, TRUE);
}
```



Algunos parámetros de nodo son necesarios como valores de punto flotante, aunque el método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) solo acepta valores DWORD en el segundo parámetro. Este ejemplo proporciona correctamente los valores de punto flotante a estos métodos sin traducción de datos al convertir las direcciones de las variables de punto flotante como punteros DWORD y, a continuación, desreferenciarlos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de vaselina](fog-types.md)
</dt> </dl>

 

 
