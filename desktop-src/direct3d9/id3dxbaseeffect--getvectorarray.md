---
description: Obtiene una matriz de vectores.
ms.assetid: 75fe454c-75f7-4f03-acd2-dd9cbf94fb96
title: Método ID3DXBaseEffect::GetVectorArray (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetVectorArray
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: fa57553b993d5746b54e9a03c6b4e52f71937f0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474467"
---
# <a name="id3dxbaseeffectgetvectorarray-method"></a>Método ID3DXBaseEffect::GetVectorArray

Obtiene una matriz de vectores.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVectorArray(
  [in]  D3DXHANDLE  hParameter,
  [out] D3DXVECTOR4 *pVector,
  [in]  UINT        Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pVector* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR4**](d3dxvector4.md)\***

Devuelve una matriz de vectores de punto flotante 4D.

</dd> <dt>

*Recuento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vectores de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Si los vectores de destino son mayores que los vectores de origen, solo se rellenarán los componentes iniciales de cada vector de destino y los restantes componentes del vector de destino se establecerán en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**SetVectorArray**](id3dxbaseeffect--setvectorarray.md)
</dt> </dl>

 

 
