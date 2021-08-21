---
title: Propiedades de ITsSbTaskInfo
description: La interfaz ITsSbTaskInfo expone las siguientes propiedades.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d91b24b95b6b19cb439350c0c6823306c66a8fab5fe47f0f9e9fb739df64e3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118128074"
---
# <a name="itssbtaskinfo-properties"></a>Propiedades de ITsSbTaskInfo

La [**interfaz ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) expone las siguientes propiedades.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**Propiedad Context**](itssbtaskinfo-context.md)
</dt> <dd>

Recupera los bytes de contexto asociados a la tarea.

</dd> <dt>

[**Propiedad Deadline**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

Recupera la hora en la que se debe iniciar la tarea. Esto se usa para dar prioridad a las revisiones. La revisión con la fecha límite más temprana se iniciará primero.

</dd> <dt>

[**EndTime, propiedad**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

Recupera la última vez que el agente de tareas puede iniciar la tarea.

</dd> <dt>

[**Propiedad Identificador**](itssbtaskinfo-identifier.md)
</dt> <dd>

Recupera un GUID que el agente de tareas usa como identificador único.

</dd> <dt>

[**propiedad Etiqueta**](itssbtaskinfo-label.md)
</dt> <dd>

Recupera la etiqueta que describe el propósito de la tarea.

</dd> <dt>

[**Propiedad del complemento**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

Recupera el nombre para mostrar del agente de tareas.

</dd> <dt>

[**Propiedad StartTime**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

Recupera la primera vez que el agente de tareas puede iniciar la tarea.

</dd> <dt>

[**Propiedad Status**](itssbtaskinfo-status.md)
</dt> <dd>

Recupera un valor [**de enumeración RDV \_ TASK \_ STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) que representa el estado de la tarea.

</dd> <dt>

[**Propiedad TargetId**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

Recupera el identificador de destino.

</dd> </dl>

 

 




