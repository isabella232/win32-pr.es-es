---
description: Permite realizar un seguimiento de las tarjetas dentro de los lectores. Estas rutinas suelen usar la estructura \_ SCARD READERSTATE dentro de una matriz.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Funciones de seguimiento de tarjetas inteligentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b81ce357cf683d29c1a86d48993c16b7f363635b8e6e3c7e0f2a6ad0900f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917345"
---
# <a name="smart-card-tracking-functions"></a>Funciones de seguimiento de tarjetas inteligentes

Las siguientes funciones permiten realizar un seguimiento de las tarjetas dentro de los lectores. Estas rutinas suelen usar la [**estructura \_ READERSTATE de SCARD**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) dentro de una matriz.



| Tema                                                | Descripción                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Busque una tarjeta cuya cadena [*ATR*](../secgloss/a-gly.md) coincida con un nombre de tarjeta proporcionado. |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Bloquee la ejecución hasta que cambie la disponibilidad actual de las tarjetas.                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Finalizar acciones pendientes.                                                                                                         |



 

 

 
