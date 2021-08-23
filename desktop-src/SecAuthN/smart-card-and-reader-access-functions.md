---
description: Conectar y comunicarse con una tarjeta inteligente específica.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Funciones de acceso de lector y tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b571764ae2d31865082e823996e8cc1ecde9d9d3e2dd618f28e528fd465a567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917960"
---
# <a name="smart-card-and-reader-access-functions"></a>Funciones de acceso de lector y tarjeta inteligente

Las siguientes funciones se conectan a una tarjeta inteligente específica y se [*comunican con él.*](../secgloss/s-gly.md) Las operaciones de E/S en la tarjeta usan un búfer para enviar o recibir datos y una estructura que contiene información de control de protocolo. La estructura de información de control de protocolo siempre comienza con una [**estructura SCARD \_ IO \_ REQUEST.**](scard-io-request.md)



| Tema                                                  | Descripción                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Conectar a una tarjeta.                                                                                                                                                                                                                         |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Restablecer una conexión.                                                                                                                                                                                                                  |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Finalizar una conexión.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Inicie una [*transacción*](../secgloss/t-gly.md), lo que impide que otras aplicaciones accedan a una tarjeta.                                                                                            |
| [**SCardEndTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Finalizar una transacción, lo que permite que otras aplicaciones accedan a una tarjeta.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Proporcione el estado actual del lector.                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Solicita el servicio y recibe datos de una tarjeta mediante [*T=0,*](../secgloss/t-gly.md) [*T=1*](../secgloss/t-gly.md)y protocolos sin procesar. |



 

 

 
