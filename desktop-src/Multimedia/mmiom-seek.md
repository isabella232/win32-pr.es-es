---
title: Mensaje de MMIOM_SEEK (mmsystem. h)
description: La \_ función mmioSeek envía el mensaje de búsqueda MMIOM a un procedimiento de e/s para solicitar que se mueva la posición del archivo actual.
ms.assetid: 428b231a-6e00-4458-9ba2-e9b0b028843a
keywords:
- Mensaje de MMIOM_SEEK de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686196"
---
# <a name="mmiom_seek-message"></a>MMIOM \_ Buscar mensaje

La función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) envía el mensaje de **\_ búsqueda MMIOM** a un procedimiento de e/s para solicitar que se mueva la posición del archivo actual.


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

Marca que especifica cómo se cambia la posición del archivo. Se definen los valores siguientes:



| Requisito | Value |
|-----------|------------------------------------------------------------------------------------------------------------------------|
| BUSCAR \_ CUR | Mueva la posición del archivo a *lNewFilePos* bytes desde la posición actual. *lNewFilePos* puede ser positivo o negativo. |
| fin de búsqueda \_ | Mueva la posición del archivo a *lNewFilePos* bytes desde el final del archivo.                                             |
| conjunto de búsqueda \_ | Mueva la posición del archivo a *lNewFilePos* bytes desde el principio del archivo.                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la nueva posición del archivo. Si hay un error, el valor devuelto es 1.

## <a name="remarks"></a>Observaciones

El procedimiento de e/s es responsable de mantener la posición del archivo actual en el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

