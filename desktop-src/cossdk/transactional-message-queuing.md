---
description: Una transacción es una serie de modificaciones de un almacén de datos (como una base de datos o un sistema de archivos) garantizada que se ejecute correctamente o que no se ejecute en absoluto.
ms.assetid: 1567d9d3-7839-42f0-9507-7bbf61d8eaf2
title: Message Queue Server transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4730b20f4014cdf7c76462d3f2cae272695d907
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080165"
---
# <a name="transactional-message-queuing"></a>Message Queue Server transaccional

Una *transacción* es una serie de modificaciones de un almacén de datos (como una base de datos o un sistema de archivos) garantizada que se ejecute correctamente o que no se ejecute en absoluto. Para implementar una transacción, se mantiene un registro del estado del almacén de datos antes de que comience la transacción y, si se produce un error en una de las modificaciones, la transacción devuelve un error y el estado inicial se restaura (o se revierte). Las transacciones se utilizan para mantener la integridad de los datos y, por consiguiente, desempeñan un papel importante en la programación del software empresarial.

A menudo, las aplicaciones se pueden desarrollar con una transacción o flujo de trabajo empresarial que se divide en varias transacciones o actividades más pequeñas. Estas actividades se separan en el tiempo y después se conectan mediante colas de mensajes confiables.

1.  La primera transacción implica la base de datos de entrada de pedidos. [Message Queue Server](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) mueve el mensaje de una cola a otra, exactamente una vez, con capacidades de transacción. Si la base de datos está actualizada, hay un mensaje en la cola. Si el mensaje no llega a la cola, se anula y se revierte la base de datos.
2.  En algún momento posterior, Message Queue Server detecta que el servidor está disponible. No hay ningún sondeo de la aplicación para la existencia del servidor. Esta es la segunda transacción.
3.  La tercera transacción implica una consulta de base de datos de envío y la actualización de la base de datos de envío. Si se produce un error en el servidor en el medio de esta transacción, la modificación se revierte y el mensaje se devuelve a la cola de entrada. Esto garantiza que la integridad de los datos y las bases de datos se mantiene durante las transacciones.

 

 



