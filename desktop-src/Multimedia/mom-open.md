---
title: MOM_OPEN mensaje (Mmsystem.h)
description: El mensaje MOM \_ OPEN se envía a una función de devolución de llamada de salida DE MIDI cuando se abre un dispositivo de salida DE MIDI.
ms.assetid: f3360482-7d16-419c-b5d1-0dd3a6e3c690
keywords:
- MOM_OPEN mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24072aad6bff9ce192460c2c8525da4506f32746
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371023"
---
# <a name="mom_open-message"></a>Mensaje \_ DE MOM OPEN

El **mensaje MOM \_ OPEN** se envía a una función de devolución de llamada de salida DE MIDI cuando se abre un dispositivo de salida DE MIDI.


```C++
MOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Reservado; no se usan.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reservado; no se usan.

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

 

 





