---
description: Establece el peso de la pista. El peso se usa para determinar cómo combinar varias pistas.
ms.assetid: a00ceae4-47b4-4fb9-a028-97493e3dc071
title: Método ID3DXAnimationController::SetTrackWeight (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dc42d283231a0e49359531827cc785bd83aefc2b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888545"
---
# <a name="id3dxanimationcontrollersettrackweight-method"></a>Método ID3DXAnimationController::SetTrackWeight

Establece el peso de la pista. El peso se usa para determinar cómo combinar varias pistas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTrackWeight(
  [in] UINT  Track,
  [in] FLOAT Weight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de la pista en la que se establecerá el peso.

</dd> <dt>

*Peso* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Valor de peso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
