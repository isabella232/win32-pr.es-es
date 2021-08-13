---
title: Sintaxis de función de efecto (Direct3D 11)
description: Una función de efecto se escribe en HLSL y se declara con la sintaxis descrita en esta sección.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 945f7104d44947f37af71ce664dd99ff64362062b1d42af62af2054538bacb52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046623"
---
# <a name="effect-function-syntax-direct3d-11"></a>Sintaxis de función de efecto (Direct3D 11)

Una función de efecto se escribe en HLSL y se declara con la sintaxis descrita en esta sección.

## <a name="syntax"></a>Sintaxis

*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )

{

<dl> \[ *Instrucciones* \]
</dl>

};



| Nombre         | Descripción                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Cualquier [tipo HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | Cadena ASCII que identifica de forma única el nombre de la función de sombreador.                                                                                                                                                                                            |
| ArgumentList | Uno o varios argumentos, separados por comas (vea [Argumentos de función (DirectX HLSL).](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)                                                                                                                             |
| Instrucciones   | Una o varias instrucciones (vea [Instrucciones (HLSL de DirectX)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) que son el cuerpo de la función. Si una función se define sin un cuerpo, se considera un prototipo; y se deben volver a definir con un cuerpo antes de su uso. |



 

Una función de efecto puede ser un sombreador o simplemente puede ser una función a la que llama un sombreador. Una función se identifica de forma única por su nombre, los tipos de sus parámetros y la plataforma de destino. por lo tanto, las funciones se pueden sobrecargar. Cualquier función HLSL válida debe ajustarse a este formato; Para obtener una lista más detallada de la sintaxis de las funciones HLSL, vea [Functions (DirectX HLSL).](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions)

## <a name="example"></a>Ejemplo

A continuación se muestra un ejemplo de una función de sombreador de píxeles.


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](d3d11-effect-format.md)
</dt> </dl>

 

 