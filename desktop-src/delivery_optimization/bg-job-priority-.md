---
title: BG_JOB_PRIORITY enumeración (Deliveryoptimization.h)
description: La BG_JOB_PRIORITY enumeración define los valores constantes que especifican el nivel de prioridad de un trabajo.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- BG_JOB_PRIORITY enumeración
- BG_JOB_PRIORITY enumeración
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964007"
---
# <a name="bg_job_priority-enumeration"></a>BG_JOB_PRIORITY enumeración

La **BG_JOB_PRIORITY** enumeración define los valores constantes que especifican el nivel de prioridad de un trabajo.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**
</dt> <dd>

Transfiere el trabajo en primer plano. Las transferencias en primer plano compiten por el ancho de banda de red con otras aplicaciones, lo que puede impedir la experiencia de red del usuario. Este es el nivel de prioridad más alto.

</dd> <dt>

<span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**
</dt> <dd>

Transfiere el trabajo en segundo plano. Las transferencias en segundo plano usan un pequeño porcentaje de ancho de banda de red.

</dd> <dt>

<span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**
</dt> <dd>

El comportamiento de DO es el mismo para todos los trabajos que no son de primer plano. Consulte los comentarios en BG_JOB_PRIORITY_HIGH para obtener más información.

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

El comportamiento de DO es el mismo para todos los trabajos que no son de primer plano. Consulte los comentarios en BG_JOB_PRIORITY_HIGH para obtener más información.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se pueden realizar varias transferencias en primer plano y en segundo plano simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IBackgroundCopyJob::GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**IBackgroundCopyJob::SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





