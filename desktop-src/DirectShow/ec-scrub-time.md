---
description: Especifica la marca de tiempo para el paso de fotograma más reciente.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530362520f8e80ef06a769383f82dee1d60d66c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161512"
---
# <a name="ec_scrub_time"></a>HORA DE \_ LIMPIEZA \_ DE EC

Especifica la marca de tiempo para el paso de fotograma más reciente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) 32 bits inferiores de la marca de tiempo.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**DWORD**) 32 bits superiores de la marca de tiempo.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

El presentador del filtro [**Representador de**](enhanced-video-renderer-filter.md) vídeo mejorado (EVR) envía este mensaje al EVR cuando completa un paso de fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> </dl>

 

 




