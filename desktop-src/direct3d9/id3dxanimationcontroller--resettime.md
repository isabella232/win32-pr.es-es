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
ms.openlocfilehash: 1206cc8514f3e7eb235f1072bf2a66c4b5bf1e7b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964875"
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

## <a name="remarks"></a>Observaciones

Este método se usa normalmente cuando el valor de tiempo de animación global se acerca a la precisión máxima del almacenamiento DOUBLE, o 2⁶⁴ - 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




