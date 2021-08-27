---
title: BG_FILE_PROGRESS estructura (Deliveryoptimization.h)
description: La BG_FILE_PROGRESS proporciona información de progreso relacionada con el archivo, como el número de bytes transferidos.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- BG_FILE_PROGRESS estructura
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd0bec0f21fb652ccc5c8d543f04816468fff9bc28db74a68a1d05c072a895a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047253"
---
# <a name="bg_file_progress-structure"></a>BG_FILE_PROGRESS estructura

La **BG_FILE_PROGRESS** proporciona información de progreso relacionada con el archivo, como el número de bytes transferidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BytesTotal**
</dt> <dd>

Tamaño del archivo en bytes. Si DO no puede determinar el tamaño del archivo (por ejemplo, si el archivo o el servidor no existe), el valor se DO_UNKNOWN_FILE_SIZE.

Si va a descargar intervalos desde un archivo, **BytesTotal** refleja el número total de bytes que desea descargar del archivo.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Número de bytes transferidos.

</dd> <dt>

**Completado**
</dt> <dd>

En el caso de las descargas, el valor **es TRUE** si el archivo está disponible para el usuario; de lo contrario, el valor es **FALSE.** Los archivos están disponibles para el usuario después de llamar al [**método IBackgroundCopyJob::Complete.**](ibackgroundcopyjob-complete.md) Si el **método Complete** genera un error transitorio, los archivos procesados antes de que se produjo el error estarán disponibles para el usuario. los demás no lo son. Use el **miembro Completed** para determinar si el archivo está disponible para el usuario cuando se produce un error **en Complete.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para determinar si do ha transferido el archivo, puede hacer lo siguiente:

-   Compare **BytesTransferred** con **BytesTotal.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





