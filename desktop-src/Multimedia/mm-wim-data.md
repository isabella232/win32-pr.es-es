---
title: Mensaje de MM_WIM_DATA (mmsystem. h)
description: El \_ mensaje de datos Wim de mm \_ se envía a una ventana cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a la aplicación. El mensaje se puede enviar cuando el búfer esté lleno o después de que se llame a la función waveInReset.
ms.assetid: 14298153-ea2f-40b7-bca7-196f4e6c1155
keywords:
- Mensaje de MM_WIM_DATA de Windows multimedia
topic_type:
- apiref
api_name:
- MM_WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c663d669635116500bc8aa7e7fdc994cdccd6dfe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686197"
---
# <a name="mm_wim_data-message"></a>\_Mensaje de \_ datos Wim mm

El mensaje de **\_ \_ datos Wim de mm** se envía a una ventana cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a la aplicación. El mensaje se puede enviar cuando el búfer esté lleno o después de que se llame a la función [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .


```C++
MM_WIM_DATA 
wParam = (WPARAM) hInputDev 
lParam = (LONG) lpwvhdr 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="hInputDev"></span><span id="hinputdev"></span><span id="HINPUTDEV"></span>*hInputDev*
</dt> <dd>

Identificador del dispositivo de entrada de onda-audio que recibió los datos.

</dd> <dt>

<span id="lpwvhdr"></span><span id="LPWVHDR"></span>*lpwvhdr*
</dt> <dd>

Puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer que contiene los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Es posible que el búfer devuelto no esté lleno. Use el miembro **dwBytesRecorded** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) especificada por *lParam* para determinar el número de bytes grabados en el búfer devuelto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Audio de onda](waveform-audio.md)
</dt> <dt>

[Mensajes de onda](waveform-messages.md)
</dt> </dl>

 

