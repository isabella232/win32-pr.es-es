---
description: Obtiene un conjunto de animaciones.
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: Método ID3DXAnimationController::GetAnimationSet (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569932"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a>Método ID3DXAnimationController::GetAnimationSet

Obtiene un conjunto de animaciones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice del conjunto de animaciones.

</dd> <dt>

*ppAnimSet* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

Puntero al conjunto [**de animaciones ID3DXAnimationSet.**](id3dxanimationset.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

El controlador de animación contiene una matriz de conjuntos de animación. Este método devuelve uno de ellos en el índice especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
