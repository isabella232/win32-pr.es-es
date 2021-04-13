---
description: Establece una clave de evento que habilita o deshabilita una pista de animación.
ms.assetid: de81e646-0b94-40d3-89c2-060d118d17b2
title: 'ID3DXAnimationController:: KeyTrackEnable (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackEnable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f22c732ff57e948ebcc2e89d790d352e4dc057ba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362450"
---
# <a name="id3dxanimationcontrollerkeytrackenable-method"></a>ID3DXAnimationController:: KeyTrackEnable (método)

Establece una clave de evento que habilita o deshabilita una pista de animación.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE KeyTrackEnable(
  [in] UINT   Track,
  [in] BOOL   NewEnable,
  [in] DOUBLE StartTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de la pista de animación que se va a modificar.

</dd> <dt>

*NewEnable* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Habilitar marca. Establézcalo en **true** para habilitar la pista de animación o en **false** para deshabilitar la pista.

</dd> <dt>

*StartTime* \[ de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Clave de tiempo global. Especifica la hora global a la que se llevará a cabo el cambio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento de mezcla de prioridad. Se devuelve **null** si Track no es válido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
