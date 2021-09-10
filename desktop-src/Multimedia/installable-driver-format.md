---
title: Formato de controlador instalable
description: Formato de controlador instalable
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- controladores instalables, formatos
- controladores instalables, función DriverProc
- controladores instalables, mensajes
- mensajes de controlador
- formatos de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372272"
---
# <a name="installable-driver-format"></a>Formato de controlador instalable

Cada controlador instalable exporta una [función DriverProc.](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) Esta función de punto de entrada común recibe *mensajes* de controlador del sistema que dirigen al controlador a realizar acciones o proporcionar información. El sistema envía mensajes de controlador a la función **DriverProc** cuando una aplicación o dll abre o cierra el controlador o solicita que se envíe un mensaje al controlador. La **función DriverProc** procesa el mensaje o pasa el mensaje al controlador de mensajes predeterminado, la [función DefDriverProc.](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) En cualquier caso, **DriverProc** debe devolver un valor que indique si la acción solicitada se ha realizado correctamente.

 

 