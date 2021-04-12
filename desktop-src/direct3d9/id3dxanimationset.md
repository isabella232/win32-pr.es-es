---
description: Esta interfaz encapsula la funcionalidad mínima necesaria de una animación establecida por un controlador de animaciones.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Interfaz ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280503"
---
# <a name="id3dxanimationset-interface"></a>Interfaz ID3DXAnimationSet

Esta interfaz encapsula la funcionalidad mínima necesaria de una animación establecida por un controlador de animaciones. Es posible que los usuarios avanzados deseen implementar esta interfaz para satisfacer sus necesidades especializadas. sin embargo, para la mayoría de los usuarios, las interfaces derivadas [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) y [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) deben ser suficientes.

## <a name="members"></a>Miembros

La interfaz **ID3DXAnimationSet** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationSet** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DXAnimationSet** tiene estos métodos.



| Método                                                                        | Descripción                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**GetAnimationIndexByName**](id3dxanimationset--getanimationindexbyname.md) | Obtiene el índice de una animación, dado su nombre.<br/>                        |
| [**GetAnimationNameByIndex**](id3dxanimationset--getanimationnamebyindex.md) | Obtiene el nombre de una animación, según su índice.<br/>                        |
| [**GetCallback**](id3dxanimationset--getcallback.md)                         | Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.<br/>       |
| [**GetName**](id3dxanimationset--getname.md)                                 | Obtiene el nombre del conjunto de animaciones.<br/>                                           |
| [**GetNumAnimations**](id3dxanimationset--getnumanimations.md)               | Obtiene el número de animaciones en el conjunto de animaciones.<br/>                    |
| [**GetPeriod**](id3dxanimationset--getperiod.md)                             | Obtiene el período del conjunto de animaciones.<br/>                                  |
| [**GetPeriodicPosition**](id3dxanimationset--getperiodicposition.md)         | Devuelve la posición de hora en el intervalo de tiempo local de un conjunto de animaciones.<br/>      |
| [**GetSRT**](id3dxanimationset--getsrt.md)                                   | Obtiene los valores de escala, rotación y traslación del conjunto de animaciones.<br/> |



 

## <a name="remarks"></a>Observaciones

Un conjunto de animaciones consta de animaciones para muchos nodos de la misma animación.

El tipo LPD3DXANIMATIONSET se define como un puntero a esta interfaz.


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
