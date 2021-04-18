---
description: Establece el peso de fusión de la prioridad usado por el controlador de animación.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'ID3DXAnimationController:: SetPriorityBlend (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718410"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a>ID3DXAnimationController:: SetPriorityBlend (método)

Establece el peso de fusión de la prioridad usado por el controlador de animación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BlendWeight* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Peso de fusión de prioridad usado por el controlador de animación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

El peso de la mezcla se usa para fusionar las pistas de prioridad alta y baja.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
