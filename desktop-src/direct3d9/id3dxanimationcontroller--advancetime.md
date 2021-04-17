---
description: Anima la malla y avanza el tiempo de animación global en una cantidad especificada.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'ID3DXAnimationController:: AdvanceTime (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698388"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a>ID3DXAnimationController:: AdvanceTime (método)

Anima la malla y avanza el tiempo de animación global en una cantidad especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TimeDelta* \[ de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Cantidad, en segundos, por la que se va a avanzar el tiempo de animación global. El valor de TimeDelta debe ser no negativo o cero.

</dd> <dt>

*pCallbackHandler* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**

Puntero a una interfaz de controlador de devolución de llamada de animación definida por el usuario, [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
