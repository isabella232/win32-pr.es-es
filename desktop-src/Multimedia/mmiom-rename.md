---
title: MMIOM_RENAME mensaje (Mmsystem.h)
description: La función mmioRename envía el mensaje RENAME de MMIOM a un procedimiento de E/S para solicitar que se cambie el nombre del \_ archivo especificado.
ms.assetid: 38a746c8-3a6f-4cb2-a5b4-c11bd1e73c8a
keywords:
- MMIOM_RENAME mensaje Windows Multimedia
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
ms.openlocfilehash: bcfd90b53f1cc42030bd00e6553d52de0f036ff274b3d4ff942c48667e4347b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065315"
---
# <a name="mmiom_rename-message"></a>Mensaje DE CAMBIO DE \_ NOMBRE DE MMIOM

La función [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename) envía el mensaje RENAME de **MMIOM \_** a un procedimiento de E/S para solicitar que se cambie el nombre del archivo especificado.


```C++
MMIOM_RENAME 
lParam1 = (LPARAM) lpszOldFilename 
lParam2 = (LPARAM) lpszNewFilename 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpszOldFilename"></span><span id="lpszoldfilename"></span><span id="LPSZOLDFILENAME"></span>*lpszOldFilename*
</dt> <dd>

Puntero a una cadena que contiene el nombre de archivo del archivo cuyo nombre se debe cambiar.

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
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

