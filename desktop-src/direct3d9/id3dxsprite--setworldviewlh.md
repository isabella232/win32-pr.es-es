---
description: Establece la transformación de vista universal que se entrega a la izquierda de un objeto Sprite. Se requiere una llamada a este método antes de la cartelera o la ordenación de los sprites.
ms.assetid: 70f1181d-41f9-4663-91e0-8df94bce4eed
title: 'ID3DXSprite:: SetWorldViewLH (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewLH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 397c3803f6d4e445f74a8b24a61e86e72e471648
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280382"
---
# <a name="id3dxspritesetworldviewlh-method"></a>ID3DXSprite:: SetWorldViewLH (método)

Establece la transformación de vista universal que se entrega a la izquierda de un objeto Sprite. Se requiere una llamada a este método antes de la cartelera o la ordenación de los sprites.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetWorldViewLH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWorld* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a un [**D3DXMATRIX**](d3dxmatrix.md) que contiene una transformación universal. Si es **null**, se utiliza la matriz de identidad para la transformación del mundo.

</dd> <dt>

*pView* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a un [**D3DXMATRIX**](d3dxmatrix.md) que contiene una transformación de vista. Si es **null**, se utiliza la matriz de identidad para la transformación de la vista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

Se requiere una llamada a este método (o a [**ID3DXSprite:: SetWorldViewRH**](id3dxsprite--setworldviewrh.md)) si el objeto Sprite se va a representar con el valor de marca D3DXSprite de la [ \_ \_ cartelera](d3dxsprite.md), D3DXSprite de \_ \_ profundidad de orden \_ \_ FRONTTOBACK o D3DXSprite \_ \_ \_ de profundidad de ordenación BACKTOFRONT \_ en [**ID3DXSprite:: Begin**](id3dxsprite--begin.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSprite](id3dxsprite.md)
</dt> </dl>

 

 




