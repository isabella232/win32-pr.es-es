---
description: Se ha producido un error de dispositivo en un filtro de representador de audio.
ms.assetid: 60e36476-f553-468d-a28d-351fdf4a02f1
title: EC_SNDDEV_OUT_ERROR (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eefe6dbe57b26bf167a7fbc668010930bacffc321d42d2847ae6776696e009fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792415"
---
# <a name="ec_snddev_out_error"></a>\_ERROR DE SALIDA DE SNDDEV DE \_ \_ EC

Se ha producido un error de dispositivo en un filtro de representador de audio.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor DWORD del tipo enumerado ERR de [**SNDDEV, \_**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) que indica cómo se accede al dispositivo cuando se produjo el error.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor DWORD que indica el error devuelto por la llamada de dispositivo de sonido.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




