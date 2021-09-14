---
description: Una transacción es una serie de modificaciones de un almacén de datos (como una base de datos o un sistema de archivos) que se garantiza que se ejecute correctamente o no se ejecute correctamente.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Transactional Message Queuing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4730b20f4014cdf7c76462d3f2cae272695d907
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361613"
---
# <a name="transactional-message-queuing"></a>Transactional Message Queuing

Una *transacción* es una serie de modificaciones de un almacén de datos (como una base de datos o un sistema de archivos) que se garantiza que se ejecute correctamente o no se ejecute correctamente. Para implementar una transacción, se mantiene un registro del estado del almacén de datos antes de que comience la transacción y, si se produce un error en una de las modificaciones, la transacción devuelve un error y el estado inicial se restaura (o se revierte). Las transacciones se usan para mantener la integridad de los datos y, por tanto, desempeñan un papel importante en la programación de software empresarial.

A menudo, las aplicaciones se pueden desarrollar mediante una transacción empresarial o un flujo de trabajo que se divide en varias transacciones o actividades más pequeñas. Estas actividades se separan en el tiempo y, a continuación, se conectan mediante colas de mensajes confiables.

1.  La primera transacción implica la base de datos de entrada de pedido. [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) mueve el mensaje de una cola a otra, exactamente una vez, mediante funcionalidades de transacción. Si la base de datos se actualiza, hay un mensaje en la cola. Si el mensaje no llega a la cola, se anula y se revierte la base de datos.
2.  En algún momento posterior, Message Queuing detecta que el servidor está disponible. No hay ningún sondeo de aplicación para la existencia del servidor. Esta es la segunda transacción.
3.  La tercera transacción implica una consulta de base de datos de envío y la actualización de la base de datos de envío. Si se produce un error en el servidor en medio de esta transacción, la modificación se revierte y el mensaje se devuelve a la cola de entrada. Esto garantiza que la integridad de los datos y las bases de datos se mantenga durante las transacciones.

 

 



