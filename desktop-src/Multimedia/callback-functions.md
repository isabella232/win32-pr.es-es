---
title: Funciones de devolución de llamada
description: Funciones de devolución de llamada
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- controladores instalables, funciones de devolución de llamada
- controladores instalables, función DriverCallback
- controladores instalables, eventos
- Función DriverCallback
- DRV_OPEN mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fabb833b0aa3adef444f8242d540eb48dcbe381ebc5c7f62c6dedc0d5e9160e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786205"
---
# <a name="callback-functions"></a>Funciones de devolución de llamada

Los controladores instalables pueden notificar a la aplicación, ventana o tarea que abrió la instancia determinada sobre eventos mediante la [función DriverCallback.](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) Esta función proporciona al controlador los medios para devolver información a una aplicación o DLL mientras continúa procesando una solicitud.

Si un controlador admite funciones de devolución de llamada, la aplicación o dll que abre la instancia debe proporcionar un valor que sea la dirección de una función de devolución de llamada, un identificador de ventana o un identificador de tarea. Este valor y una marca que identifica el tipo del valor se pasan normalmente en una estructura a la que apunta el segundo parámetro del [**mensaje DRV \_ OPEN.**](drv-open.md)

 

 