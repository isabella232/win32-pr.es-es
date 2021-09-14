---
description: Quita todos los eventos de una pista de animación especificada.
ms.assetid: 25c4d04a-0d75-4113-ad90-db84aa937098
title: Método ID3DXAnimationController::UnkeyAllTrackEvents (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnkeyAllTrackEvents
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5904e9e09c8a821cdc532f9046217ae64bbf3de5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964855"
---
# <a name="id3dxanimationcontrollerunkeyalltrackevents-method"></a>Método ID3DXAnimationController::UnkeyAllTrackEvents

Quita todos los eventos de una pista de animación especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnkeyAllTrackEvents(
  [in] UINT Track
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de la pista en la que se deben quitar todos los eventos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método evita la ejecución de todos los eventos programados previamente en la pista y descarta todos los datos asociados a esos eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
