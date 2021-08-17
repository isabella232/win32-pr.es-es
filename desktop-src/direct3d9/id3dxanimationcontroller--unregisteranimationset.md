---
description: Quita un conjunto de animaciones del controlador de animación.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: Método ID3DXAnimationController::UnregisterAnimationSet (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4b2065ee9928291812b614b42137e130a7986402b25234537fc9b84fafa6f714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118522354"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a>Método ID3DXAnimationController::UnregisterAnimationSet

Quita un conjunto de animaciones del controlador de animación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAnimSet* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Puntero a la [**animación ID3DXAnimationSet**](id3dxanimationset.md) establecida para quitar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, D3DERR \_ NOTFOUND.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




