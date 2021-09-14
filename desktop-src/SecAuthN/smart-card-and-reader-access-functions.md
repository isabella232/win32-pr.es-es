---
description: Conectar y comunicarse con una tarjeta inteligente específica.
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: Funciones de acceso de lector y tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374955"
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



 

 

 
