---
title: MMIOM_READ mensaje (Mmsystem.h)
description: La función mmioRead envía el mensaje MMIOM READ a un procedimiento de E/S para solicitar que se lea un número especificado de bytes de \_ un archivo abierto.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- MMIOM_READ mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_READ
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcf5bbdbb20e2bc168f93857a7d59016197ccc4142d4ba18a2e6fd80842ff06c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065355"
---
# <a name="mmiom_read-message"></a>MENSAJE DE LECTURA \_ DE MMIOM

La función [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) envía el mensaje **\_ MMIOM READ** a un procedimiento de E/S para solicitar que se lea un número especificado de bytes de un archivo abierto.


```C++
MMIOM_READ 
lParam1 = (LPARAM) lBuffer 
lParam2 = (LPARAM) cbRead 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lBuffer"></span><span id="lbuffer"></span><span id="LBUFFER"></span>*lBuffer*
</dt> <dd>

Puntero al búfer que se va a rellenar con los datos leídos del archivo.

</dd> <dt>

<span id="cbRead"></span><span id="cbread"></span><span id="CBREAD"></span>*cbRead*
</dt> <dd>

Número de bytes que se leerán del archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bytes leídos realmente del archivo. Si no se pueden leer más bytes, el valor devuelto es 0. Si se produce un error, el valor devuelto es 1.

## <a name="remarks"></a>Comentarios

El procedimiento de E/S es responsable de actualizar el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para reflejar la nueva posición del archivo después de la operación de lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

