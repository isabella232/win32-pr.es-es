---
title: Evento RenderingParametersUpdate
description: Se produce cada vez que se actualiza cualquiera de los parámetros de control de representación en la DMR.
ms.assetid: 863ca879-a420-43d6-9ac8-94f8303bb759
keywords:
- RenderingParametersUpdate event Media Streaming API
topic_type:
- apiref
api_name:
- RenderingParametersUpdate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35e4898bae876babb0e5fbc1c4b9760eec6a9b62
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571656"
---
# <a name="renderingparametersupdate-event"></a>Evento RenderingParametersUpdate

Se produce cada vez que se actualiza cualquiera de los parámetros de control de representación en la DMR.

## <a name="syntax"></a>Sintaxis


```C++
void RenderingParametersUpdate();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85)) mediante el [**método add \_ RenderingParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-add_renderingparametersupdate) Para anular el registro del controlador de eventos, use [**el \_ método Remove RenderingParametersUpdate.**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-remove_renderingparametersupdate)

 

 