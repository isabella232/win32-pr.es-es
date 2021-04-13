---
title: Mensaje de MM_MCISIGNAL (mmsystem. h)
description: El \_ mensaje mm MCISIGNAL se envía a una ventana para notificar a una aplicación que un dispositivo MCI ha alcanzado una posición definida en un comando de señal anterior (señal de MCI \_ ).
ms.assetid: 12512d23-9a89-4e38-9ec5-88845766f4f6
keywords:
- Mensaje de MM_MCISIGNAL de Windows multimedia
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422494"
---
# <a name="mm_mcisignal-message"></a>\_Mensaje MCISIGNAL mm

El mensaje **mm \_ MCISIGNAL** se envía a una ventana para notificar a una aplicación que un dispositivo MCI ha alcanzado una posición definida en un comando de [**señal**](signal.md) anterior ( [**\_ señal de MCI**](mci-signal.md)).


```C++
MM_MCISIGNAL 
wParam = (WPARAM) wID      
lParam = (LONG) lUserParm  
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="wID"></span><span id="wid"></span><span id="WID"></span>*wID*
</dt> <dd>

Identificador del dispositivo que inicia el mensaje de señal.

</dd> <dt>

<span id="lUserParm"></span><span id="luserparm"></span><span id="LUSERPARM"></span>*lUserParm*
</dt> <dd>

Valor pasado en el miembro **dwUserParm** de la estructura de parámetros de **señal de MCI \_ \_ \_ DGV** cuando el comando **Signal** ha definido esta función de devolución de llamada. Como alternativa, podría contener el valor de la posición.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Mensajes de MCI](mci-messages.md)
</dt> <dt>

[**marcar**](signal.md)
</dt> </dl>

 

 





