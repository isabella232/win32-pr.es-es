---
description: Permite realizar un seguimiento de las tarjetas en los lectores. Estas rutinas suelen usar la \_ estructura READERSTATE de la matriz en una matriz.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Funciones de seguimiento de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912074"
---
# <a name="smart-card-tracking-functions"></a>Funciones de seguimiento de tarjetas inteligentes

Las siguientes funciones le permiten realizar un seguimiento de las tarjetas en los lectores. Estas rutinas suelen usar la estructura [**\_ READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) de la matriz en una matriz.



| Tema                                                | Descripción                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Busque una tarjeta cuya [*cadena ATR*](../secgloss/a-gly.md) coincida con un nombre de tarjeta proporcionado. |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Bloquear la ejecución hasta que cambie la disponibilidad actual de las tarjetas.                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Finalizar acciones pendientes.                                                                                                         |



 

 

 
