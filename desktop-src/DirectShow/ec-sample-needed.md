---
description: Solicita un nuevo ejemplo de entrada del filtro Representador de vídeo mejorado (EVR).
ms.assetid: f1bf32ba-ecb7-435f-aefc-f60fdd355620
title: EC_SAMPLE_NEEDED (Dshow.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da73d02604e128fdf94edb8f84d1526cfcdb586e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161514"
---
# <a name="ec_sample_needed"></a>EJEMPLO \_ DE EC \_ NECESARIO

Solicita un nuevo ejemplo de entrada del filtro [**Representador de**](enhanced-video-renderer-filter.md) vídeo mejorado (EVR).

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificador del flujo de entrada que necesita nueva entrada.

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
| Encabezado<br/> | <dl> <dt>Dshow.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de notificación de eventos](event-notification-codes.md)
</dt> </dl>

 

 




