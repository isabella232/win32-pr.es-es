---
title: BG_FILE_PROGRESS estructura (Deliveryoptimization. h)
description: La estructura BG_FILE_PROGRESS proporciona información de progreso relacionada con archivos, como el número de bytes transferidos.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Estructura de BG_FILE_PROGRESS
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
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803301"
---
# <a name="bg_file_progress-structure"></a>Estructura de BG_FILE_PROGRESS

La estructura **BG_FILE_PROGRESS** proporciona información de progreso relacionada con archivos, como el número de bytes transferidos.

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

Tamaño del archivo en bytes. Si no puede determinar el tamaño del archivo (por ejemplo, si el archivo o el servidor no existen), el valor es DO_UNKNOWN_FILE_SIZE.

Si va a descargar intervalos de un archivo, **bytesTotal** refleja el número total de bytes que desea descargar del archivo.

</dd> <dt>

**BytesTransferred**
</dt> <dd>

Número de bytes transferidos.

</dd> <dt>

**Completado**
</dt> <dd>

En el caso de las descargas, el valor es **true** si el archivo está disponible para el usuario; de lo contrario, el valor es **false**. Los archivos están disponibles para el usuario después de llamar al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) . Si el método **Complete** genera un error transitorio, los archivos procesados antes de que se produjera el error están disponibles para el usuario; los demás no lo son. Use el miembro **completado** para determinar si el archivo está disponible para el usuario cuando se produce un error de **finalización** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para determinar si transfirió el archivo, puede:

-   Compare **BytesTransferred** con **bytesTotal**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BG_JOB_PROGRESS**](bg-job-progress.md)
</dt> <dt>

[**IBackgroundCopyFile:: GetProgress**](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





