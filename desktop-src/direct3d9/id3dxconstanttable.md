---
description: La interfaz ID3DXConstantTable se usa para tener acceso a la tabla constante. Esta tabla contiene las variables que usan los sombreadores y efectos de lenguaje de alto nivel.
ms.assetid: 5d412c77-3d35-4913-86e5-8efa0549a2bb
title: Interfaz ID3DXConstantTable (D3DX9Shader.h)
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
ms.openlocfilehash: 0ead9e594e79daf8bd43bf4125b857030482028f7128c8063196413d52c9a8b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675485"
---
# <a name="id3dxconstanttable-interface"></a>Interfaz ID3DXConstantTable

La interfaz ID3DXConstantTable se usa para tener acceso a la tabla constante. Esta tabla contiene las variables que usan los sombreadores y efectos de lenguaje de alto nivel.

## <a name="members"></a>Miembros

La **interfaz ID3DXConstantTable** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXConstantTable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DXConstantTable** tiene estos métodos.



| Método                                                                                       | Descripción                                                                                                                        |
|:---------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBufferPointer**](id3dxconstanttable--getbufferpointer.md)                             | Obtiene un puntero al búfer que contiene la tabla constante.<br/>                                                          |
| [**GetBufferSize**](id3dxconstanttable--getbuffersize.md)                                   | Obtiene el tamaño de búfer de la tabla constante.<br/>                                                                             |
| [**GetConstant**](id3dxconstanttable--getconstant.md)                                       | Obtiene una constante mediante la búsqueda de su índice.<br/>                                                                                |
| [**GetConstantByName**](id3dxconstanttable--getconstantbyname.md)                           | Obtiene una constante mediante la búsqueda de su nombre.<br/>                                                                                 |
| [**GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)                               | Obtiene un puntero a una matriz de descripciones constantes de la tabla constante.<br/>                                              |
| [**GetConstantElement**](id3dxconstanttable--getconstantelement.md)                         | Obtiene una constante de una matriz de constantes. Una matriz se forma de elementos .<br/>                                            |
| [**GetDesc**](id3dxconstanttable--getdesc.md)                                               | Obtiene una descripción de la tabla constante.<br/>                                                                               |
| [**GetSamplerIndex**](id3dxconstanttable--getsamplerindex.md)                               | Devuelve el índice del muestreador.<br/>                                                                                              |
| [**SetBool**](id3dxconstanttable--setbool.md)                                               | Establece un valor booleano.<br/>                                                                                                   |
| [**SetBoolArray**](id3dxconstanttable--setboolarray.md)                                     | Establece una matriz de valores booleanos.<br/>                                                                                        |
| [**SetDefaults**](id3dxconstanttable--setdefaults.md)                                       | Establece las constantes en sus valores predeterminados. Los valores predeterminados se declaran en las declaraciones de variable en el sombreador.<br/> |
| [**SetFloat**](id3dxconstanttable--setfloat.md)                                             | Establece un número de punto flotante.<br/>                                                                                           |
| [**SetFloatArray**](id3dxconstanttable--setfloatarray.md)                                   | Establece una matriz de números de punto flotante.<br/>                                                                                |
| [**SetInt**](id3dxconstanttable--setint.md)                                                 | Establece un valor entero.<br/>                                                                                                  |
| [**SetIntArray**](id3dxconstanttable--setintarray.md)                                       | Establece una matriz de enteros.<br/>                                                                                              |
| [**SetMatrix**](id3dxconstanttable--setmatrix.md)                                           | Establece una matriz sin transacciones.<br/>                                                                                            |
| [**SetMatrixArray**](id3dxconstanttable--setmatrixarray.md)                                 | Establece una matriz de matrices no transpuestas.<br/>                                                                                |
| [**SetMatrixPointerArray**](id3dxconstanttable--setmatrixpointerarray.md)                   | Establece una matriz de punteros a matrices no transaccionadas.<br/>                                                                    |
| [**SetMatrixTranspose**](id3dxconstanttable--setmatrixtranspose.md)                         | Establece una matriz transpuesta.<br/>                                                                                               |
| [**SetMatrixTransposeArray**](id3dxconstanttable--setmatrixtransposearray.md)               | Establece una matriz de matrices transpuestas.<br/>                                                                                   |
| [**SetMatrixTransposePointerArray**](id3dxconstanttable--setmatrixtransposepointerarray.md) | Establece una matriz de punteros en matrices transpuestas.<br/>                                                                       |
| [**SetValue**](id3dxconstanttable--setvalue.md)                                             | Establece el contenido del búfer en la tabla constante.<br/>                                                                  |
| [**SetVector**](id3dxconstanttable--setvector.md)                                           | Establece un vector 4D.<br/>                                                                                                       |
| [**SetVectorArray**](id3dxconstanttable--setvectorarray.md)                                 | Establece una matriz de vectores 4D.<br/>                                                                                            |



 

## <a name="remarks"></a>Comentarios

El tipo LPD3DXCONSTANTTABLE se define como un puntero a la **interfaz ID3DXConstantTable.**


```
typedef interface ID3DXConstantTable ID3DXConstantTable;
typedef interface ID3DXConstantTable *LPD3DXCONSTANTTABLE;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[D3DX Interfaces](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
