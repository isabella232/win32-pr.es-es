---
title: MM_MCISIGNAL mensaje (Mmsystem.h)
description: El mensaje MM MCISIGNAL se envía a una ventana para notificar a una aplicación que un dispositivo MCI ha alcanzado una posición definida en un comando de señal anterior \_ (MCI \_ SIGNAL).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- MM_MCISIGNAL mensaje Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MCISIGNAL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d42d4d39f31b82c7461a5bd8d8561b0da1b6bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265948"
---
# <a name="mm_mcisignal-message"></a>Mensaje \_ MM MCISIGNAL

El **mensaje MM \_ MCISIGNAL** se envía a una ventana para notificar a una aplicación [](signal.md) que un dispositivo MCI ha alcanzado una posición definida en un comando de señal anterior [**(MCI \_ SIGNAL).**](mci-signal.md)


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*Wid*
</dt> <dd>

Identificador del dispositivo que inicia el mensaje de señal.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*
</dt> <dd>

Valor pasado en el **miembro dwUserParm** de la estructura **\_ MCI DGV \_ SIGNAL \_ PARAMS** cuando el comando **signal** ha definido esta función de devolución de llamada. Como alternativa, podría contener el valor de posición.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Mensajes de MCI](mci-messages.md)
</dt> <dt>

[**Señal**](signal.md)
</dt> </dl>

 

 





