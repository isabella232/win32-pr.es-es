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
ms.openlocfilehash: 00e3a600b7345b2cf05b5fb76f20b968e1af9ddecfb72f8442ada34dfd98ae3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034523"
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

## <a name="remarks"></a>Comentarios

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85)) mediante el [**método add \_ TransportParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_transportparametersupdate) Para anular el registro del controlador de eventos, use [**el \_ método Remove TransportParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_transportparametersupdate)

 

 