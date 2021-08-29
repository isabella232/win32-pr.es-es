---
title: Método IRDVTaskPluginNotifySink OnTaskStateChange
description: Se usa para notificar al agente de desencadenador que el estado de una tarea ha cambiado.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Método OnTaskStateChange Servicios de Escritorio remoto
- Método OnTaskStateChange Servicios de Escritorio remoto , interfaz IRDVTaskPluginNotifySink
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto , método OnTaskStateChange
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6e580a78ba14363b140d48896d63ddafaf27f5a2e64c9ff18045b007bcc8d9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129117"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a>Método IRDVTaskPluginNotifySink::OnTaskStateChange

Se usa para notificar al agente de desencadenador que el estado de una tarea ha cambiado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnTaskStateChange(
  [in] BSTR            bstrIdentifier,
  [in] RDV_TASK_STATUS status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrIdentifier* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Identificador único de la tarea. Este es el identificador que se pasa al [**método StartTask.**](irdvtaskplugin-starttask.md)

</dd> <dt>

*status* \[ En\]
</dt> <dd>

Tipo: **[ **ESTADO DE TAREA \_ RDV \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**

Valor de la [**enumeración RDV \_ TASK \_ STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que especifica el nuevo estado de la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ESTADO DE LA \_ TAREA RDV \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





