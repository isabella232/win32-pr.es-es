---
description: Establece una clave de evento que cambia el peso de una pista de animación. El peso se usa como multiplicador al combinar varias pistas.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: Método ID3DXAnimationController::KeyTrackWeight (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackWeight
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 74f5e38392f6b4ac192f02b9d85421c8357a16ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964884"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a>Método ID3DXAnimationController::KeyTrackWeight

Establece una clave de evento que cambia el peso de una pista de animación. El peso se usa como multiplicador al combinar varias pistas.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE KeyTrackWeight(
  [in] UINT                Track,
  [in] FLOAT               NewWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Identificador de la pista que se modificará.

</dd> <dt>

*NewWeight* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Nuevo peso de la pista.

</dd> <dt>

*StartTime* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Clave de hora global. Especifica la hora global en la que se llevará a cabo el cambio.

</dd> <dt>

*Duración* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Tiempo de transición, que especifica cuánto tiempo se tardará en completarse la transición sin problemas.

</dd> <dt>

*Transición* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

Especifica el tipo de transición utilizado para la transición entre pesos. Vea [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento de combinación de prioridad. **Se** devuelve NULL si uno o varios de los parámetros de entrada no son válidos o no hay ningún evento gratuito disponible.

## <a name="remarks"></a>Observaciones

El peso se usa como un multiplicador para determinar la cantidad de esta pista que se va a combinar con otras pistas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
