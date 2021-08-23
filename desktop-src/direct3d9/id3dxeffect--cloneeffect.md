---
description: Crea una copia de un efecto.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: Método ID3DXEffect::CloneEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: ab5ebe2898c1525d3a539121d1e57708c4713df3a06b43bfa41572f0e7b23b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494265"
---
# <a name="id3dxeffectcloneeffect-method"></a>Método ID3DXEffect::CloneEffect

Crea una copia de un efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado al efecto.

</dd> <dt>

*ppEffect* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Puntero a una [**interfaz ID3DXEffect,**](id3dxeffect.md) que contiene el efecto clonado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Esta función no clonará ningún efecto si el usuario especifica [D3DXFX \_ NOT \_ CLONEABLE durante](d3dxfx.md) la creación del efecto.

 

Para actualizar los parámetros compartidos y no compartidos en una técnica activa de un efecto clonado, vea [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
