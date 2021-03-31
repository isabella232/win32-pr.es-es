---
title: Operaciones asincrónicas
description: Cuando se invoca RasDial como una operación asincrónica, la función vuelve inmediatamente.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db434b7e6d080933e7e21de056f9af5ea7d57dfe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418815"
---
# <a name="asynchronous-operations"></a>Operaciones asincrónicas

Cuando se invoca [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) como una operación asincrónica, la función vuelve inmediatamente. En el modo asincrónico, la llamada **rasdial** debe especificar un [controlador de notificación](notification-handlers.md) que el administrador de conexiones de acceso remoto utiliza para informar al cliente siempre que la operación de conexión cambie de estado o se produzca un error.

El controlador de notificación puede ser una ventana para recibir mensajes o una función de devolución de llamada [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc), [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)o [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) . El administrador de conexiones de acceso remoto realiza sus notificaciones asincrónicas en el contexto del subproceso que realizó la llamada [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Por esta razón, el subproceso que realiza la llamada no debe finalizar hasta que la operación de conexión se haya establecido correctamente o se produzca un error. Como en modo sincrónico, la aplicación cliente puede terminar con seguridad una vez que se ha establecido la conexión y debe [cerrar la operación de conexión](disconnecting.md) si se produce un error.

 

 




