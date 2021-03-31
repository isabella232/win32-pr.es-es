---
description: La \_ estructura Job info \_ 3 se usa para vincular un conjunto de trabajos de impresión.
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: Estructura de JOB_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279024"
---
# <a name="job_info_3-structure"></a>Estructura de información de trabajo \_ \_ 3

La estructura **Job \_ info \_ 3** se usa para vincular un conjunto de trabajos de impresión.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a>Miembros

<dl> <dt>

**JobId**
</dt> <dd>

Identificador del trabajo de impresión.

</dd> <dt>

**NextJobId**
</dt> <dd>

Identificador del trabajo de impresión para el siguiente trabajo de impresión en el conjunto vinculado de trabajos de impresión.

</dd> <dt>

**Reserved**
</dt> <dd>

Este valor está reservado para uso futuro. Debe establecerlo en cero.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Impresión](printdocs-printing.md)
</dt> <dt>

[Estructuras de API del administrador de trabajos de impresión](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 




