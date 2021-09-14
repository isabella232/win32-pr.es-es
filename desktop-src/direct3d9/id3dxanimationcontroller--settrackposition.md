---
description: Establece la pista en la hora de animación local especificada.
ms.assetid: 2ce87b06-1196-415f-958c-7bd407d6c69c
title: Método ID3DXAnimationController::SetTrackPosition (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c408a43df3047a52d93da0cca3d9b17053d320
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964864"
---
# <a name="id3dxanimationcontrollersettrackposition-method"></a>Método ID3DXAnimationController::SetTrackPosition

Establece la pista en la hora de animación local especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE Position
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de seguimiento.

</dd> <dt>

*Posición* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Valor de tiempo de animación local que se asignará a la pista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
