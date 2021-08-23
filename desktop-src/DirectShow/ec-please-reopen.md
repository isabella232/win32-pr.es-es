---
description: El archivo de origen ha cambiado. La aplicación debe volver a generar el gráfico de filtros.
ms.assetid: f99df68f-d7e8-4dbf-b958-84fe3f0821f0
title: EC_PLEASE_REOPEN (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efafbcd441dc62b48612e325a3520f9b3cfbdeb9b3b4d5b11144e12f9f22acd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686185"
---
# <a name="ec_please_reopen"></a>EC \_ PLEASE \_ REOPEN

El archivo de origen ha cambiado. La aplicación debe volver a generar el gráfico de filtros.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Cero.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

El filtro heredado [Windows origen multimedia](windows-media-source-filter.md) envía este evento. Los nuevos filtros no deben enviar este evento.

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

 

 




