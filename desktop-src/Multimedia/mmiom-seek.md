---
title: MMIOM_SEEK mensaje (Mmsystem.h)
description: La función mmioSeek envía el mensaje MMIOM SEEK a un procedimiento de E/S para solicitar que se traslade la posición \_ actual del archivo.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- MMIOM_SEEK mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_SEEK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4855ec4e610f1456e1bf26ee05800e31933f05fd
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371113"
---
# <a name="mmiom_seek-message"></a>Mensaje MMIOM \_ SEEK

La función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) envía el mensaje **\_ MMIOM SEEK** a un procedimiento de E/S para solicitar que se traslade la posición actual del archivo.


```C++
MMIOM_SEEK 
lParam1 = (LPARAM) lNewFilePos 
lParam2 = (LPARAM) lChangeFlag 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lNewFilePos"></span><span id="lnewfilepos"></span><span id="LNEWFILEPOS"></span>*lNewFilePos*
</dt> <dd>

Nueva posición del archivo. El significado de este valor depende de la marca especificada en **lChangeFlag**.

</dd> <dt>

<span id="lChangeFlag"></span><span id="lchangeflag"></span><span id="LCHANGEFLAG"></span>*lChangeFlag*
</dt> <dd>

Marca que especifica cómo se cambia la posición del archivo. Se definen los siguientes valores:



| Requisito | Value |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| SEEK \_ CUR | Mueva la posición del archivo para que *sea lNewFilePos* bytes desde la posición actual. *lNewFilePos* puede ser positivo o negativo. |
| SEEK \_ END | Mueva la posición del archivo para *que sea lNewFilePos* bytes desde el final del archivo.                                             |
| SEEK \_ SET | Mueva la posición del archivo para que *sea lNewFilePos* bytes desde el principio del archivo.                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la nueva posición del archivo. Si se produce un error, el valor devuelto es 1.

## <a name="remarks"></a>Observaciones

El procedimiento de E/S es responsable de mantener la posición actual del archivo en el **miembro lDiskOffset** de la [**estructura MMIOINFO.**](/previous-versions//dd757322(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

