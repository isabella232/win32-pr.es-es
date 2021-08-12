---
description: Aplica el conjunto de animación a la pista especificada.
ms.assetid: f48bb0f1-3ccd-4db9-8a30-58c79ae0939e
title: Método ID3DXAnimationController::SetTrackAnimationSet (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a94fee2a0bd80f391b514895aa5b5348cbef6d8a53e31200b49a403a6712e2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118296888"
---
# <a name="id3dxanimationcontrollersettrackanimationset-method"></a>Método ID3DXAnimationController::SetTrackAnimationSet

Aplica el conjunto de animación a la pista especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTrackAnimationSet(
  [in] UINT               Track,
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de la pista a la que se aplica el conjunto de animaciones.

</dd> <dt>

*pAnimSet* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Puntero a la [**animación ID3DXAnimationSet**](id3dxanimationset.md) establecida para agregarse a la pista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Este método establece el conjunto de animación en la pista especificada para la combinación. El conjunto de animación para cada pista se combina según el peso y la velocidad de la pista cuando se llama a [**AdvanceTime.**](id3dxanimationcontroller--advancetime.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
