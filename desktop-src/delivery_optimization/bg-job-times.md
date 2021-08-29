---
title: BG_JOB_TIMES estructura (Deliveryoptimization.h)
description: La BG_JOB_TIMES proporciona marcas de tiempo relacionadas con el trabajo.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- BG_JOB_TIMES estructura
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b0fe36c9994bc03a807ff4a575945d203b1f62391b498cca094ed8f264be684
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793414"
---
# <a name="bg_job_times-structure"></a>BG_JOB_TIMES estructura

La **BG_JOB_TIMES** proporciona marcas de tiempo relacionadas con el trabajo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a>Miembros

<dl> <dt>

**CreationTime**
</dt> <dd>

Hora en que se creó el trabajo. La hora se especifica como [FILETIME.](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

**ModificationTime**
</dt> <dd>

Hora en que se modificó por última vez el trabajo o se transfirieron bytes. La adición de archivos o la llamada a cualquiera de los métodos establecidos en las interfaces [ * *IBackgroundCopyJob \** _](/previous-versions//mt811348(v=vs.85)) cambia este valor. Además, los cambios en el estado del trabajo y la llamada a los métodos [_ *Suspend* *](ibackgroundcopyjob-suspend.md), [**Resume,**](ibackgroundcopyjob-resume.md) [**Cancel**](ibackgroundcopyjob-cancel.md) [**y Complete**](ibackgroundcopyjob-complete.md) cambian este valor. La hora se especifica como [FILETIME.](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

**TransferCompletionTime**
</dt> <dd>

Hora en que el trabajo entró en BG_JOB_STATE_TRANSFERRED estado. La hora se especifica como [FILETIME.](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob::GetTimes**](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

