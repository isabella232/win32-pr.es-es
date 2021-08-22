---
description: Obtiene el valor de un parámetro o anotación arbitrarios, incluidos los tipos simples, structs, matrices, cadenas, sombreadores y texturas. Este método se puede usar en lugar de casi todas las llamadas Getxxx en ID3DXBaseEffect.
ms.assetid: 41343922-99a7-486f-b4b0-1aa07f339664
title: Método ID3DXBaseEffect::GetValue (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f957ae3b59f10a086f2326e82478afb6b0ba7fd85bbf6b3f78df5746b7fcb56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494705"
---
# <a name="id3dxbaseeffectgetvalue-method"></a>Método ID3DXBaseEffect::GetValue

Obtiene el valor de un parámetro o anotación arbitrarios, incluidos los tipos simples, structs, matrices, cadenas, sombreadores y texturas. Este método se puede usar en lugar de casi todas las llamadas Getxxx en [**ID3DXBaseEffect**](id3dxbaseeffect.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetValue(
  [in]  D3DXHANDLE hParameter,
  [out] LPVOID     pData,
  [in]  UINT       Bytes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pData* \[ out\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Devuelve un búfer que contiene el valor.

</dd> <dt>

*Bytes* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

\[en \] Número de bytes del búfer. Pase D3DX DEFAULT si sabe que el búfer es lo suficientemente grande como para contener todo el parámetro y desea omitir \_ la validación de tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetValue**](id3dxbaseeffect--setvalue.md)
</dt> </dl>

 

 
