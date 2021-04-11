---
description: Establece una clave de evento que cambia la hora local de una pista de animación.
ms.assetid: b527e960-8ab9-42a0-bb4d-bea5aaf83424
title: 'ID3DXAnimationController:: KeyTrackPosition (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d027069efa9fb49cad3d2344da593eae4c3c844c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362701"
---
# <a name="id3dxanimationcontrollerkeytrackposition-method"></a>ID3DXAnimationController:: KeyTrackPosition (método)

Establece una clave de evento que cambia la hora local de una pista de animación.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE KeyTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE NewPosition,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de la pista que se va a modificar.

</dd> <dt>

*NewPosition* \[ de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Nueva hora local de la pista de animación.

</dd> <dt>

*StartTime* \[ de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Clave de tiempo global. Especifica la hora global a la que se llevará a cabo el cambio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento de mezcla de prioridad. Se devuelve **null** si Track no es válido o si no hay ningún evento Free disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
