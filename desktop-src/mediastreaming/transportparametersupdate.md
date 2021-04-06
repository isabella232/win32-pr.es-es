---
title: Evento TransportParametersUpdate
description: Se produce siempre que se actualiza cualquier conjunto de parámetros de transporte en el DMR.
ms.assetid: df9256ca-6c59-462c-b32f-4653546db384
keywords:
- TransportParametersUpdate Event media streaming API
topic_type:
- apiref
api_name:
- TransportParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58df04862275af5da8714f8a954dc5b127f833f2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904582"
---
# <a name="transportparametersupdate-event"></a>Evento TransportParametersUpdate

Se produce siempre que se actualiza cualquier conjunto de parámetros de transporte en el DMR.

## <a name="syntax"></a>Sintaxis


```C++
void TransportParametersUpdate();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) mediante el método [**Add \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) . Para anular el registro del controlador de eventos, use el método [**Remove \_ TransportParametersUpdate**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate) .

 

 