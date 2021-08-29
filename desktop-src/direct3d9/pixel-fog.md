---
description: Pixel pixel pixel gets its name from the fact that it is calculated on a per-pixel basis in the device driver.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Pixel Pixel Pixel (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73606f585b78b0f8a1f92d669e936f503900d700c2a2f44cb654019d5315864a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628375"
---
# <a name="pixel-fog-direct3d-9"></a>Pixel Pixel Pixel (Direct3D 9)

Pixel pixel pixel gets its name from the fact that it is calculated on a per-pixel basis in the device driver. Esto es diferente de la curva de vértices, que se calcula mediante la canalización durante los cálculos de transformación e iluminación. Los píxeles a veces se denominan "tabla", ya que algunos controladores usan una tabla de búsqueda precalculada para determinar el factor de fusión, usando la profundidad de cada píxel para aplicar en los cálculos de combinación. Se puede aplicar mediante cualquier fórmula de fórmula identificada por los miembros del tipo enumerado [**D3DFOGMODE.**](./d3dfogmode.md) Las implementaciones de estas fórmulas son específicas del controlador. Si un controlador no admite una fórmula compleja, debe degradarse a una fórmula menos compleja.

## <a name="eye-relative-vs-z-based-depth"></a>Eye-Relative frente a la profundidad basada en Z

Para mitigar los artefactos gráficos relacionados con la humedad causados por una distribución desigual de los valores z en un búfer de profundidad, la mayoría de los dispositivos de hardware usan la profundidad relativa a los ojos en lugar de los valores de profundidad basados en Z para el desenlazado de píxeles. La profundidad relativa de los ojos es básicamente el elemento w de un conjunto de coordenadas homogéneo. Microsoft Direct3D toma el recíproco del elemento RHW de un conjunto de coordenadas de espacio del dispositivo para reproducir true w. Si un dispositivo es compatible con los ojos, establece la marca **\_ WFOG D3DPRASTERCAPS** en el miembro RasterCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) cuando se llama al método [**IDirect3DDevice9::GetDeviceCaps.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) A excepción del rasterizador de referencia, los dispositivos de software siempre usan z para calcular los efectos de píxeles.

Cuando se admite la matriz relativa de los ojos, el sistema usa automáticamente la profundidad relativa a los ojos en lugar de la profundidad basada en z si la matriz de proyección proporcionada genera valores z en el espacio mundial equivalentes a w-values en el espacio del dispositivo. Establezca la matriz de proyección llamando al método [**IDirect3DDevice9::SetTransform,**](/windows/desktop/api) usando el valor PROYECCIÓN de D3DTS y pasando una estructura \_ [**D3DMATRIX**](d3dmatrix.md) que representa la matriz deseada. Si la matriz de proyección no cumple este requisito, los efectos de efecto de efecto no se aplican correctamente. Para obtener más información sobre cómo generar una matriz compatible, vea [Transformación de proyección (Direct3D 9).](projection-transform.md)

Direct3D usa la matriz de proyección establecida actualmente en sus cálculos de profundidad basados en w. Como resultado, una aplicación debe establecer una matriz de proyección compatible para recibir las características deseadas basadas en w, incluso si no usa la canalización de transformación direct3D.

Direct3D comprueba la cuarta columna de la matriz de proyección. Si los coeficientes son \[ 0,0,0,1 (para una proyección afín), el sistema usará valores de profundidad basados en z para \] el ángulo. En este caso, también debe especificar las distancias de inicio y finalización para los efectos lineales de ánima en el espacio del dispositivo, que oscila entre 0,0 en el punto más cercano al usuario y 1,0 en el punto más alejado.

## <a name="using-pixel-fog"></a>Uso de Pixel Pixel Pixel

Siga estos pasos para habilitar pixeles en la aplicación.

1.  Habilite la combinación de mezcla estableciendo el estado de representación \_ DE D3DRSEVEENABLE en **TRUE.**
2.  Establezca el color de paleta deseado en el estado de representación \_ D3DRSCOLOR DE COLOR.
3.  Elija la fórmula de fórmula que se va a usar estableciendo el estado de representación D3DRSOGTABLEMODE en el miembro correspondiente del tipo \_ enumerado [**D3DFOGMODE.**](./d3dfogmode.md)
4.  Establezca los parámetros de yón como desee para el modo de nube seleccionado en los estados de representación asociados. Esto incluye las distancias de inicio y finalización para la curva lineal y la densidad de densidad para el modo de fusión exponencial.

En el ejemplo siguiente se muestra el aspecto que podrían tener estos pasos en el código.


```
// For brevity, error values in this example are not checked 
//   after each call. A real-world application should check 
//   these values appropriately.
//
// For the purposes of this example, g_pDevice is a valid
//   pointer to an IDirect3DDevice9 interface.
void SetupPixelFog(DWORD Color, DWORD Mode)
{
    float Start   = 0.5f;    // For linear mode
    float End     = 0.8f;
    float Density = 0.66f;   // For exponential modes
 
    // Enable fog blending.
    g_pDevice->SetRenderState(D3DRS_FOGENABLE, TRUE);
 
    // Set the fog color.
    g_pDevice->SetRenderState(D3DRS_FOGCOLOR, Color);
    
    // Set fog parameters.
    if( Mode == D3DFOG_LINEAR )
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGSTART, *(DWORD *)(&Start));
        g_pDevice->SetRenderState(D3DRS_FOGEND,   *(DWORD *)(&End));
    }
    else
    {
        g_pDevice->SetRenderState(D3DRS_FOGTABLEMODE, Mode);
        g_pDevice->SetRenderState(D3DRS_FOGDENSITY, *(DWORD *)(&Density));
    }
```



Algunos parámetros de nodo son necesarios como valores de punto flotante, aunque el método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) solo acepta valores DWORD en el segundo parámetro. En el ejemplo anterior se proporcionan los valores de punto flotante a **IDirect3DDevice9::SetRenderState** sin traducción de datos al convertir las direcciones de las variables de punto flotante como punteros DWORD y, a continuación, desreferenciarlos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de vaselina](fog-types.md)
</dt> </dl>

 

 
