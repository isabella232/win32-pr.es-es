---
title: MMIOM_WRITEFLUSH mensaje (Mmsystem.h)
description: La función mmioWrite envía el mensaje WRITEFLUSH de MMIOM a un procedimiento de E/S para solicitar que los datos se escriban en un archivo abierto y que todos los búferes internos utilizados por el procedimiento de E/S se vacíe en el \_ disco.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- MMIOM_WRITEFLUSH mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MMIOM_WRITEFLUSH
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b294d4c461970a3304f09088cf63a6564acd50c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371114"
---
# <a name="mmiom_writeflush-message"></a>Mensaje WRITEFLUSH de MMIOM \_

La función [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) envía el mensaje **\_ WRITEFLUSH de MMIOM** a un procedimiento de E/S para solicitar que los datos se escriban en un archivo abierto y que todos los búferes internos utilizados por el procedimiento de E/S se vacíe en el disco.


```C++
MMIOM_WRITEFLUSH 
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

## <a name="remarks"></a>Observaciones

El procedimiento de E/S es responsable de actualizar el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) para reflejar la nueva posición del archivo después de la operación de escritura.

Este mensaje es equivalente al mensaje WRITE de [**MMIOM, \_**](mmiom-write.md) salvo que solicita que el procedimiento de E/S vacíe sus búferes internos, si los hubiera. A menos que un procedimiento de E/S realice el almacenamiento en búfer interno, este mensaje se puede controlar exactamente igual que el **mensaje WRITE \_ de MMIOM.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



 

