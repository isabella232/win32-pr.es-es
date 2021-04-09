---
title: IMsTscAxEvents OnMouseInputModeChanged, método
description: Se le llama cuando cambia el modo de entrada del mouse.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- Método OnMouseInputModeChanged Servicios de Escritorio remoto
- Método OnMouseInputModeChanged Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnMouseInputModeChanged
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
ms.openlocfilehash: 5dbfef19aa79ba634a13d92b8d11866b8016e893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150499"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a>IMsTscAxEvents:: OnMouseInputModeChanged (método)

Se le llama cuando cambia el modo de entrada del mouse.

## <a name="syntax"></a>Sintaxis


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fMouseModeRelative* \[ de\]
</dt> <dd>

Indica si el mouse está en modo relativo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Implemente este método en el receptor de eventos para recibir la notificación de que el modo de entrada del mouse ha cambiado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





