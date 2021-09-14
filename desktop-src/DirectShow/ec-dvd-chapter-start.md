---
description: Indica que el reproductor de DVD inició la reproducción de un nuevo programa en el dominio DE \_ DOMINIO \_ de DVD.
ms.assetid: c0745615-d527-4d93-9118-30419c6c811e
title: EC_DVD_CHAPTER_START (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_START
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 87a4408f1631d8a23cf42e790688856d6c246393
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061177"
---
# <a name="ec_dvd_chapter_start"></a>INICIO DEL \_ CAPÍTULO DE DVD DE \_ \_ EC

Indica que el reproductor de DVD inició la reproducción de un nuevo programa en el dominio DE \_ DOMINIO \_ de DVD.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valor DWORD** que indica el nuevo número de capítulo (programa).

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Solo las películas lineales simples señalan este evento.

Este evento se genera en el dominio de título.

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
</dt> <dt>

[**ENUMERACIÓN \_ DE DOMINIO DE DVD**](/windows/win32/api/strmif/ne-strmif-dvd_domain)
</dt> </dl>

 

 




