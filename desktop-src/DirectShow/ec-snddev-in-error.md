---
description: Se ha producido un error de dispositivo en un filtro de captura de audio.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bfc65b751010288ed37fc1596e020887e6ea901c451dcdac729fe05ea33f93a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102815"
---
# <a name="ec_snddev_in_error"></a>ERROR \_ DE EC SNDDEV \_ \_

Se ha producido un error de dispositivo en un filtro de captura de audio.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor DWORD del [**tipo enumerado \_ ERR de SNDDEV,**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) que indica cómo se accedía al dispositivo cuando se produjo el error.

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

 

 




