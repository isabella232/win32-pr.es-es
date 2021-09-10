---
title: MM_WOM_DONE mensaje (Mmsystem.h)
description: El mensaje MM WOM DONE se envía a una ventana cuando se devuelve el búfer de salida \_ \_ dado a la aplicación. Los búferes se devuelven a la aplicación cuando se han reproducido o como resultado de una llamada a la función waveOutReset.
ms.assetid: bbdebb68-82e5-4963-90bb-f93f8a91a8cf
keywords:
- MM_WOM_DONE mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_WOM_DONE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7198aa2f60a7f5a0e6d839a3ee5b453a3a4d3f59
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371240"
---
# <a name="mm_wom_done-message"></a>MENSAJE \_ DE MM WOM \_ DONE

El **mensaje \_ MM WOM \_ DONE** se envía a una ventana cuando se devuelve el búfer de salida dado a la aplicación. Los búferes se devuelven a la aplicación cuando se han reproducido o como resultado de una llamada a la [**función waveOutReset.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)


```C++
MM_WOM_DONE 
wParam = (WPARAM) hOutputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Identificador del dispositivo de salida de audio de forma de onda que reproducía el búfer.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Puntero a una [**estructura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer.

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

[Audio de forma de onda](waveform-audio.md)
</dt> <dt>

[Mensajes de forma de onda](waveform-messages.md)
</dt> </dl>

 

