---
description: Busca un comentario determinado en un sombreador. El comentario se identifica mediante un código de cuatro caracteres (FOURCC) en el primer valor DWORD del comentario.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Función D3DXFindShaderComment (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707885"
---
# <a name="d3dxfindshadercomment-function"></a>D3DXFindShaderComment función)

Busca un comentario determinado en un sombreador. El comentario se identifica mediante un código de cuatro caracteres (FOURCC) en el primer valor DWORD del comentario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFunction* \[ de\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a la secuencia DWORD de la función de sombreador.

</dd> <dt>

*FourCC* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Código FOURCC que identifica el bloque de comentario. Vea [formatos FourCC](d3dformat.md).

</dd> <dt>

*ppData* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Devuelve un puntero a los datos de comentario (sin incluir el token de comentario y el código FOURCC). Este valor puede ser **null**.

</dd> <dt>

*pSizeInBytes* \[ enuncia\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Devuelve el tamaño de los datos de comentario en bytes. Este valor puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si no se encuentra el comentario y no se ha producido ningún otro error, \_ se devuelve S false.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones del sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
