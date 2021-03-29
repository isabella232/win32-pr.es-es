---
title: Mensaje de MMIOM_READ (mmsystem. h)
description: La \_ función mmioRead envía el mensaje de lectura MMIOM a un procedimiento de e/s para solicitar que se lea un número especificado de bytes desde un archivo abierto.
ms.assetid: db769a68-f0ac-4a79-931e-6174e438439d
keywords:
- Mensaje de MMIOM_READ de Windows multimedia
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
ms.openlocfilehash: 5715bf8db51017c16997530256c6dfb83b3b3fc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493265"
---
# <a name="mmiom_read-message"></a>MMIOM \_ leer mensaje

La función [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) envía el mensaje de **\_ lectura MMIOM** a un procedimiento de e/s para solicitar que se lea un número especificado de bytes desde un archivo abierto.


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

Número de bytes que se van a leer del archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bytes realmente leídos del archivo. Si no se pueden leer más bytes, el valor devuelto es 0. Si hay un error, el valor devuelto es 1.

## <a name="remarks"></a>Observaciones

El procedimiento de e/s es responsable de actualizar el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para reflejar la nueva posición de archivo después de la operación de lectura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

