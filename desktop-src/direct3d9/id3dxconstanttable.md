---
description: La interfaz ID3DXConstantTable se usa para tener acceso a la tabla de constantes. Esta tabla contiene las variables que usan los sombreadores y efectos de lenguaje de alto nivel.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interfaz ID3DXConstantTable (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bb2b7614c4d6a0e677f71e66ab94abdb89deb973
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718245"
---
# <a name="id3dxconstanttable-interface"></a>Interfaz ID3DXConstantTable

La interfaz ID3DXConstantTable se usa para tener acceso a la tabla de constantes. Esta tabla contiene las variables que usan los sombreadores y efectos de lenguaje de alto nivel.

## <a name="members"></a>Miembros

La interfaz **ID3DXConstantTable** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXConstantTable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXConstantTable** tiene estos métodos.



| Método                                                                                       | Descripción                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBufferPointer**](id3dxconstanttable--getbufferpointer.md)                             | Obtiene un puntero al búfer que contiene la tabla de constantes.<br/>                                                          |
| [**GetBufferSize**](id3dxconstanttable--getbuffersize.md)                                   | Obtiene el tamaño de búfer de la tabla de constantes.<br/>                                                                             |
| [**GetConstant**](id3dxconstanttable--getconstant.md)                                       | Obtiene una constante mediante la búsqueda de su índice.<br/>                                                                                |
| [**GetConstantByName**](id3dxconstanttable--getconstantbyname.md)                           | Obtiene una constante buscando su nombre.<br/>                                                                                 |
| [**GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)                               | Obtiene un puntero a una matriz de descripciones constantes en la tabla Constant.<br/>                                              |
| [**GetConstantElement**](id3dxconstanttable--getconstantelement.md)                         | Obtiene una constante de una matriz de constantes. Una matriz se compone de elementos.<br/>                                            |
| [**GetDesc**](id3dxconstanttable--getdesc.md)                                               | Obtiene una descripción de la tabla de constantes.<br/>                                                                               |
| [**GetSamplerIndex**](id3dxconstanttable--getsamplerindex.md)                               | Devuelve el índice de muestra.<br/>                                                                                              |
| [**SetBool**](id3dxconstanttable--setbool.md)                                               | Establece un valor booleano.<br/>                                                                                                   |
| [**SetBoolArray**](id3dxconstanttable--setboolarray.md)                                     | Establece una matriz de valores booleanos.<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | Establece las constantes en sus valores predeterminados. Los valores predeterminados se declaran en las declaraciones de variable en el sombreador.<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | Establece un número de punto flotante.<br/>                                                                                           |
| [**SetFloatArray**](id3dxconstanttable--setfloatarray.md)                                   | Establece una matriz de números de punto flotante.<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | Establece un valor entero.<br/>                                                                                                  |
| [**SetIntArray**](id3dxconstanttable--setintarray.md)                                       | Establece una matriz de enteros.<br/>                                                                                              |
| [**SetMatrix**](id3dxconstanttable--setmatrix.md)                                           | Establece una matriz de nontransposed.<br/>                                                                                            |
| [**SetMatrixArray**](id3dxconstanttable--setmatrixarray.md)                                 | Establece una matriz de matrices nontransposed.<br/>                                                                                |
| [**SetMatrixPointerArray**](id3dxconstanttable--setmatrixpointerarray.md)                   | Establece una matriz de punteros a matrices de nontransposed.<br/>                                                                    |
| [**SetMatrixTranspose**](id3dxconstanttable--setmatrixtranspose.md)                         | Establece una matriz transpuesta.<br/>                                                                                               |
| [**SetMatrixTransposeArray**](id3dxconstanttable--setmatrixtransposearray.md)               | Establece una matriz de matrices transpuestas.<br/>                                                                                   |
| [**SetMatrixTransposePointerArray**](id3dxconstanttable--setmatrixtransposepointerarray.md) | Establece una matriz de punteros a matrices transpuestas.<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | Establece el contenido del búfer en la tabla de constantes.<br/>                                                                  |
| [**SetVector**](id3dxconstanttable--setvector.md)                                           | Establece un vector 4D.<br/>                                                                                                       |
| [**SetVectorArray**](id3dxconstanttable--setvectorarray.md)                                 | Establece una matriz de vectores 4D.<br/>                                                                                            |



 

## <a name="remarks"></a>Observaciones

El tipo LPD3DXCONSTANTTABLE se define como un puntero a la interfaz **ID3DXConstantTable** .


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
