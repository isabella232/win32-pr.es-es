---
description: Indica que el conjunto disponible de métodos de interfaz IDvdControl2 ha cambiado.
ms.assetid: dfe698b9-abe5-44a7-9844-f408f11fd0ce
title: EC_DVD_VALID_UOPS_CHANGE (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VALID_UOPS_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 26ab0674b504fac3fe374247f47ca20496b22ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653493"
---
# <a name="ec_dvd_valid_uops_change"></a>\_cambio de \_ \_ UOPS válido de DVD \_ de EC

Indica que el conjunto disponible de métodos de interfaz [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) ha cambiado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Valor **DWORD** que contiene una combinación de cero o más marcas de la enumeración de [**\_ \_ marcas UOP válidas**](/windows/win32/api/strmif/ne-strmif-valid_uop_flag) . Los bits indican qué comandos de [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) se deshabilitaron explícitamente en el disco DVD.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este evento indica únicamente las operaciones que el contenido del disco DVD deshabilita explícitamente. No garantiza que sea válido para llamar a métodos que no estén deshabilitados. Por ejemplo, si no hay botones presentes, el método [**IDvdControl2:: ActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-activatebutton) no funcionará, aunque el método no esté deshabilitado explícitamente.

Este evento se desencadena en todos los dominios.

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

 

 




