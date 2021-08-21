---
title: MMIOM_WRITE mensaje (Mmsystem.h)
description: La función mmioWrite envía el mensaje MMIOM WRITE a un procedimiento de E/S para solicitar que los datos se escriban \_ en un archivo abierto.
ms.assetid: 46e2dd9a-c4a7-4c99-86e4-a67b424411d1
keywords:
- MMIOM_WRITE mensaje Windows Multimedia
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
ms.openlocfilehash: 755b89d7e268e266b4761142dc3820bdd4d33d4bd4d86522ce5363b95e5be282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065275"
---
# <a name="mmiom_write-message"></a>MMIOM \_ WRITE message

La función [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) envía el mensaje **\_ MMIOM WRITE** a un procedimiento de E/S para solicitar que los datos se escriban en un archivo abierto.


```C++
MMIOM_WRITE 
lParam1 = (LPARAM) lpBuffer 
lParam2 = (LPARAM) cbWrite 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lpBuffer"></span><span id="lpbuffer"></span><span id="LPBUFFER"></span>*lpBuffer*
</dt> <dd>

Puntero a un búfer que contiene los datos que se escribirán en el archivo.

</dd> <dt>

<span id="cbWrite"></span><span id="cbwrite"></span><span id="CBWRITE"></span>*cbWrite*
</dt> <dd>

Número de bytes que se escribirán en el archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de bytes escritos realmente en el archivo. Si se produce un error, el valor devuelto es 1.

## <a name="remarks"></a>Comentarios

El procedimiento de E/S es responsable de actualizar el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para reflejar la nueva posición del archivo después de la operación de escritura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

