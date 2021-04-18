---
description: Conectarse a una tarjeta inteligente específica y comunicarse con ella.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Funciones de acceso a tarjetas inteligentes y lectores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668262"
---
# <a name="smart-card-and-reader-access-functions"></a>Funciones de acceso a tarjetas inteligentes y lectores

Las siguientes funciones se conectan a una [*tarjeta inteligente*](../secgloss/s-gly.md)específica y se comunican con ella. Las operaciones de e/s en la tarjeta utilizan un búfer para enviar o recibir datos y una estructura que contiene información de control de protocolo. La estructura de información de control de protocolo siempre comienza con una estructura de [**\_ \_ solicitud de e/s**](scard-io-request.md) .



| Tema                                                  | Descripción                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardConnect**](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | Conectarse a una tarjeta.                                                                                                                                                                                                                         |
| [**SCardReconnect**](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | Restablecer una conexión.                                                                                                                                                                                                                  |
| [**SCardDisconnect**](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | Finalizar una conexión.                                                                                                                                                                                                                    |
| [**SCardBeginTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | Iniciar una [*transacción*](../secgloss/t-gly.md)y bloquear el acceso de otras aplicaciones a una tarjeta.                                                                                            |
| [**SCardEndTransaction**](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | Finalizar una transacción y permitir que otras aplicaciones tengan acceso a una tarjeta.                                                                                                                                                                           |
| [**SCardStatus**](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | Proporcione el estado actual del lector.                                                                                                                                                                                                  |
| [**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | Solicita el servicio y recibe datos de una tarjeta mediante [*T = 0*](../secgloss/t-gly.md), [*t = 1*](../secgloss/t-gly.md)y protocolos sin formato. |



 

 

 
