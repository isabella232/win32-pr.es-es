---
description: Solicita un nuevo ejemplo de entrada del filtro de representador de vídeo mejorado (EVR).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da73d02604e128fdf94edb8f84d1526cfcdb586e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678909"
---
# <a name="ec_sample_needed"></a>ejemplo de EC \_ \_ necesario

Solicita un nuevo ejemplo de entrada del filtro de [**representador de vídeo mejorado**](enhanced-video-renderer-filter.md) (EVR).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificador del flujo de entrada que necesita una nueva entrada.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Cero.

</dd> </dl>

## <a name="default-action"></a>Acción predeterminada

Ninguno.

## <a name="remarks"></a>Observaciones

El mezclador del filtro EVR envía este mensaje cuando necesita un nuevo ejemplo de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> </dl>

 

 




