---
description: Señala una condición de advertencia de DVD.
ms.assetid: d7221e8a-089f-4eaf-a193-548709c14336
title: EC_DVD_WARNING (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_WARNING
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7f25d4565c2afeb4619f7832f6d5742e07dcca0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246464"
---
# <a name="ec_dvd_warning"></a>ADVERTENCIA \_ DE DVD DE \_ EC

Señala una condición de advertencia de DVD.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valor DWORD** que indica la condición de advertencia. Miembro del tipo de datos enumerado [**\_ DVD WARNING.**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_warning)

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Si *pParam1 es* igual a DVD WARNING Open, DVD WARNING Seek o \_ DVD WARNING \_ \_ \_ \_ \_ Read, *lParam2* contiene el último código de error devuelto de GetLastError.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dvdevcode.h (incluir Dshow.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> <dt>

[Códigos de notificación de eventos de DVD](dvd-notification-codes.md)
</dt> <dt>

[Notificación de eventos en DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




