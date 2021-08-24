---
description: Establece una clave de evento que cambia la velocidad de reproducción de una pista de animación.
ms.assetid: 217d3a2d-0fb7-4995-86ec-7a4e8420e338
title: Método ID3DXAnimationController::KeyTrackSpeed (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 21ad7b0b1423a25ede319a623cad0a8b453af481d4aac5fae4e5bcce252dd31e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791195"
---
# <a name="id3dxanimationcontrollerkeytrackspeed-method"></a>Método ID3DXAnimationController::KeyTrackSpeed

Establece una clave de evento que cambia la velocidad de reproducción de una pista de animación.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE KeyTrackSpeed(
  [in] UINT                Track,
  [in] FLOAT               NewSpeed,
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

*NewSpeed* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Nueva velocidad de la pista de animación.

</dd> <dt>

*StartTime* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Clave de hora global. Especifica la hora global en la que se realizará el cambio.

</dd> <dt>

*Duración* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Tiempo de transición, que especifica cuánto tiempo llevará completarse la transición sin problemas.

</dd> <dt>

*Transición* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

Especifica el tipo de transición utilizado para la transición entre velocidades. Vea [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento de combinación de prioridad. **Se** devuelve NULL si uno o varios de los parámetros de entrada no son válidos o no hay ningún evento gratuito disponible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
