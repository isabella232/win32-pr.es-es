---
description: Un subproceso puede, en cualquier momento, llamar a WSAIsBlocking para determinar si una llamada de bloqueo está actualmente en curso.
ms.assetid: 6213ded4-feab-404f-86a0-3db9a0a42769
title: Cancelar operaciones de bloqueo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 502870b8935dc97c1d6c3714808d1c6532780f7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705649"
---
# <a name="canceling-blocking-operations"></a>Cancelar operaciones de bloqueo

Un subproceso puede, en cualquier momento, llamar a [WSAIsBlocking](/windows/desktop/api/winsock2/nf-winsock2-wsaisblocking) para determinar si una llamada de bloqueo está actualmente en curso. (Esta función se implementa dentro de las correcciones de compatibilidad de Windows Sockets 1,1 y, por lo tanto, no tiene ningún homólogo SPI). Claramente, esto solo es posible cuando el proveedor de servicios está empleando un pseudo bloqueo, en lugar de un bloqueo real. Cuando sea necesario, se puede llamar a [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) en cualquier momento para cancelar cualquier operación de pseudo bloqueo actual.

 

 
