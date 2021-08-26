---
description: Habilita o deshabilita una pista en el controlador de animación.
ms.assetid: 8d06287b-e076-4553-962c-5c423e355101
title: Método ID3DXAnimationController::SetTrackEnable (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61078a40e13ee1422c29de091e1758444e2bafa1586bb443e763e50d57457ad5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026585"
---
# <a name="id3dxanimationcontrollersettrackenable-method"></a>Método ID3DXAnimationController::SetTrackEnable

Habilita o deshabilita una pista en el controlador de animación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTrackEnable(
  [in] UINT Track,
  [in] BOOL Enable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de la pista que se va a mezclar.

</dd> <dt>

*Habilitar* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Habilite el valor. Establezca en **TRUE** para habilitar esta pista en el controlador o en **FALSE** para evitar que se mezcle.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Para mezclar una pista con otras pistas, la marca Habilitar debe establecerse en **TRUE.** Por el contrario, establecer la marca en **FALSE** impedirá que la pista se mezcle con otras pistas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
