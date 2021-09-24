---
title: BG_JOB_PROGRESS estructura (Deliveryoptimization.h)
description: La BG_JOB_PROGRESS proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos. Para los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- BG_JOB_PROGRESS estructura
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f948b9b1150550fad432b0b816f8d435f2af0b4d
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521182"
---
# <a name="bg_job_progress-structure"></a>BG_JOB_PROGRESS estructura

La **BG_JOB_PROGRESS** proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos. Para los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**BytesTotal**
</dt> <dd>

Número total de bytes que se transferirán para todos los archivos del trabajo. Si el valor es BG_SIZE_UNKNOWN, no se ha determinado el tamaño total de todos los archivos del trabajo. Optimización de distribución no establece este valor si no puede determinar el tamaño de uno de los archivos. Por ejemplo, si el archivo o servidor especificado no existe, Optimización de distribución puede determinar el tamaño del archivo.

Si va a descargar intervalos desde el archivo, **BytesTotal** incluye el número total de bytes que desea descargar del archivo.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Número de bytes transferidos.

</dd> <dt>

**FilesTotal**
</dt> <dd>

Número total de archivos que se transferirán para este trabajo.

</dd> <dt>

**FilesTransferred**
</dt> <dd>

Número de archivos transferidos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyJob::GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





