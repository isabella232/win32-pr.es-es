---
description: Establece una clave de evento que cambia el peso de una pista de animación. El peso se utiliza como multiplicador al combinar varias pistas.
ms.assetid: fb2859de-9e77-49dd-be48-a50e22e2fc3a
title: 'ID3DXAnimationController:: KeyTrackWeight (método) (D3dx9anim. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718416"
---
# <a name="id3dxanimationcontrollerkeytrackweight-method"></a>ID3DXAnimationController:: KeyTrackWeight (método)

Establece una clave de evento que cambia el peso de una pista de animación. El peso se utiliza como multiplicador al combinar varias pistas.

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

*Seguimiento* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de la pista que se va a modificar.

</dd> <dt>

*NewWeight* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Nuevo peso de la pista.

</dd> <dt>

*StartTime* \[ de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Clave de tiempo global. Especifica la hora global a la que se llevará a cabo el cambio.

</dd> <dt>

*Duración* \[ de de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Tiempo de transición, que especifica cuánto tiempo tardará la transición suave en completarse.

</dd> <dt>

*Transición* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ Type**](./d3dxtransition-type.md)**

Especifica el tipo de transición que se usa para realizar la transición entre pesos. Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento de mezcla de prioridad. Se devuelve **null** si uno o varios de los parámetros de entrada no son válidos o no hay ningún evento libre disponible.

## <a name="remarks"></a>Observaciones

El peso se usa como un multiplicador para determinar la cantidad de esta pista que se va a combinar con otras pistas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
