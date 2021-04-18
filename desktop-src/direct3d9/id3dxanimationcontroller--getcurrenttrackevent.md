---
description: Devuelve un identificador de evento al evento que se está ejecutando actualmente en la pista de animación especificada.
ms.assetid: 2e3d4b85-42f0-463f-9eca-d9b1fa8932f6
title: 'ID3DXAnimationController:: GetCurrentTrackEvent (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentTrackEvent
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b00b90f6fbb3f4bb6170c8987f3634fec4bd0bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718375"
---
# <a name="id3dxanimationcontrollergetcurrenttrackevent-method"></a>ID3DXAnimationController:: GetCurrentTrackEvent (método)

Devuelve un identificador de evento al evento que se está ejecutando actualmente en la pista de animación especificada.

## <a name="syntax"></a>Sintaxis


```C++
D3DXEVENTHANDLE GetCurrentTrackEvent(
  [in] UINT           Track,
  [in] D3DXEVENT_TYPE EventType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Seguimiento* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Identificador de seguimiento.

</dd> <dt>

*EventType* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXEVENT \_ Type**](./d3dxevent-type.md)**

Tipo de evento que se va a consultar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento para el evento que se ejecuta actualmente en la pista especificada. Se devuelve **null** si no se está ejecutando ningún evento en la pista especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
