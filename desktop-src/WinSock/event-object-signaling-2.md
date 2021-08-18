---
description: WSPEventSelect se comporta exactamente igual que WSPAsyncSelect, salvo que, en lugar de hacer que se envíe un mensaje Windows tras la aparición de cualquier evento de red FD XXX designado \_ (por ejemplo, FD \_ READ, FD WRITE, etc.), se establece un objeto de evento \_ designado.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Señalización de objetos de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eed237db696298a2f8053fb61cb0009d9d25d7f37497e0a19d58044d27d8dbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132628"
---
# <a name="event-object-signaling"></a>Señalización de objetos de evento

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) se comporta exactamente igual que [**WSPAsyncSelect,**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) salvo que, en lugar de hacer que se envíe un mensaje Windows tras la aparición de cualquier evento de red FD XXX designado \_ (por ejemplo, FD \_ READ, FD \_ WRITE, etc.), se establece un objeto de evento designado.

Además, el proveedor de servicios recuerda el hecho de que se haya producido un evento de red \_ FD XXX determinado. Esto es necesario, ya que la aparición de todos y cada uno de los eventos de red designados dará lugar a la señalización de un único objeto de evento. Una llamada a [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) hace que el contenido actual de la memoria de eventos de red se copie en un búfer proporcionado por el cliente y se borra la memoria de eventos de red. El cliente también puede designar un objeto de evento determinado que se va a borrar de forma atómica junto con la memoria de eventos de red.

 

 
