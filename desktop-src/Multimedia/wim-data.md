---
title: Mensaje de WIM_DATA (mmsystem. h)
description: El \_ mensaje de datos Wim se envía a la función de devolución de llamada de entrada de audio de forma de onda especificada cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a la aplicación.
ms.assetid: 94cc02b8-61c4-44b9-9f8e-041fe989c1a6
keywords:
- Mensaje de WIM_DATA de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676907"
---
# <a name="wim_data-message"></a>\_Mensaje de datos Wim

El mensaje de **\_ datos Wim** se envía a la función de devolución de llamada de entrada de audio de forma de onda especificada cuando los datos de audio de forma de onda están presentes en el búfer de entrada y el búfer se devuelve a la aplicación. Se puede enviar el mensaje cuando el búfer esté lleno o después de que se llame a la función [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset) .


```C++
WIM_DATA 
dwParam1 = (DWORD) lpwvhdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Puntero a una estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) que identifica el búfer que contiene los datos.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Sector debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Es posible que el búfer devuelto no esté lleno. Use el miembro **dwBytesRecorded** de la estructura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) especificada por *lpwvhdr* para determinar el número de bytes grabados en el búfer devuelto.

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

 

