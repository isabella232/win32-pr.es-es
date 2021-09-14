---
description: Indica que ha cambiado el número de ángulos disponibles o que ha cambiado el número de ángulo actual.
ms.assetid: 0564b0e3-6434-448b-80fb-5362ab67fef7
title: EC_DVD_ANGLE_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_ANGLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 08914e3fcb93d38ccad25053f7c33480e900ad93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061185"
---
# <a name="ec_dvd_angle_change"></a>EC \_ DVD \_ ANGLE \_ CHANGE

Indica que ha cambiado el número de ángulos disponibles o que ha cambiado el número de ángulo actual.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valor DWORD** que indica el número de ángulos disponibles. Cuando el número de ángulos disponibles es 1, el vídeo actual no es multirelaz.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valor DWORD** que indica el número de ángulo actual.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los números angulares oscilan entre 1 y 9.

El número de ángulo actual puede cambiar automáticamente con un comando de navegación creado en el disco, así como a través del control de aplicación mediante la [**interfaz IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

Este evento se genera en todos los dominios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode.h (incluir Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




