---
description: Especifica la marca de tiempo para el paso de fotograma más reciente.
ms.assetid: 2c2ef8b8-7bee-4cd8-ad87-b48d6a48aa0e
title: EC_SCRUB_TIME (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d4d3cc09d286f6955dda30aeb77288b75e90e8c66777a5f9f16246507f64b45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686095"
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

## <a name="remarks"></a>Comentarios

El presentador del filtro [**Representador de**](enhanced-video-renderer-filter.md) vídeo mejorado (EVR) envía este mensaje al EVR cuando completa un paso de fotograma.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> </dl>

 

 




