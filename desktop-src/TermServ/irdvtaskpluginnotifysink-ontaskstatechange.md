---
title: IRDVTaskPluginNotifySink OnTaskStateChange, método
description: Se usa para notificar al agente de desencadenador que el estado de una tarea ha cambiado.
ms.assetid: 3021ea7a-2627-48d1-8df5-c40e7a9b51c5
ms.tgt_platform: multiple
keywords:
- Método OnTaskStateChange Servicios de Escritorio remoto
- Método OnTaskStateChange Servicios de Escritorio remoto, interfaz IRDVTaskPluginNotifySink
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto, método OnTaskStateChange
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTaskStateChange
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c3e3acf1a2d47b1721ef90554f7a11714c02e6df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676957"
---
# <a name="irdvtaskpluginnotifysinkontaskstatechange-method"></a>IRDVTaskPluginNotifySink:: OnTaskStateChange (método)

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

*bstrIdentifier* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Identificador único de la tarea. Este es el identificador que se pasa al método [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*Estado* \[ de de\]
</dt> <dd>

Tipo: estado de la **[ **\_ tarea \_ RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)**

Un valor de la enumeración del [**\_ \_ Estado de la tarea RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que especifica el nuevo estado de la tarea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 Enterprise<br/>   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estado de la \_ tarea RDV \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)
</dt> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





