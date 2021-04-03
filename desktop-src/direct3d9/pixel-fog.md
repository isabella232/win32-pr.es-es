---
description: La niebla de píxeles obtiene su nombre del hecho de que se calcula por píxel en el controlador de dispositivo.
ms.assetid: 6fcfb9fa-cacc-4dbc-bfc6-85d533dbfbf8
title: Niebla de píxeles (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f62a597820fa009207d8dda7836d161cdf34c88
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906325"
---
# <a name="pixel-fog-direct3d-9"></a>Niebla de píxeles (Direct3D 9)

La niebla de píxeles obtiene su nombre del hecho de que se calcula por píxel en el controlador de dispositivo. Esto es diferente del niebla de vértices, que es calculado por la canalización durante los cálculos de transformación e iluminación. La niebla de píxeles a veces se denomina niebla de tabla porque algunos controladores usan una tabla de búsqueda precalculada para determinar el factor de niebla, usando la profundidad de cada píxel que se va a aplicar a los cálculos de mezcla. Se puede aplicar mediante cualquier fórmula de niebla identificada por los miembros del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) . Las implementaciones de estas fórmulas son específicas del controlador. Si un controlador no es compatible con una fórmula de niebla compleja, se debe degradar a una fórmula menos compleja.

## <a name="eye-relative-vs-z-based-depth"></a>Profundidad basada en Eye-Relative frente a Z

Para aliviar los artefactos gráficos relacionados con la niebla causados por la distribución desigual de los valores z en un búfer de profundidad, la mayoría de los dispositivos de hardware usan la profundidad relativa a la vista en lugar de los valores de profundidad basados en z para la niebla de píxeles. La profundidad relativa a la vista es esencialmente el elemento w de un conjunto de coordenadas homogéneo. Microsoft Direct3D toma el recíproco del elemento RHW de un conjunto de coordenadas de espacio de dispositivo para reproducir true. Si un dispositivo admite la niebla relativa a la vista, establece la marca **D3DPRASTERCAPS \_ WFOG** en el miembro RasterCaps de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) cuando se llama al método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) . A excepción del rasterizador de referencia, los dispositivos de software siempre utilizan z para calcular los efectos de niebla de píxeles.

Cuando se admite la niebla relativa a la vista, el sistema utiliza automáticamente la profundidad relativa a la vista en lugar de la profundidad basada en z si la matriz de proyección proporcionada genera valores z en el espacio universal que son equivalentes a los valores w en el espacio del dispositivo. La matriz de proyección se establece llamando al método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) , utilizando el \_ valor de proyección D3DTS y pasando una estructura [**D3DMATRIX**](d3dmatrix.md) que representa la matriz deseada. Si la matriz de proyección no es compatible con este requisito, los efectos de niebla no se aplican correctamente. Para obtener más información sobre cómo generar una matriz compatible, vea [transformación de proyección (Direct3D 9)](projection-transform.md).

Direct3D usa la matriz de proyección establecida actualmente en los cálculos de profundidad basados en w. Como resultado, una aplicación debe establecer una matriz de proyección compatible para recibir las características basadas en w deseadas, incluso si no usa la canalización de transformación de Direct3D.

Direct3D comprueba la cuarta columna de la matriz de proyección. Si los coeficientes son \[ 0, 0, 0, 1 \] (para una proyección afín), el sistema usará valores de profundidad basados en z para la niebla. En este caso, también debe especificar las distancias de inicio y finalización de los efectos de niebla lineal en el espacio del dispositivo, que va desde 0,0 en el punto más cercano al usuario y 1,0 en el punto más lejano.

## <a name="using-pixel-fog"></a>Usar la niebla de píxeles

Siga los pasos que se indican a continuación para habilitar la niebla de píxeles en la aplicación.

1.  Habilite la combinación de niebla mediante el establecimiento del estado de representación de FOGENABLE de D3DRS \_ en **true**.
2.  Establezca el color de niebla deseado en el \_ Estado de representación de D3DRS FOGCOLOR.
3.  Elija la fórmula de niebla que se va a usar estableciendo el \_ Estado de representación de D3DRS FOGTABLEMODE en el miembro correspondiente del tipo enumerado [**D3DFOGMODE**](./d3dfogmode.md) .
4.  Establezca los parámetros de niebla como desee para el modo de niebla seleccionado en los Estados de representación asociados. Esto incluye las distancias de inicio y finalización para la niebla lineal y la densidad de niebla para el modo de niebla exponencial.

En el ejemplo siguiente se muestra el aspecto de estos pasos en el código.


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



Algunos parámetros de niebla son necesarios como valores de punto flotante, aunque el método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) solo acepta valores DWORD en el segundo parámetro. En el ejemplo anterior se proporcionan los valores de punto flotante a **IDirect3DDevice9:: SetRenderState** sin conversión de datos al convertir las direcciones de las variables de punto flotante como punteros DWORD y, a continuación, desreferenciarlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos de niebla](fog-types.md)
</dt> </dl>

 

 
