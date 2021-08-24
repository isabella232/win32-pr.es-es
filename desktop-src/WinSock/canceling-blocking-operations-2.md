---
description: En cualquier momento, un subproceso puede llamar a WSAIsBlocking para determinar si hay o no una llamada de bloqueo en curso.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Cancelación de operaciones de bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064948fe7c1c1262acb9f4f8ef25a3ad3e721e77a188f313541595ef75f9ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030695"
---
# <a name="canceling-blocking-operations"></a>Cancelación de operaciones de bloqueo

En cualquier momento, un subproceso puede llamar a [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) para determinar si hay o no una llamada de bloqueo en curso. (Esta función se implementa dentro de las correcciones de compatibilidad de Windows Sockets 1.1 y, por tanto, no tiene ningún homólogo SPI). Claramente, esto solo es posible cuando el proveedor de servicios emplea el pseudobloqueo, en lugar de un bloqueo verdadero. Cuando sea necesario, se puede llamar a [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) en cualquier momento para cancelar cualquier operación de pseudobloqueo actual.

 

 
