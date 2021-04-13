---
description: Una función Effect se escribe en HLSL y se declara con la sintaxis siguiente.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Sintaxis de la función Effect (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496151"
---
# <a name="effect-function-syntax-direct3d-10"></a>Sintaxis de la función Effect (Direct3D 10)

Una función Effect se escribe en HLSL y se declara con la sintaxis siguiente.

## <a name="syntax"></a>Sintaxis

*ReturnType* *nombrefunción* ( \[ *ArgumentList* \] )

{

<dl> \[ *Instrucciones* \]
</dl>

};



| Nombre         | Descripción                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ReturnType   | Cualquier [tipo HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)                                                                                                                                                                                                       |
| FunctionName | Cadena ASCII que identifica de forma única el nombre de la función de sombreador.                                                                                                                                                                                            |
| ArgumentList | Uno o más argumentos, separados por comas (vea [argumentos de función (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).                                                                                                                             |
| Instrucciones   | Una o más instrucciones (vea [instrucciones (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) que componen el cuerpo de la función. Si una función se define sin cuerpo, se considera que es un prototipo. y deben redefinirse con un cuerpo antes del uso. |



 

Una función de efecto puede ser un sombreador o simplemente puede ser una función llamada por un sombreador. Una función se identifica de forma exclusiva por su nombre, los tipos de sus parámetros y la plataforma de destino; por lo tanto, las funciones se pueden sobrecargar. Cualquier función HLSL válida debe ajustarse a este formato; para obtener una lista más detallada de la sintaxis de las funciones de HLSL, consulte [funciones (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).

## <a name="example"></a>Ejemplo

El [ejemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa un sombreador de píxeles y un sombreador de vértices. La función de sombreador de píxeles se denomina RenderScenePS y se muestra a continuación.


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

[Formato de efecto](d3d10-effect-format.md)
</dt> </dl>

 

 
