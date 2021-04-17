---
title: Mensaje de MM_MOM_OPEN (mmsystem. h)
description: El \_ mensaje abierto de MOM de mm \_ se envía a una ventana cuando se abre un dispositivo de salida MIDI.
ms.assetid: 1374a07c-02fa-4b43-82df-cbd96302aec5
keywords:
- Mensaje de MM_MOM_OPEN de Windows multimedia
topic_type:
- apiref
api_name:
- MM_MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f676dccf532290ab2153b888c20fad7b19d98d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488969"
---
# <a name="mm_mom_open-message"></a>\_Mensaje abierto de MOM de mm \_

El **mensaje \_ \_ abierto de MOM de mm** se envía a una ventana cuando se abre un dispositivo de salida MIDI.


```C++
MM_MOM_OPEN 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Identificador del dispositivo de salida MIDI.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Sector No use.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes MIDI](midi-messages.md)
</dt> </dl>

 

 





