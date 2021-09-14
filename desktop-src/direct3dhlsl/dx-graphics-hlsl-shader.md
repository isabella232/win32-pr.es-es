---
title: Tipo de sombreador
description: La sintaxis para declarar una variable de sombreador en un efecto ha cambiado de Direct3D 9 a Direct3D 10.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Tipo de sombreador HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974736"
---
# <a name="shader-type"></a>Tipo de sombreador

La sintaxis para declarar una variable de sombreador en un efecto ha cambiado de Direct3D 9 a Direct3D 10.

## <a name="shader-type-for-direct3d-10"></a>Tipo de sombreador para Direct3D 10

Declare una variable de sombreador dentro de un paso de efecto (en Direct3D 10) mediante la sintaxis de tipo de sombreador:



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SetPixelShader** Compile( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile( **ShaderTarget, ShaderFunction** ); |



 

### <a name="parameters"></a>Parámetros



| Elemento                                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**<br/>         | La llamada API de Direct3D que crea el objeto de sombreador. Puede ser: **SetPixelShader,** **SetGeometryShader** o **SetVertexShader.**<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>         | Modelo de sombreador con el que se compilará. Esto es válido para cualquier destino, incluidos todos los destinos de Direct3D 9 más el modelo de sombreador [4](dx-graphics-hlsl-sm4.md) destinos: frente a \_ 4 \_ 0, gs \_ 4 0 y ps \_ \_ 4 \_ 0.<br/>                                                                                                                                                                                                                                          |
| <span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**<br/> | Cadena ASCII que contiene el nombre de la función de punto de entrada del sombreador; esta es la función que comienza la ejecución cuando se invoca el sombreador. (...) representa los argumentos del sombreador; estos son los mismos argumentos que se pasan a la API de creación del sombreador: [**VSSetShader,**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) o [**PSSetShader.**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader)<br/> |



 

### <a name="example"></a>Ejemplo

Este es un ejemplo que crea un sombreador de vértices y un objeto de sombreador de píxeles, compilados para un modelo de sombreador determinado. En el ejemplo de Direct3D 10, no hay ningún sombreador de geometría, por lo que el puntero se establece en **NULL.**


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a>Tipo de sombreador para Direct3D 9

Declare una variable de sombreador dentro de un paso de efecto (para Direct3D 9) mediante la sintaxis de tipo de sombreador:



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| **PixelShader** = compile **ShaderTarget ShaderFunction(...); VertexShader** = compile **ShaderTarget ShaderFunction(...);** |



 

### <a name="parameters"></a>Parámetros



| Elemento                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**<br/>                                         | Variable de sombreador, que representa el sombreador compilado. Puede ser: **PixelShader o** **VertexShader.**<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>                             | Modelo [de sombreador con](dx-graphics-hlsl-models.md) el que se compilará; depende del tipo de variable de sombreador.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**<br/> | Cadena ASCII que contiene el nombre de la función de punto de entrada del sombreador; esta es la función que comienza la ejecución cuando se invoca el sombreador. (...) representa los argumentos del sombreador; estos son los mismos argumentos que se pasan a la API de creación del sombreador: [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) o [**SetPixelShader.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)<br/> |



 

### <a name="example"></a>Ejemplo

Este es un ejemplo de un sombreador de vértices y un objeto de sombreador de píxeles, compilado para un modelo de sombreador determinado.


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

