---
description: Indica cuándo cambia el número de título de DVD actual.
ms.assetid: 9888f2ec-fc2d-4d6d-a03d-b381373337eb
title: EC_DVD_TITLE_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_TITLE_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 9539d29704797b1c7b001d426250762d2ed27b3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653403"
---
# <a name="ec_dvd_title_change"></a>\_cambio de \_ título de DVD de EC \_

Indica cuándo cambia el número de título de DVD actual.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que indica el nuevo número de título.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los números de título oscilan entre 1 y 99. Este número indica el valor de TTN, que es el número de título con respecto a todo el disco, no a la TTN de VTS, \_ que es el número de título con respecto a un STB actual.

Este evento se desencadena en el dominio de título.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode. h (incluir DShow. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




