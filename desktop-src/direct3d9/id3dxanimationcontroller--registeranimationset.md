---
description: Agrega un conjunto de animaciones al controlador de animación.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: Método ID3DXAnimationController::RegisterAnimationSet (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca70baf55a3dae19422c9026575d75f63eed4bde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964883"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a>Método ID3DXAnimationController::RegisterAnimationSet

Agrega un conjunto de animaciones al controlador de animación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAnimSet* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Puntero al conjunto [**de animación ID3DXAnimationSet**](id3dxanimationset.md) que se agregará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




