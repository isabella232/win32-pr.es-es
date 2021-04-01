---
title: IRDVTaskPluginNotifySink ScheduleTask (método)
description: Llamado por el agente de tareas para programar una tarea.
ms.assetid: 06793439-cf16-40ca-8a91-08acc22c73ed
ms.tgt_platform: multiple
keywords:
- ScheduleTask (método) Servicios de Escritorio remoto
- Método ScheduleTask Servicios de Escritorio remoto, interfaz IRDVTaskPluginNotifySink
- IRDVTaskPluginNotifySink interface Servicios de Escritorio remoto, ScheduleTask (método)
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.ScheduleTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9bde92992eec9c4ab3d4151c59e6d687ec2f3fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905597"
---
# <a name="irdvtaskpluginnotifysinkscheduletask-method"></a>IRDVTaskPluginNotifySink:: ScheduleTask (método)

Llamado por el agente de tareas para programar una tarea.

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

*ftStartTime* \[ de\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

La hora de inicio de la tarea más temprana, en formato UTC.

</dd> <dt>

*ftEndTime* \[ de\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Hora de finalización de la tarea, en formato UTC. Pasar un valor de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) a ceros si no se especifica ninguna hora de finalización.

</dd> <dt>

*ftDeadline* \[ de\]
</dt> <dd>

Tipo: **[ **FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)**

Fecha límite de la tarea, en UTC. Se usa para establecer la prioridad de varias tareas que se encuentran dentro de su ventana de inicio. Si se debe iniciar más de una tarea, primero se iniciará la que tenga la fecha límite más temprana.

</dd> <dt>

*bstrLabel* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Etiqueta de la tarea. Se pasa al método [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*bstrIdentifier* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Identificador único de la tarea. Se pasa al método [**StartTask**](irdvtaskplugin-starttask.md) .

</dd> <dt>

*saContext* \[ de\]
</dt> <dd>

Tipo: **SAFEARRAY (byte)**

Datos opcionales para la tarea. Se pasa al método [**StartTask**](irdvtaskplugin-starttask.md) .

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

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

