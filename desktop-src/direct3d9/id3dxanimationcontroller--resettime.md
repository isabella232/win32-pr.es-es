---
description: Restablece el tiempo de animación global a cero. Los eventos pendientes conservarán sus programaciones originales, pero en el nuevo período de tiempo.
ms.assetid: 70b073ec-ef97-4af4-9f42-b6a6cc13605f
title: Método ID3DXAnimationController::ResetTime (D3dx9anim.h)
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
ms.openlocfilehash: a3f5f4ba6f10d5119e479a56e9e207e410b2d1e817d6809e7ceac1c98c8d2ee5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893745"
---
# <a name="id3dxanimationcontrollerresettime-method"></a>Método ID3DXAnimationController::ResetTime

Restablece el tiempo de animación global a cero. Los eventos pendientes conservarán sus programaciones originales, pero en el nuevo período de tiempo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResetTime();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método se usa normalmente cuando el valor de tiempo de animación global se acerca a la precisión máxima del almacenamiento DOUBLE, o 2⁶⁴ - 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




