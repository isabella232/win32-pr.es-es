---
title: Operaciones asincrónicas
description: Cuando RasDial se invoca como una operación asincrónica, la función se devuelve inmediatamente.
ms.assetid: f165b4a7-00fb-4888-8225-8fd106e113f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db434b7e6d080933e7e21de056f9af5ea7d57dfe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476655"
---
# <a name="asynchronous-operations"></a>Operaciones asincrónicas

Cuando [**RasDial se**](/windows/desktop/api/Ras/nf-ras-rasdiala) invoca como una operación asincrónica, la función se devuelve inmediatamente. En modo asincrónico, la llamada **RasDial** debe especificar un controlador de notificaciones que el Connection Manager de acceso remoto usa para informar al cliente cada vez que la operación de conexión cambia de estado o se produce un error. [](notification-handlers.md)

El controlador de notificaciones puede ser una ventana para recibir mensajes o una función de devolución de llamada [**RasDialFunc,**](/windows/desktop/api/Ras/nc-ras-rasdialfunc) [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)o [**RasDialFunc2.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) El acceso remoto Connection Manager realiza sus notificaciones asincrónicas en el contexto del subproceso que realizó la [**llamada RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Por este motivo, el subproceso que realiza la llamada no debe finalizar hasta que la operación de conexión se haya establecido correctamente o se produzca un error. Al igual que en el modo sincrónico, la aplicación [](disconnecting.md) cliente puede finalizar de forma segura una vez establecida la conexión y debe apagar la operación de conexión si se produce un error.

 

 




