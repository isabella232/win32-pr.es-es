---
title: Mensaje de MMIOM_RENAME (mmsystem. h)
description: La \_ función mmioRename envía el mensaje de cambio de nombre MMIOM a un procedimiento de e/s para solicitar que se cambie el nombre del archivo especificado.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- Mensaje de MMIOM_RENAME de Windows multimedia
topic_type:
- apiref
api_name:
- MMIOM_RENAME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71770dec6a92693a50e8e0210da3f9b8028587c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492347"
---
# <a name="mmiom_rename-message"></a>MMIOM \_ cambiar nombre de mensaje

La función [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) envía el mensaje de **\_ cambio de nombre MMIOM** a un procedimiento de e/s para solicitar que se cambie el nombre del archivo especificado.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*
</dt> <dd>

Puntero a una cadena que contiene el nombre del archivo al que se va a cambiar el nombre.

</dd> <dt>

<span id="lpszNewFilename"></span><span id="lpsznewfilename"></span><span id="LPSZNEWFILENAME"></span>*lpszNewFilename*
</dt> <dd>

Puntero a una cadena que contiene el nuevo nombre de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se cambia el nombre del archivo correctamente, el valor devuelto es cero. Si no se encuentra el archivo especificado, el valor devuelto es MMIOERR \_ FILENOTFOUND.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

