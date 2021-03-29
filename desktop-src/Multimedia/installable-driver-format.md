---
title: Formato del controlador instalable
description: Formato del controlador instalable
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- Controladores instalables, formatos
- Controladores instalables, función DriverProc
- Controladores instalables, mensajes
- mensajes de controlador
- formatos de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358914"
---
# <a name="installable-driver-format"></a>Formato del controlador instalable

Cada controlador instalable exporta una función [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) . Esta función de punto de entrada común recibe *mensajes de controlador* del sistema que dirigen al controlador para llevar a cabo acciones o proporcionar información. El sistema envía mensajes de controlador a la función **DriverProc** cuando una aplicación o dll abre o cierra el controlador o solicita que se envíe un mensaje al controlador. La función **DriverProc** procesa el mensaje o pasa el mensaje al controlador de mensajes predeterminado, la función [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) . En cualquier caso, **DriverProc** debe devolver un valor que indique si la acción solicitada se realizó correctamente.

 

 