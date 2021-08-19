---
description: Puesto que lo que se duplica son los descriptores de socket y no los sockets subyacentes, todos los estados asociados a un socket se mantienen en común en todos los descriptores.
ms.assetid: f3a2cd5a-bc3a-4aeb-8606-7b8aa6afb105
title: Varios identificadores para un único socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e402d19c3306158a905f2e9ddc263649e52d214a3d9441509e7a277f7d2800
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121405"
---
# <a name="multiple-handles-to-a-single-socket"></a>Varios identificadores para un único socket

Puesto que lo que se duplica son los descriptores de socket y no los sockets subyacentes, todos los estados asociados a un socket se mantienen en común en todos los descriptores. Por ejemplo, una [**operación WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) realizada con un descriptor se ve posteriormente mediante [**un WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) de cualquiera o todos los descriptores.

La notificación en sockets compartidos está sujeta a las restricciones habituales [**de WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) y [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)). La emisión de cualquiera de estas llamadas mediante cualquiera de los descriptores compartidos cancela cualquier registro de eventos anterior para el socket, independientemente del descriptor que se usó para realizar ese registro. Por lo tanto, por ejemplo, no sería posible que el proceso A reciba eventos FD READ y que \_ el proceso B reciba eventos FD \_ WRITE. En el caso de situaciones en las que se requiere una coordinación tan estrecha, se sugiere que los desarrolladores consideren la posibilidad de usar subprocesos en lugar de procesos independientes.

 

 
