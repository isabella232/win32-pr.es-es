---
title: Sintaxis de la función Effect (Direct3D 11)
description: Una función Effect se escribe en HLSL y se declara con la sintaxis descrita en esta sección.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791685"
---
# <a name="effect-function-syntax-direct3d-11"></a>Sintaxis de la función Effect (Direct3D 11)

Una función Effect se escribe en HLSL y se declara con la sintaxis descrita en esta sección.

## <a name="syntax"></a>Sintaxis

*ReturnType* *nombrefunción* ( \[ *ArgumentList* \] )

{

<dl> \[ *Instrucciones* \]
</dl>

};



| Nombre         | Descripción                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Cualquier [tipo HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)                                                                                                                                                                                                       |
| FunctionName | Cadena ASCII que identifica de forma única el nombre de la función de sombreador.                                                                                                                                                                                            |
| ArgumentList | Uno o más argumentos, separados por comas (vea [argumentos de función (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).                                                                                                                             |
| Instrucciones   | Una o más instrucciones (vea [instrucciones (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) que componen el cuerpo de la función. Si una función se define sin cuerpo, se considera que es un prototipo. y deben redefinirse con un cuerpo antes del uso. |



 

Una función de efecto puede ser un sombreador o simplemente puede ser una función llamada por un sombreador. Una función se identifica de forma exclusiva por su nombre, los tipos de sus parámetros y la plataforma de destino; por lo tanto, las funciones se pueden sobrecargar. Cualquier función HLSL válida debe ajustarse a este formato; para obtener una lista más detallada de la sintaxis de las funciones de HLSL, consulte [funciones (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).

## <a name="example"></a>Ejemplo

El siguiente es un ejemplo de una función de sombreador de píxeles.


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

 

 