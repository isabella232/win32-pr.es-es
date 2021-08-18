---
description: 'EC_ERRORABORTEX: se anuló una operación debido a un error.'
ms.assetid: de7b5222-3a29-40cc-af1a-2672bd68b7c9
title: EC_ERRORABORTEX (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18f0cb010e6ebf94f69cd8bbebfc7cdeea16d1d085069ad2f12fedb6fbf4a266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015983"
---
# <a name="ec_errorabortex"></a>\_ERROR DE ECABORTEX

Se anuló una operación debido a un error.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

**(HRESULT)** Código de error de la operación que ha generado un error.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

**(BSTR)** Cadena que contiene información de error adicional.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Comentarios

El filtro [heredado Windows origen multimedia](windows-media-source-filter.md) envía este evento. Los nuevos filtros no deben enviar este evento.

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

 

 




