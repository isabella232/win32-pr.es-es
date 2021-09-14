---
title: Evento TransportParametersUpdate
description: Se produce cada vez que se actualiza cualquiera de un conjunto de parámetros de transporte en la DMR.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- TransportParametersUpdate event Media Streaming API
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252471"
---
# <a name="transportparametersupdate-event"></a>Evento TransportParametersUpdate

Se produce cada vez que se actualiza cualquiera de un conjunto de parámetros de transporte en la DMR.

## <a name="syntax"></a>Sintaxis


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) mediante el [**método add \_ TransportParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) Para anular el registro del controlador de eventos, use [**el \_ método Remove TransportParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate)

 

 