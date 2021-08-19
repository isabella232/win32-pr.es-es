---
title: Evento ConnectionStatusChanged
description: Se produce cuando cambia el estado de conexión de red del dispositivo.
ms.assetid: d1f04fa5-895e-4e86-9643-e880388dcded
keywords:
- Api de streaming multimedia de eventos ConnectionStatusChanged
topic_type:
- apiref
api_name:
- ConnectionStatusChanged
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ccc19c71b56977a77ac5ec05448ea72eaff79d9e96b42f4f297d7046079f571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060435"
---
# <a name="connectionstatuschanged-event"></a>Evento ConnectionStatusChanged

Se produce cuando cambia el estado de conexión de red del dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
void ConnectionStatusChanged();
```



## <a name="parameters"></a>Parámetros

Este evento no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Para controlar las notificaciones de este evento, registre una función de controlador de eventos [**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85)) mediante el [**método add \_ ConnectionStatusChanged.**](ibasicdevice-add-connectionstatuschanged.md) Para anular el registro del controlador de eventos, use [**el \_ método remove ConnectionStatusChanged.**](ibasicdevice-remove-connectionstatuschanged.md)

 

 