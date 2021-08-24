---
title: Método IRDVTaskPluginNotifySink ScheduleTask
description: Lo llama el agente de tareas para programar una tarea.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- Método ScheduleTask Servicios de Escritorio remoto
- Método ScheduleTask Servicios de Escritorio remoto , interfaz IRDVTaskPluginNotifySink
- Interfaz IRDVTaskPluginNotifySink Servicios de Escritorio remoto método , ScheduleTask
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fdcecba38b1fd5eb773e5076f5485ae900e5423267a3a311091bf01e0ed86ac0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512025"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>IrDVTaskPluginNotifySink::ScheduleTask (método)

Lo llama el agente de tareas para programar una tarea.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ScheduleTask(
  [in] FILETIME        ftStartTime,
  [in] FILETIME        ftEndTime,
  [in] FILETIME        ftDeadline,
  [in] BSTR            bstrLabel,
  [in] BSTR            bstrIdentifier,
  [in] SAFEARRAY(BYTE) saContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ftStartTime* \[ En\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

La hora de inicio de la tarea más temprana, en UTC.

</dd> <dt>

*ftEndTime* \[ En\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Hora de finalización de la tarea, en UTC. Pase un [**conjunto FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) a todos los ceros si no se especifica ninguna hora de finalización.

</dd> <dt>

*ftDeadline* \[ En\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Fecha límite de la tarea, en FORMATO UTC. Esto se usa para establecer la prioridad de varias tareas que se encuentran dentro de su ventana de inicio. Si se debe iniciar más de una tarea, primero se inicia la que tenga la fecha límite más temprana.

</dd> <dt>

*bstrLabel* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Etiqueta de la tarea. Esto se pasa al [**método StartTask.**](irdvtaskplugin-starttask.md)

</dd> <dt>

*bstrIdentifier* \[ En\]
</dt> <dd>

Tipo: **BSTR**

Identificador único de la tarea. Esto se pasa al [**método StartTask.**](irdvtaskplugin-starttask.md)

</dd> <dt>

*saContext* \[ En\]
</dt> <dd>

Tipo: **SAFEARRAY(BYTE)**

Datos opcionales para la tarea. Esto se pasa al [**método StartTask.**](irdvtaskplugin-starttask.md)

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

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

