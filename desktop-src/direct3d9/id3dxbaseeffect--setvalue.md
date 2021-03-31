---
description: Establezca el valor de un parámetro o anotación arbitrario, incluidos los tipos simples, Structs, matrices, cadenas, sombreadores y texturas.
ms.assetid: ab71f1a1-3e10-4883-99b4-607e0b5751c2
title: 'ID3DXBaseEffect:: SetValue (método) (D3DX9Shader. h)'
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
ms.openlocfilehash: 3281306240cefc0312ff9a2af7e056dab74a085b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157216"
---
# <a name="id3dxbaseeffectsetvalue-method"></a>ID3DXBaseEffect:: SetValue (método)

Establezca el valor de un parámetro o anotación arbitrario, incluidos los tipos simples, Structs, matrices, cadenas, sombreadores y texturas.

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

*hParameter* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*pdata* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero a un búfer que contiene datos.

</dd> <dt>

*Bytes* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

\[en \] número de bytes en el búfer. Pase \_ el valor predeterminado de D3DX si sabe que el búfer es lo suficientemente grande como para contener todo el parámetro y desea omitir la validación de tamaño.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método se puede usar en lugar de casi todas las llamadas API de conjunto de efectos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetValue**](id3dxbaseeffect--getvalue.md)
</dt> </dl>

 

 
