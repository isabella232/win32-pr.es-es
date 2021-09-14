---
description: Se ha producido un error de dispositivo en un filtro de captura de audio.
ms.assetid: 13f8641b-7881-4f1c-816c-77c140e48ed4
title: EC_SNDDEV_IN_ERROR (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f9b95055483b1bda812179f1a1bf132d12de7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161502"
---
# <a name="ec_snddev_in_error"></a>ERROR \_ DE SNDDEV \_ DE \_ EC

Se ha producido un error de dispositivo en un filtro de captura de audio.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor DWORD del tipo [**enumerado \_ ERR de SNDDEV,**](/previous-versions/windows/desktop/api/audevcod/ne-audevcod-snddev_err) que indica cómo se tenía acceso al dispositivo cuando se produjo el error.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




