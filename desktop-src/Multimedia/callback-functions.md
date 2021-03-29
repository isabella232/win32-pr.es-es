---
title: Funciones de devolución de llamada
description: Funciones de devolución de llamada
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- Controladores instalables, funciones de devolución de llamada
- Controladores instalables, función DriverCallback
- Controladores instalables, eventos
- DriverCallback función)
- Mensaje DRV_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e23f933567d125dd07f81047ea8868c12f41ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904584"
---
# <a name="callback-functions"></a>Funciones de devolución de llamada

Los controladores instalables pueden notificar a la aplicación, ventana o tarea que abrió la instancia determinada sobre eventos mediante la función [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) . Esta función proporciona al controlador el medio para devolver información a una aplicación o DLL mientras continúa procesando una solicitud.

Si un controlador admite funciones de devolución de llamada, la aplicación o DLL que abre la instancia debe proporcionar un valor que sea la dirección de una función de devolución de llamada, un identificador de ventana o un identificador de tarea. Este valor y una marca que identifica el tipo del valor se pasan normalmente en una estructura señalada por el segundo parámetro del mensaje [**\_ abierto DRV**](drv-open.md) .

 

 