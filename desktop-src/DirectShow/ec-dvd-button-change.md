---
description: Indica que el número de botones de menú de DVD ha cambiado o que la selección del botón ha cambiado.
ms.assetid: af6c841d-ca06-4535-b418-14409fa78c81
title: EC_DVD_BUTTON_CHANGE (Dvdevcode.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BUTTON_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 8647c1100e5cca6897e2068b2a20119a8f047396
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061178"
---
# <a name="ec_dvd_button_change"></a>CAMBIO \_ DEL BOTÓN DE DVD DE \_ \_ EC

Indica que el número de botones de menú de DVD ha cambiado o que la selección del botón ha cambiado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**Valor DWORD** que indica el número de botones disponibles.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**Valor DWORD** que indica el número de botón seleccionado actualmente. El número de botón seleccionado cero implica que no se ha seleccionado ningún botón.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los números de botón oscilan entre 1 y 36.

El botón seleccionado actualmente puede cambiar automáticamente con un comando de navegación creado en el disco, así como mediante el control de aplicación mediante la [**interfaz IDvdControl2.**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2)

Este evento puede indicar cualquiera de los números de botón disponibles. Estos números no siempre se corresponden con los números de botón usados para [**IDvdControl2::SelectAndActivateButton**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectandactivatebutton) porque ese método solo puede activar un subconjunto de botones.

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

 

 




