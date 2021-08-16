---
description: Obtiene un puntero al grupo de parámetros compartidos.
ms.assetid: 1e999fd5-76ef-43fa-8a77-ae6f2821f46d
title: Método ID3DXEffect::GetPool (D3DX9Effect.h)
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
ms.openlocfilehash: 0220b2864d6c668c2d4fbb71925da6452f6cc8661d0d931a379969418dfe7e19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118521231"
---
# <a name="id3dxeffectgetpool-method"></a>Método ID3DXEffect::GetPool

Obtiene un puntero al grupo de parámetros compartidos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPool(
  [out] LPD3DXEFFECTPOOL *ppPool
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppPool* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)\***

Puntero a un [**objeto ID3DXEffectPool.**](id3dxeffectpool.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método siempre devuelve el valor S \_ OK.

## <a name="remarks"></a>Comentarios

Los grupos contienen parámetros compartidos entre efectos. Consulte [Clonación y uso compartido (Direct3D 9).](cloning-and-sharing.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




