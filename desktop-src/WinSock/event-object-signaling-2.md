---
description: WSPEventSelect se comporta exactamente igual que WSPAsyncSelect, salvo que, en lugar de hacer que se envíe un mensaje de Windows tras la aparición de cualquier \_ evento de red FD XXX designado (por ejemplo, FD \_ Read, FD \_ de escritura, etc.), se establece un objeto de evento designado.
ms.assetid: 28f6eb78-1bb8-4eda-aac5-017975890502
title: Señalización del objeto de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42854a1f4e116c8dba100025007362898d183f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705629"
---
# <a name="event-object-signaling"></a>Señalización del objeto de evento

[**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)) se comporta exactamente igual que [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) , salvo que, en lugar de hacer que se envíe un mensaje de Windows tras la aparición de cualquier \_ evento de red FD XXX designado (por ejemplo, FD \_ Read, FD \_ de escritura, etc.), se establece un objeto de evento designado.

Además, el proveedor de servicios recuerda el hecho de que se \_ ha producido un evento de red FD XXX determinado. Esto es necesario, ya que la repetición de todos los eventos de red nominados dará lugar a la señalización de un objeto de evento único. Una llamada a [**WSPEnumNetworkEvents**](/previous-versions/windows/hardware/network/ff566284(v=vs.85)) hace que el contenido actual de la memoria de eventos de red se copie en un búfer proporcionado por el cliente y la memoria de eventos de red que se va a borrar. El cliente también puede designar un objeto de evento determinado que se va a borrar de forma atómica junto con la memoria de eventos de red.

 

 
