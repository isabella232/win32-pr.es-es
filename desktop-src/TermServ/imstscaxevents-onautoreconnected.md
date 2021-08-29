---
title: Método IMsTscAxEvents OnAutoReconnected
description: Se llama cuando el control de cliente se ha vuelto a conectar automáticamente a una sesión remota. | Método IMsTscAxEvents OnAutoReconnected
ms.assetid: 50307002-33F9-453C-A880-AF4111412854
ms.tgt_platform: multiple
keywords:
- Método OnAutoReconnected Servicios de Escritorio remoto
- Método OnAutoReconnected Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto , método OnAutoReconnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df16cbb2976bdbf5518a56bc90e4978772deb81608d5d24fba5516f9f538d6dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125205"
---
# <a name="imstscaxeventsonautoreconnected-method"></a>Método IMsTscAxEvents::OnAutoReconnected

Se llama cuando el control de cliente se ha vuelto a conectar automáticamente a una sesión remota.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnAutoReconnected();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





