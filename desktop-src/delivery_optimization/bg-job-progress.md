---
title: BG_JOB_PROGRESS estructura (Deliveryoptimization. h)
description: La estructura BG_JOB_PROGRESS proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos. En el caso de los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Estructura de BG_JOB_PROGRESS
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
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534935"
---
# <a name="bg_job_progress-structure"></a>Estructura de BG_JOB_PROGRESS

La estructura **BG_JOB_PROGRESS** proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos. En el caso de los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta.

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

Número total de bytes que se van a transferir para todos los archivos del trabajo. Si el valor es BG_SIZE_UNKNOWN, no se ha determinado el tamaño total de todos los archivos del trabajo. No establezca este valor si no puede determinar el tamaño de uno de los archivos. Por ejemplo, si el archivo o el servidor especificado no existe, no puede determinar el tamaño del archivo.

Si va a descargar intervalos del archivo, **bytesTotal** incluye el número total de bytes que desea descargar del archivo.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Número de bytes transferidos.

</dd> <dt>

**FilesTotal**
</dt> <dd>

Número total de archivos que se van a transferir para este trabajo.

</dd> <dt>

**FilesTransferred**
</dt> <dd>

Número de archivos transferidos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyJob:: GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





