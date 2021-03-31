---
title: BG_JOB_TIMES estructura (Deliveryoptimization. h)
description: La estructura BG_JOB_TIMES proporciona marcas de tiempo relacionadas con el trabajo.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Estructura de BG_JOB_TIMES
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
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801393"
---
# <a name="bg_job_times-structure"></a>Estructura de BG_JOB_TIMES

La estructura **BG_JOB_TIMES** proporciona marcas de tiempo relacionadas con el trabajo.

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

Hora en que se creó el trabajo. La hora se especifica como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**ModificationTime**
</dt> <dd>

Hora en que el trabajo se modificó por última vez o se transfirieron bytes. La adición de archivos o la llamada a cualquiera de los métodos set de las interfaces [ * *IBackgroundCopyJob \** _](/previous-versions//mt811348(v=vs.85)) cambia este valor. Además, los cambios en el estado del trabajo y la llamada a los métodos [_ *Suspend* *](ibackgroundcopyjob-suspend.md), [**resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md)y [**Complete**](ibackgroundcopyjob-complete.md) cambian este valor. La hora se especifica como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

**TransferCompletionTime**
</dt> <dd>

Hora en que el trabajo entró en el estado BG_JOB_STATE_TRANSFERRED. La hora se especifica como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IBackgroundCopyJob::GetTimes**](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

