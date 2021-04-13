---
description: Establece las claves de evento de mezcla para la pista de animación especificada.
ms.assetid: 2023d566-1de5-465a-ad6f-04a78ac01c33
title: 'ID3DXAnimationController:: KeyPriorityBlend (método) (D3dx9anim. h)'
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
ms.openlocfilehash: 31778da9b26ddd79b5f05c69c822ed62a5b5281e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362451"
---
# <a name="id3dxanimationcontrollerkeypriorityblend-method"></a>ID3DXAnimationController:: KeyPriorityBlend (método)

Establece las claves de evento de mezcla para la pista de animación especificada.

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

*NewBlendWeight* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Número comprendido entre 0 y 1 que se usa para fusionar las pistas.

</dd> <dt>

*StartTime* \[ de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Hora global para iniciar la mezcla.

</dd> <dt>

*Duración* \[ de de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Duración global de la mezcla.

</dd> <dt>

*Transición* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXTRANSITION \_ Type**](./d3dxtransition-type.md)**

Especifica el tipo de transición que se usa para la duración de la mezcla. Consulte [**\_ tipo de D3DXTRANSITION**](./d3dxtransition-type.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento de mezcla de prioridad. Se devuelve **null** si uno o varios de los parámetros de entrada no son válidos o no hay ningún evento libre disponible.

## <a name="remarks"></a>Observaciones

El controlador de animación se mezcla en tres fases: las pistas de prioridad baja se mezclan en primer lugar, las pistas de prioridad alta se combinan en segundo y, a continuación, se combinan los resultados de ambos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
