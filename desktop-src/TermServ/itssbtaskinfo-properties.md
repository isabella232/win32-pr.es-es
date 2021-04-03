---
title: Propiedades de ITsSbTaskInfo
description: La interfaz ITsSbTaskInfo expone las siguientes propiedades.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783820"
---
# <a name="itssbtaskinfo-properties"></a>Propiedades de ITsSbTaskInfo

La interfaz [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) expone las siguientes propiedades.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**Propiedad de contexto**](itssbtaskinfo-context.md)
</dt> <dd>

Recupera los bytes de contexto asociados a la tarea.

</dd> <dt>

[**Propiedad fecha límite**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

Recupera la hora en la que se debe iniciar la tarea. Se usa para priorizar las revisiones. En primer lugar, se iniciará la revisión con la fecha límite más temprana.

</dd> <dt>

[**EndTime (propiedad)**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

Recupera la hora más reciente en la que el agente de tareas puede iniciar la tarea.

</dd> <dt>

[**Propiedad Identificador**](itssbtaskinfo-identifier.md)
</dt> <dd>

Recupera un GUID que el agente de tareas usa como identificador único.

</dd> <dt>

[**propiedad Etiqueta**](itssbtaskinfo-label.md)
</dt> <dd>

Recupera la etiqueta que describe el propósito de la tarea.

</dd> <dt>

[**Propiedad de complemento**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Recupera el nombre para mostrar del agente de tareas.

</dd> <dt>

[**StartTime (propiedad)**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Recupera la hora más temprana en la que el agente de tareas puede iniciar la tarea.

</dd> <dt>

[**Propiedad Status**](itssbtaskinfo-status.md)
</dt> <dd>

Recupera un valor de enumeración de [**\_ \_ Estado de la tarea RDV**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa el estado de la tarea.

</dd> <dt>

[**Propiedad TargetId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Recupera el identificador de destino.

</dd> </dl>

 

 




