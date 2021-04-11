---
description: Cuando el sistema realiza la luneta térmica de los vértices, aplica los cálculos de niebla en cada vértice de un polígono y, a continuación, interpola los resultados a lo largo de la superficie del polígono durante la rasterización.
ms.assetid: 76989eb3-cd95-4dfc-ba0f-7563860b531c
title: Niebla de vértices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35cd880bda7ebffd36bd95bec5f8565e104eaa15
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151941"
---
# <a name="vertex-fog-direct3d-9"></a>Niebla de vértices (Direct3D 9)

Cuando el sistema realiza la luneta térmica de los vértices, aplica los cálculos de niebla en cada vértice de un polígono y, a continuación, interpola los resultados a lo largo de la superficie del polígono durante la rasterización. Los efectos de la niebla de vértice se calculan mediante el motor de luz y transformación de Direct3D. Para obtener más información, vea [parámetros de niebla (Direct3D 9)](fog-parameters.md).

Si la aplicación no usa Direct3D para la transformación y la iluminación, la aplicación debe realizar cálculos de niebla. En este caso, coloque el factor de niebla que se calcula en el componente alfa del color especular para cada vértice. Puede usar las fórmulas que desee: basadas en intervalos, volumétricas o de otro modo. Direct3D usa el factor de niebla proporcionado para interpolar en la superficie de cada polígono. Las aplicaciones que realizan su propia transformación e iluminación también deben realizar sus propios cálculos de niebla de vértices. Como resultado, este tipo de aplicación solo necesita habilitar la combinación de niebla y establecer el color de la niebla a través de los Estados de representación asociados, como se describe en el [apartado de combinación de niebla (Direct3D 9)](fog-blending.md) y en el [color de niebla (Direct3D 9)](fog-color.md).

> [!Note]  
> Cuando se usa un sombreador de vértices, debe usar la niebla de vértice. Esto se logra mediante el sombreador de vértices para escribir la intensidad de la niebla por vértices en el registro oFog. Una vez completado el sombreador de píxeles, los datos de oFog se usan para interpolar linealmente con el color de niebla. Esta intensidad no está disponible en un sombreador de píxeles.

 

## <a name="range-based-fog"></a>Niebla de Range-Based

> [!Note]  
> Direct3D usa cálculos de niebla basados en intervalos solo cuando se usa la niebla de vértices con el motor de transformación y iluminación de Direct3D. Esto se debe a que la niebla de píxeles se implementa en el controlador de dispositivo y no existe ningún hardware actualmente para admitir la niebla basada en intervalos por píxel. Si la aplicación realiza su propia transformación e iluminación, debe realizar sus propios cálculos de niebla, basados en intervalos o en cualquier otro caso.

 

A veces, el uso de niebla puede introducir artefactos gráficos que hacen que los objetos se mezclen con el color de niebla de maneras no intuitivas. Por ejemplo, imagine una escena en la que hay dos objetos visibles: uno lo suficientemente lejano como para que se vea afectado por la niebla y el otro cerca de lo suficiente como para no verse afectado. Si el área de visualización gira en su lugar, los efectos de niebla aparentes pueden cambiar, aunque los objetos sean estacionarios. En el diagrama siguiente se muestra una vista de la parte superior de esta situación.

![diagrama de dos puntos de vista y cómo afectan a la niebla para dos objetos](images/artifog.png)

La niebla basada en intervalos es otra, más precisa, para determinar los efectos de niebla. En la niebla basada en intervalo, Direct3D usa la distancia real desde el punto de vista a un vértice para los cálculos de niebla. Direct3D aumenta el efecto de la niebla a medida que aumenta la distancia entre los dos puntos, en lugar de la profundidad del vértice dentro de la escena, con lo que se evitan los artefactos de rotación.

Si el dispositivo actual admite la niebla basada en intervalos, establecerá el \_ valor de FOGRANGE de D3DPRASTERCAPS en el miembro RasterCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) al llamar al método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) . Para habilitar la niebla basada en intervalos, establezca el \_ Estado de representación de D3DRS RANGEFOGENABLE en **true**.

Direct3D calcula la niebla basada en intervalo durante la transformación y la iluminación. Las aplicaciones que no usan el motor de transformación y iluminación de Direct3D también deben realizar sus propios cálculos de niebla de vértices. En este caso, proporcione el factor de niebla basado en el intervalo en el componente alfa del componente especular para cada vértice.

## <a name="using-vertex-fog"></a>Usar la niebla de vértice

Siga los pasos que se indican a continuación para habilitar la niebla de vértices en la aplicación.

1.  Habilite la combinación de niebla estableciendo D3DRS \_ FOGENABLE en **true**.
2.  Establezca el color de niebla en el \_ Estado de representación de FOGCOLOR de D3DRS.
3.  Elija la fórmula de niebla deseada estableciendo el estado de representación de D3DRS \_ FOGVERTEXMODE en un miembro del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .
4.  Establezca los parámetros de niebla como desee para la fórmula de niebla seleccionada en los Estados de representación.

En el ejemplo siguiente, escrito en C++, se muestra el aspecto que podrían tener estos pasos en el código.


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



Algunos parámetros de niebla son necesarios como valores de punto flotante, aunque el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) solo acepta valores DWORD en el segundo parámetro. En este ejemplo se proporcionan correctamente los valores de punto flotante a estos métodos sin conversión de datos al convertir las direcciones de las variables de punto flotante como punteros DWORD y después desreferenciarlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de niebla](fog-types.md)
</dt> </dl>

 

 
