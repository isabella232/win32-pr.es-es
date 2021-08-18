---
description: Establece claves de evento de combinación para la pista de animación especificada.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: Método ID3DXAnimationController::KeyPriorityBlend (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.KeyPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33d2b4e18fc93dff3054a98442c86a4c05467898afe09fc3bc82ccbd2f0ba456
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279045"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>Método ID3DXAnimationController::KeyPriorityBlend

Establece claves de evento de combinación para la pista de animación especificada.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE KeyPriorityBlend(
  [in] FLOAT               NewBlendWeight,
  [in] DOUBLE              StartTime,
  [in] DOUBLE              Duration,
  [in] D3DXTRANSITION_TYPE Transition
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewBlendWeight* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Número entre 0 y 1 que se usa para combinar pistas.

</dd> <dt>

*StartTime* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Hora global para iniciar la mezcla.

</dd> <dt>

*Duración* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Duración de tiempo global de la mezcla.

</dd> <dt>

*Transición* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md)**

Especifica el tipo de transición utilizado para la duración de la mezcla. Vea [**D3DXTRANSITION \_ TYPE**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento de combinación de prioridad. **Se** devuelve NULL si uno o varios de los parámetros de entrada no son válidos o no hay ningún evento gratuito disponible.

## <a name="remarks"></a>Comentarios

El controlador de animación se combina en tres fases: las pistas de prioridad baja se mezclan primero, las pistas de alta prioridad se mezclan en segundo lugar y, a continuación, se mezclan los resultados de ambos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
