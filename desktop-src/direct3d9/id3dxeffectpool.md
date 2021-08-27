---
description: Las aplicaciones usan la interfaz ID3DXEffectPool para identificar los parámetros que se van a compartir entre los efectos. Consulte uso compartido de parámetros en Clonación y uso compartido (Direct3D 9). Esta interfaz no tiene métodos.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interfaz ID3DXEffectPool (D3DX9Effect.h)
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
ms.openlocfilehash: 42b7669d974fffde76c8c8f1e7beb4f8d78bf58fda3810130b255d4bc5a693df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118685"
---
# <a name="id3dxeffectpool-interface"></a>Interfaz ID3DXEffectPool

Las aplicaciones usan **la interfaz ID3DXEffectPool para** identificar los parámetros que se van a compartir entre los efectos. Vea uso compartido de parámetros [en Clonación y uso compartido (Direct3D 9).](cloning-and-sharing.md) Esta interfaz no tiene métodos.

## <a name="members"></a>Miembros

La **interfaz ID3DXEffectPool** hereda de la [**interfaz IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pero no tiene miembros adicionales.

## <a name="remarks"></a>Comentarios

La interfaz ID3DXEffectPool se obtiene mediante una llamada a [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).

El tipo LPD3DXEFFECTPOOL se define como un puntero a esta interfaz.


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de efecto](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
