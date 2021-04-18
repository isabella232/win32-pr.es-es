---
description: Bloquea un búfer de vértice y obtiene un puntero a la memoria del búfer de vértices.
ms.assetid: afcd479c-b268-4720-b26c-88b82f1aab08
title: 'ID3DXBaseMesh:: LockVertexBuffer (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.LockVertexBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2e93e59715d9f262d7693f2bef652f8be63337f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718260"
---
# <a name="id3dxbasemeshlockvertexbuffer-method"></a>ID3DXBaseMesh:: LockVertexBuffer (método)

Bloquea un búfer de vértice y obtiene un puntero a la memoria del búfer de vértices.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LockVertexBuffer(
  [in]          DWORD  Flags,
  [out, retval] LPVOID *ppData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de cero o más marcas de bloqueo que describen el tipo de bloqueo que se va a realizar. Para este método, las marcas válidas son:

-   \_Descartar D3DLOCK
-   \_No se \_ pudo \_ Actualizar D3DLOCK
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ ReadOnly
-   D3DLOCK \_ NOOVERWRITE

Para obtener una descripción de las marcas, vea [D3DLOCK](d3dlock.md).

</dd> <dt>

*ppData* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)\***

\*Puntero void a un búfer que contiene los datos de vértices.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Al trabajar con búferes de vértices, se permite realizar varias llamadas de bloqueo; sin embargo, debe asegurarse de que el número de llamadas de bloqueo coincide con el número de llamadas de desbloqueo. Las llamadas a DrawPrimitive no se realizarán correctamente con ningún recuento de bloqueos pendientes en ningún búfer de vértice establecido actualmente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
