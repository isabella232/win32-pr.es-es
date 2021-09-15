---
description: Clona o copia un controlador de animación.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: Método ID3DXAnimationController::CloneAnimationController (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569929"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a>Método ID3DXAnimationController::CloneAnimationController

Clona o copia un controlador de animación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MaxNumAnimationOutputs* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de salidas de animación que el controlador puede admitir.

</dd> <dt>

*MaxNumAnimationSets* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de conjuntos de animación que el controlador puede admitir.

</dd> <dt>

*MaxNumTracks* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de pistas que el controlador puede admitir.

</dd> <dt>

*MaxNumEvents* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de eventos que el controlador puede admitir.

</dd> <dt>

*ppAnimController* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Dirección de un puntero al controlador de animación [**ID3DXAnimationController**](id3dxanimationcontroller.md) clonado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
