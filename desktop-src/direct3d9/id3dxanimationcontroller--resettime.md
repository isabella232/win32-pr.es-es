---
description: Restablece el tiempo de la animación global en cero. Los eventos pendientes conservarán las programaciones originales, pero en el nuevo período de tiempo.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: 'ID3DXAnimationController:: ResetTime (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.ResetTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821303"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>ID3DXAnimationController:: ResetTime (método)

Restablece el tiempo de la animación global en cero. Los eventos pendientes conservarán las programaciones originales, pero en el nuevo período de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método se utiliza normalmente cuando el valor de tiempo de animación global está cerca de la precisión máxima del almacenamiento doble o 2 ⁶ ⁴-1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




