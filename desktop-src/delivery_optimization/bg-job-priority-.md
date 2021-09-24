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
ms.openlocfilehash: 252b7a8843c4bd7b0a45dbc7cfef235ac5303ea5
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521039"
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

Optimización de distribución comportamiento es el mismo para todos los trabajos que no están en primer plano. Consulte los comentarios en BG_JOB_PRIORITY_HIGH para obtener más información.

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

Optimización de distribución comportamiento es el mismo para todos los trabajos que no están en primer plano. Consulte los comentarios en BG_JOB_PRIORITY_HIGH para obtener más información.

</dd> </dl>

## <a name="remarks"></a>Comentarios

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

 

 





