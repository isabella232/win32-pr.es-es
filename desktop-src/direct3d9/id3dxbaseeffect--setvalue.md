---
description: Establezca el valor de un parámetro o anotación arbitrarios, incluidos los tipos simples, structs, matrices, cadenas, sombreadores y texturas.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: Método ID3DXBaseEffect::SetValue (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetValue
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2bb619c9d0ef469b36f96d1e35ee70719ede8f6eee494cc950f6fabadbf86304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748975"
---
# <a name="id3dxbaseeffectsetvalue-method"></a>Método ID3DXBaseEffect::SetValue

Establezca el valor de un parámetro o anotación arbitrarios, incluidos los tipos simples, structs, matrices, cadenas, sombreadores y texturas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetValue(
  [in] D3DXHANDLE hParameter,
  [in] LPCVOID    pData,
  [in] UINT       Bytes
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero a un búfer que contiene datos.

</dd> <dt>

*Bytes* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

\[en \] Número de bytes del búfer. Pase D3DX DEFAULT si sabe que el búfer es lo suficientemente grande como para contener todo el parámetro y desea omitir \_ la validación de tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método se puede usar en lugar de casi todas las llamadas API del conjunto de efectos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetValue**](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
