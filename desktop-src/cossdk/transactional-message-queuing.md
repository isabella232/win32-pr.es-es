---
description: Una transacción es una serie de modificaciones de un almacén de datos (como una base de datos o un sistema de archivos) que se garantiza que se ejecuta correctamente o no se ejecuta correctamente.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Transactional Message Queuing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3282a95d4f9a3ba451e78fe4d9f17acf007b0007abea4fdb4951de9c1540383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636735"
---
# <a name="transactional-message-queuing"></a>Transactional Message Queuing

Una *transacción* es una serie de modificaciones de un almacén de datos (como una base de datos o un sistema de archivos) que se garantiza que se ejecuta correctamente o no se ejecuta correctamente. Para implementar una transacción, se mantiene un registro del estado del almacén de datos antes de que comience la transacción y, si se produce un error en una de las modificaciones, la transacción devuelve un error y el estado inicial se restaura (o se revierte). Las transacciones se usan para mantener la integridad de los datos y, por tanto, desempeñan un papel importante en la programación de software empresarial.

A menudo, las aplicaciones se pueden desarrollar mediante una transacción empresarial o un flujo de trabajo que se divide en varias transacciones o actividades más pequeñas. Estas actividades se separan en el tiempo y, a continuación, se conectan mediante colas de mensajes confiables.

1.  La primera transacción implica la base de datos de entrada de pedido. [Message Queuing mueve](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) el mensaje de una cola a otra, exactamente una vez, mediante funcionalidades de transacción. Si se actualiza la base de datos, hay un mensaje en la cola. Si el mensaje no llega a la cola, se anula y se revierte la base de datos.
2.  En algún momento posterior, Message Queuing detecta que el servidor está disponible. No hay ningún sondeo de aplicación para la existencia del servidor. Esta es la segunda transacción.
3.  La tercera transacción implica una consulta de base de datos de envío y la actualización de la base de datos de envío. Si se produce un error en el servidor en medio de esta transacción, la modificación se revierte y el mensaje se devuelve a la cola de entrada. Esto garantiza que la integridad de los datos y las bases de datos se mantenga durante las transacciones.

 

 



