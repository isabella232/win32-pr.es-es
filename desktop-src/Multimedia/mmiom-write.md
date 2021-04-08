---
title: Mensaje de MMIOM_WRITE (mmsystem. h)
description: La \_ función mmioWrite envía el mensaje de escritura MMIOM a un procedimiento de e/s para solicitar que los datos se escriban en un archivo abierto.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- Mensaje de MMIOM_WRITE de Windows multimedia
topic_type:
- apiref
api_name:
- MMIOM_WRITE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c27cf96827f803608c369cc9022faa6235add9ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997009"
---
# <a name="mmiom_write-message"></a>MMIOM \_ escribir mensaje

La función [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) envía el mensaje de **\_ escritura MMIOM** a un procedimiento de e/s para solicitar que los datos se escriban en un archivo abierto.


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*
</dt> <dd>

Puntero a un búfer que contiene los datos que se van a escribir en el archivo.

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*
</dt> <dd>

Número de bytes que se van a escribir en el archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bytes realmente escritos en el archivo. Si hay un error, el valor devuelto es 1.

## <a name="remarks"></a>Observaciones

El procedimiento de e/s es responsable de actualizar el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para reflejar la nueva posición de archivo después de la operación de escritura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

