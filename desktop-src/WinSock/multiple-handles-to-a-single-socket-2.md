---
description: Puesto que los elementos duplicados son los descriptores de socket y no los sockets subyacentes, todos los Estados asociados a un socket se mantienen en común en todos los descriptores.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Varios identificadores para un solo socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2356f24a69d132f87e0f6543f61509ff12acba5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696372"
---
# <a name="multiple-handles-to-a-single-socket"></a>Varios identificadores para un solo socket

Puesto que los elementos duplicados son los descriptores de socket y no los sockets subyacentes, todos los Estados asociados a un socket se mantienen en común en todos los descriptores. Por ejemplo, una operación de [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) realizada con un descriptor es visible posteriormente mediante un [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) de uno o todos los descriptores.

La notificación en sockets compartidos está sujeta a las restricciones habituales de [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) y [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). La emisión de cualquiera de estas llamadas mediante cualquiera de los descriptores compartidos cancela cualquier registro de eventos anterior para el socket, independientemente del descriptor que se haya utilizado para realizar ese registro. Por lo tanto, por ejemplo, no sería posible tener el procesamiento de eventos de lectura FD de recepción \_ y eventos de escritura FD de recepción de proceso B \_ . En situaciones en las que se requiere una coordinación tan estrecha, se recomienda que los desarrolladores consideren el uso de subprocesos en lugar de procesos independientes.

 

 
