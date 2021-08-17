---
description: Busca un comentario determinado en un sombreador. El comentario se identifica mediante un código de cuatro caracteres (FOURCC) en el primer DWORD del comentario.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: Función D3DXFindShaderComment (D3DX9Shader.h)
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
ms.openlocfilehash: 07ff15b77866732f7a2dcab814e1ccf84d5344f640d83300af874e162485879b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096060"
---
# <a name="d3dxfindshadercomment-function"></a>Función D3DXFindShaderComment

Busca un comentario determinado en un sombreador. El comentario se identifica mediante un código de cuatro caracteres (FOURCC) en el primer DWORD del comentario.

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

*pFunction* \[ En\]
</dt> <dd>

Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***

Puntero a la secuencia DWORD de la función de sombreador.

</dd> <dt>

*FourCC* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Código FOURCC que identifica el bloque de comentarios. Vea [Formatos fourCC](d3dformat.md).

</dd> <dt>

*ppData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)\***

Devuelve un puntero a los datos de comentario (sin incluir el token de comentario y el código FOURCC). Este valor puede ser **NULL.**

</dd> <dt>

*pSizeInBytes* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Devuelve el tamaño de los datos de comentario en bytes. Este valor puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si no se encuentra el comentario y no se ha producido ningún otro error, se devuelve S \_ FALSE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de sombreador](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
