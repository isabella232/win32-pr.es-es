---
title: Mensaje de MMIOM_WRITEFLUSH (mmsystem. h)
description: La \_ función mmioWrite envía el mensaje WRITEFLUSH MMIOM a un procedimiento de e/s para solicitar que los datos se escriban en un archivo abierto y que los búferes internos utilizados por el procedimiento de e/s se vacíen en el disco.
ms.assetid: e04acaef-9584-410c-a020-af09fb888490
keywords:
- Mensaje de MMIOM_WRITEFLUSH de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803668"
---
# <a name="mmiom_writeflush-message"></a>MMIOM \_ WRITEFLUSH

La función [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) envía el mensaje **\_ WRITEFLUSH MMIOM** a un procedimiento de e/s para solicitar que los datos se escriban en un archivo abierto y que los búferes internos utilizados por el procedimiento de e/s se vacíen en el disco.


```C++
MMIOM_WRITEFLUSH 
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

Este mensaje es equivalente al mensaje [**de \_ escritura MMIOM**](mmiom-write.md) , salvo que solicita que el procedimiento de e/s vacíe sus búferes internos, si los hay. A menos que un procedimiento de e/s realice un almacenamiento en búfer interno, este mensaje se puede controlar exactamente como el mensaje de **\_ escritura MMIOM** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



 

