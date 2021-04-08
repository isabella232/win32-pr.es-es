---
title: Evento ConnectionStatusChanged
description: Se produce cuando cambia el estado de la conexión de red del dispositivo.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- ConnectionStatusChanged Event media streaming API
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8034cf49298b6523667f2434324a5be9da3b639
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791223"
---
# <a name="connectionstatuschanged-event"></a>Evento ConnectionStatusChanged

Se produce cuando cambia el estado de la conexión de red del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Observaciones

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) mediante el método [**Add \_ ConnectionStatusChanged**](ibasicdevice-add-connectionstatuschanged.md) . Para anular el registro del controlador de eventos, use el método [**Remove \_ ConnectionStatusChanged**](ibasicdevice-remove-connectionstatuschanged.md) .

 

 