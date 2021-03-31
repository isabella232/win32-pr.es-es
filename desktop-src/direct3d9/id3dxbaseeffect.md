---
description: Proporciona métodos para obtener y establecer parámetros de efectos como constantes, funciones, sombreadores y técnicas.
ms.assetid: dd5e107d-2f09-4f6c-ad6c-52cbcbe0cbd1
title: Interfaz ID3DXBaseEffect (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e72fabf7db8341821885afb160fa73cb0fc9f395
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157164"
---
# <a name="id3dxbaseeffect-interface"></a>Interfaz ID3DXBaseEffect

Proporciona métodos para obtener y establecer parámetros de efectos como constantes, funciones, sombreadores y técnicas.

## <a name="members"></a>Miembros

La interfaz **ID3DXBaseEffect** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXBaseEffect** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXBaseEffect** tiene estos métodos.



| Método                                                                                    | Descripción                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnnotation**](id3dxbaseeffect--getannotation.md)                                   | Obtiene el identificador de una anotación. <br/>                                                                                                                                                                                     |
| [**GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md)                       | Obtiene el identificador de una anotación buscando su nombre.<br/>                                                                                                                                                               |
| [**GetBool**](id3dxbaseeffect--getbool.md)                                               | Obtiene un valor BOOLEANO.<br/>                                                                                                                                                                                                     |
| [**GetBoolArray**](id3dxbaseeffect--getboolarray.md)                                     | Obtiene una matriz de valores BOOL.<br/>                                                                                                                                                                                          |
| [**GetDesc**](id3dxbaseeffect--getdesc.md)                                               | Obtiene la descripción del efecto.<br/>                                                                                                                                                                                           |
| [**GetFloat**](id3dxbaseeffect--getfloat.md)                                             | Obtiene un valor de punto flotante.<br/>                                                                                                                                                                                           |
| [**GetFloatArray**](id3dxbaseeffect--getfloatarray.md)                                   | Obtiene una matriz de valores de punto flotante.<br/>                                                                                                                                                                                |
| [**GetFunction (**](id3dxbaseeffect--getfunction.md)                                       | Obtiene el identificador de una función.<br/>                                                                                                                                                                                         |
| [**GetFunctionByName**](id3dxbaseeffect--getfunctionbyname.md)                           | Obtiene el identificador de una función buscando su nombre.<br/>                                                                                                                                                                  |
| [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md)                               | Obtiene una descripción de la función.<br/>                                                                                                                                                                                           |
| [**GetInt**](id3dxbaseeffect--getint.md)                                                 | Obtiene un entero.<br/>                                                                                                                                                                                                       |
| [**GetIntArray**](id3dxbaseeffect--getintarray.md)                                       | Obtiene una matriz de enteros.<br/>                                                                                                                                                                                             |
| [**GetMatrix**](id3dxbaseeffect--getmatrix.md)                                           | Obtiene una matriz de nontransposed.<br/>                                                                                                                                                                                           |
| [**GetMatrixArray**](id3dxbaseeffect--getmatrixarray.md)                                 | Obtiene una matriz de matrices nontransposed.<br/>                                                                                                                                                                               |
| [**GetMatrixPointerArray**](id3dxbaseeffect--getmatrixpointerarray.md)                   | Obtiene una matriz de punteros a matrices de nontransposed.<br/>                                                                                                                                                                   |
| [**GetMatrixTranspose**](id3dxbaseeffect--getmatrixtranspose.md)                         | Obtiene una matriz transpuesta.<br/>                                                                                                                                                                                              |
| [**GetMatrixTransposeArray**](id3dxbaseeffect--getmatrixtransposearray.md)               | Obtiene una matriz de matrices transpuestas.<br/>                                                                                                                                                                                  |
| [**GetMatrixTransposePointerArray**](id3dxbaseeffect--getmatrixtransposepointerarray.md) | Obtiene una matriz de punteros a matrices transpuestas.<br/>                                                                                                                                                                      |
| [**GetParameter**](id3dxbaseeffect--getparameter.md)                                     | Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura.<br/>                                                                                                                                              |
| [**GetParameterByName**](id3dxbaseeffect--getparameterbyname.md)                         | Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su nombre.<br/>                                                                                                                       |
| [**GetParameterBySemantic**](id3dxbaseeffect--getparameterbysemantic.md)                 | Obtiene el identificador de un parámetro de nivel superior o un parámetro de miembro de estructura buscando su semántica con una búsqueda que no distinga mayúsculas de minúsculas.<br/>                                                                                    |
| [**GetParameterDesc**](id3dxbaseeffect--getparameterdesc.md)                             | Obtiene un parámetro o una descripción de la anotación.<br/>                                                                                                                                                                            |
| [**GetParameterElement**](id3dxbaseeffect--getparameterelement.md)                       | Obtiene el identificador de un parámetro de elemento de matriz.<br/>                                                                                                                                                                          |
| [**GetPass**](id3dxbaseeffect--getpass.md)                                               | Obtiene el identificador de un paso.<br/>                                                                                                                                                                                             |
| [**GetPassByName**](id3dxbaseeffect--getpassbyname.md)                                   | Obtiene el identificador de un paso buscando su nombre.<br/>                                                                                                                                                                      |
| [**GetPassDesc**](id3dxbaseeffect--getpassdesc.md)                                       | Obtiene una descripción del paso.<br/>                                                                                                                                                                                               |
| [**GetPixelShader**](id3dxbaseeffect--getpixelshader.md)                                 | Obtiene un sombreador de píxeles.<br/>                                                                                                                                                                                                   |
| [**GetString**](id3dxbaseeffect--getstring.md)                                           | Obtiene una cadena.<br/>                                                                                                                                                                                                         |
| [**GetTechnique**](id3dxbaseeffect--gettechnique.md)                                     | Obtiene el identificador de una técnica.<br/>                                                                                                                                                                                        |
| [**GetTechniqueByName**](id3dxbaseeffect--gettechniquebyname.md)                         | Obtiene el identificador de una técnica buscando su nombre.<br/>                                                                                                                                                                 |
| [**GetTechniqueDesc**](id3dxbaseeffect--gettechniquedesc.md)                             | Obtiene una descripción de la técnica.<br/>                                                                                                                                                                                          |
| [**GetTexture**](id3dxbaseeffect--gettexture.md)                                         | Obtiene una textura.<br/>                                                                                                                                                                                                        |
| [**GetValue**](id3dxbaseeffect--getvalue.md)                                             | Obtiene el valor de un parámetro o anotación arbitrarios, incluidos los tipos simples, Structs, matrices, cadenas, sombreadores y texturas. Este método se puede usar en lugar de casi todas las llamadas a GetXXX en **ID3DXBaseEffect**.<br/> |
| [**GetVector**](id3dxbaseeffect--getvector.md)                                           | Obtiene un vector.<br/>                                                                                                                                                                                                         |
| [**GetVectorArray**](id3dxbaseeffect--getvectorarray.md)                                 | Obtiene una matriz de vectores.<br/>                                                                                                                                                                                              |
| [**GetVertexShader**](id3dxbaseeffect--getvertexshader.md)                               | Obtiene un sombreador de vértices.<br/>                                                                                                                                                                                                  |
| [**SetArrayRange**](id3dxbaseeffect--setarrayrange.md)                                   | Establezca el intervalo de una matriz que se va a pasar al dispositivo.<br/>                                                                                                                                                                       |
| [**SetBool**](id3dxbaseeffect--setbool.md)                                               | Establece un valor BOOLEANO.<br/>                                                                                                                                                                                                     |
| [**SetBoolArray**](id3dxbaseeffect--setboolarray.md)                                     | Establece una matriz de valores booleanos.<br/>                                                                                                                                                                                       |
| [**SetFloat**](id3dxbaseeffect--setfloat.md)                                             | Establece un valor de punto flotante.<br/>                                                                                                                                                                                           |
| [**SetFloatArray**](id3dxbaseeffect--setfloatarray.md)                                   | Establece una matriz de valores de punto flotante.<br/>                                                                                                                                                                                |
| [**SetInt**](id3dxbaseeffect--setint.md)                                                 | Establece un entero.<br/>                                                                                                                                                                                                       |
| [**SetIntArray**](id3dxbaseeffect--setintarray.md)                                       | Establece una matriz de enteros.<br/>                                                                                                                                                                                             |
| [**SetMatrix**](id3dxbaseeffect--setmatrix.md)                                           | Establece una matriz no transpuesta.<br/>                                                                                                                                                                                          |
| [**SetMatrixArray**](id3dxbaseeffect--setmatrixarray.md)                                 | Establece una matriz de matrices nontransposed.<br/>                                                                                                                                                                               |
| [**SetMatrixPointerArray**](id3dxbaseeffect--setmatrixpointerarray.md)                   | Establece una matriz de punteros a matrices de nontransposed.<br/>                                                                                                                                                                   |
| [**SetMatrixTranspose**](id3dxbaseeffect--setmatrixtranspose.md)                         | Establece una matriz transpuesta.<br/>                                                                                                                                                                                              |
| [**SetMatrixTransposeArray**](id3dxbaseeffect--setmatrixtransposearray.md)               | Establece una matriz de matrices transpuestas.<br/>                                                                                                                                                                                  |
| [**SetMatrixTransposePointerArray**](id3dxbaseeffect--setmatrixtransposepointerarray.md) | Establece una matriz de punteros a matrices transpuestas.<br/>                                                                                                                                                                      |
| [**SetString**](id3dxbaseeffect--setstring.md)                                           | Establece una cadena.<br/>                                                                                                                                                                                                         |
| [**SetTexture**](id3dxbaseeffect--settexture.md)                                         | Establece una textura.<br/>                                                                                                                                                                                                        |
| [**SetValue**](id3dxbaseeffect--setvalue.md)                                             | Establezca el valor de un parámetro o anotación arbitrario, incluidos los tipos simples, Structs, matrices, cadenas, sombreadores y texturas. <br/>                                                                                        |
| [**SetVector**](id3dxbaseeffect--setvector.md)                                           | Establece un vector.<br/>                                                                                                                                                                                                         |
| [**SetVectorArray**](id3dxbaseeffect--setvectorarray.md)                                 | Establece una matriz de vectores.<br/>                                                                                                                                                                                              |



 

## <a name="remarks"></a>Observaciones

El tipo LPD3DXBASEEFFECT se define como un puntero a esta interfaz.


```
typedef interface ID3DXBaseEffect ID3DXBaseEffect;
typedef interface ID3DXBaseEffect *LPD3DXBASEEFFECT;
        
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de efectos](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> </dl>

 

 
