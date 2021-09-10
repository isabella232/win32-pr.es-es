---
title: MM_MOM_DONE mensaje (Mmsystem.h)
description: El mensaje MM MOM DONE se envía a una ventana cuando se ha reproducido el búfer de flujo o exclusivo del sistema DE MIDI especificado y se devuelve \_ \_ a la aplicación.
ms.assetid: 4651d5b4-3c98-4fa7-b761-dafb30e0d31e
keywords:
- MM_MOM_DONE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ad5d4a7e91cc05aa51017cba79418b34445362
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371030"
---
# <a name="mm_mom_done-message"></a>Mensaje \_ DE MM MOM \_ DONE

El **mensaje MM MOM \_ \_ DONE** se envía a una ventana cuando se ha reproducido el búfer de flujo o exclusivo del sistema DE MIDI especificado y se devuelve a la aplicación.


```C++
MM_MOM_DONE 
wParam = (WPARAM) hOutput 
lParam = (LPARAM) lpMidiHdr 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Identificador del dispositivo de salida de MIDI que reproducía el búfer.

</dd> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Puntero a una [**estructura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes DE MIDI](midi-messages.md)
</dt> </dl>

 

