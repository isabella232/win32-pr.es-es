---
description: Obtiene un puntero al grupo de parámetros compartidos.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: 'ID3DXEffect:: GetPool (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetPool
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 18a35e9bc0a596cb88da6d4c1faf10941fbce8a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003778"
---
# <a name="id3dxeffectgetpool-method"></a>ID3DXEffect:: GetPool (método)

Obtiene un puntero al grupo de parámetros compartidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppPool* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Puntero a un objeto [**ID3DXEffectPool**](id3dxeffectpool.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método siempre devuelve el valor S \_ correcto.

## <a name="remarks"></a>Observaciones

Los grupos contienen parámetros compartidos entre efectos. Vea [clonación y uso compartido (Direct3D 9)](cloning-and-sharing.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




