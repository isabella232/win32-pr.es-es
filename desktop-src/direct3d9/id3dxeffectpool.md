---
description: Las aplicaciones usan la interfaz ID3DXEffectPool para identificar los parámetros que se van a compartir entre los efectos. Consulte uso compartido de parámetros en la clonación y el uso compartido (Direct3D 9). Esta interfaz no tiene métodos.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interfaz ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424339"
---
# <a name="id3dxeffectpool-interface"></a>Interfaz ID3DXEffectPool

Las aplicaciones usan la interfaz **ID3DXEffectPool** para identificar los parámetros que se van a compartir entre los efectos. Consulte uso compartido de parámetros en la [clonación y el uso compartido (Direct3D 9)](cloning-and-sharing.md). Esta interfaz no tiene métodos.

## <a name="members"></a>Miembros

La interfaz **ID3DXEffectPool** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , pero no tiene miembros adicionales.

## <a name="remarks"></a>Observaciones

La interfaz ID3DXEffectPool se obtiene llamando a [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).

El tipo LPD3DXEFFECTPOOL se define como un puntero a esta interfaz.


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de efectos](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
