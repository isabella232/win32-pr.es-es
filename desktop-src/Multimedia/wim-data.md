---
title: WIM_DATA mensaje (Mmsystem.h)
description: El mensaje WIM DATA se envía a la función de devolución de llamada de entrada de audio de forma de onda dada cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a \_ la aplicación.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- WIM_DATA mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- WIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28bcfdd249dda5621d4914d75d3ffc7b13e4d767
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371251"
---
# <a name="wim_data-message"></a>Mensaje DE DATOS DE WIM \_

El **mensaje WIM \_ DATA** se envía a la función de devolución de llamada de entrada de audio de forma de onda dada cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a la aplicación. El mensaje se puede enviar cuando el búfer está lleno o después de llamar a [**la función waveInReset.**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Puntero a una [**estructura WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer que contiene los datos.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reservado; debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Es posible que el búfer devuelto no esté lleno. Use el **miembro dwBytesRecorded** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) especificada por *lpwvhdr* para determinar el número de bytes registrados en el búfer devuelto.

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

 

