---
title: Método IRDVTaskPluginNotifySink OnTerminated (Sbtsv.h)
description: Llamado por el agente de tareas para solicitar que se cierre el agente de tareas.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Método OnTerminated Servicios de Escritorio remoto
- Método OnTerminated Servicios de Escritorio remoto , interfaz IRDVTaskPluginNotifySink
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto , método OnTerminated
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29ab2a3e8ddea5999b6d63322dbeb9fca07983e591e849f22a3e98e27c67609a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129137"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>IRDVTaskPluginNotifySink::OnTerminated (Método)

Llamado por el agente de tareas para solicitar que se cierre el agente de tareas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hr* \[ En\]
</dt> <dd>

Indica si el apagado se debe a un apagado normal o a un error. Si el apagado es normal, contiene **S \_ OK**. De lo contrario, contiene un código de error **HRESULT.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                  |
| Header<br/>                   | <dl> <dt>Sbtsv.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





