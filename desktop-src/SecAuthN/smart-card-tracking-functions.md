---
description: Permite realizar un seguimiento de las tarjetas dentro de los lectores. Estas rutinas suelen usar la estructura \_ SCARD READERSTATE dentro de una matriz.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Funciones de seguimiento de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253659"
---
# <a name="smart-card-tracking-functions"></a>Funciones de seguimiento de tarjetas inteligentes

Las siguientes funciones permiten realizar un seguimiento de las tarjetas dentro de los lectores. Estas rutinas suelen usar la [**estructura \_ SCARD READERSTATE**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) dentro de una matriz.



| Tema                                                | Descripción                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Busque una tarjeta cuya cadena [*ATR*](../secgloss/a-gly.md) coincida con un nombre de tarjeta proporcionado. |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Bloquee la ejecución hasta que cambie la disponibilidad actual de las tarjetas.                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Finalizar acciones pendientes.                                                                                                         |



 

 

 
