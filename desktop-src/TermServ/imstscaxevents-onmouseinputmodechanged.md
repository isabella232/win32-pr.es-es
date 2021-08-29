---
title: Método IMsTscAxEvents OnMouseInputModeChanged
description: Se llama cuando cambia el modo de entrada del mouse.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- Método OnMouseInputModeChanged Servicios de Escritorio remoto
- Método OnMouseInputModeChanged Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnMouseInputModeChanged
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c86ce3ba30dae836077189b79553e5e39b16f53f9846f41216697d110d1dfb20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512255"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a>Método IMsTscAxEvents::OnMouseInputModeChanged

Se llama cuando cambia el modo de entrada del mouse.

## <a name="syntax"></a>Sintaxis


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fMouseModeRelative* \[ En\]
</dt> <dd>

Indica si el mouse está en modo relativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Implemente este método en el receptor de eventos para recibir la notificación de que el modo de entrada del mouse ha cambiado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





