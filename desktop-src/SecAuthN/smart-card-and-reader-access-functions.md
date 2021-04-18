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
# <a name="smart-card-and-reader-access-functions"></a><span data-ttu-id="30666-103">Funciones de acceso a tarjetas inteligentes y lectores</span><span class="sxs-lookup"><span data-stu-id="30666-103">Smart Card and Reader Access Functions</span></span>

<span data-ttu-id="30666-104">Las siguientes funciones se conectan a una [*tarjeta inteligente*](../secgloss/s-gly.md)específica y se comunican con ella.</span><span class="sxs-lookup"><span data-stu-id="30666-104">The following functions connect to and communicate with a specific [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="30666-105">Las operaciones de e/s en la tarjeta utilizan un búfer para enviar o recibir datos y una estructura que contiene información de control de protocolo.</span><span class="sxs-lookup"><span data-stu-id="30666-105">I/O operations to the card use a buffer for sending or receiving data and a structure that contains protocol control information.</span></span> <span data-ttu-id="30666-106">La estructura de información de control de protocolo siempre comienza con una estructura de [**\_ \_ solicitud de e/s**](scard-io-request.md) .</span><span class="sxs-lookup"><span data-stu-id="30666-106">The protocol control information structure always begins with an [**SCARD\_IO\_REQUEST**](scard-io-request.md) structure.</span></span>



| <span data-ttu-id="30666-107">Tema</span><span class="sxs-lookup"><span data-stu-id="30666-107">Topic</span></span>                                                  | <span data-ttu-id="30666-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="30666-108">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="30666-109">**SCardConnect**</span><span class="sxs-lookup"><span data-stu-id="30666-109">**SCardConnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | <span data-ttu-id="30666-110">Conectarse a una tarjeta.</span><span class="sxs-lookup"><span data-stu-id="30666-110">Connect to a card.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="30666-111">**SCardReconnect**</span><span class="sxs-lookup"><span data-stu-id="30666-111">**SCardReconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | <span data-ttu-id="30666-112">Restablecer una conexión.</span><span class="sxs-lookup"><span data-stu-id="30666-112">Reestablish a connection.</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="30666-113">**SCardDisconnect**</span><span class="sxs-lookup"><span data-stu-id="30666-113">**SCardDisconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | <span data-ttu-id="30666-114">Finalizar una conexión.</span><span class="sxs-lookup"><span data-stu-id="30666-114">Terminate a connection.</span></span>                                                                                                                                                                                                                    |
| [<span data-ttu-id="30666-115">**SCardBeginTransaction**</span><span class="sxs-lookup"><span data-stu-id="30666-115">**SCardBeginTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | <span data-ttu-id="30666-116">Iniciar una [*transacción*](../secgloss/t-gly.md)y bloquear el acceso de otras aplicaciones a una tarjeta.</span><span class="sxs-lookup"><span data-stu-id="30666-116">Start a [*transaction*](../secgloss/t-gly.md), blocking other applications from accessing a card.</span></span>                                                                                            |
| [<span data-ttu-id="30666-117">**SCardEndTransaction**</span><span class="sxs-lookup"><span data-stu-id="30666-117">**SCardEndTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | <span data-ttu-id="30666-118">Finalizar una transacción y permitir que otras aplicaciones tengan acceso a una tarjeta.</span><span class="sxs-lookup"><span data-stu-id="30666-118">End a transaction, allowing other applications to access a card.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="30666-119">**SCardStatus**</span><span class="sxs-lookup"><span data-stu-id="30666-119">**SCardStatus**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | <span data-ttu-id="30666-120">Proporcione el estado actual del lector.</span><span class="sxs-lookup"><span data-stu-id="30666-120">Provide the current status of the reader.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="30666-121">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="30666-121">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | <span data-ttu-id="30666-122">Solicita el servicio y recibe datos de una tarjeta mediante [*T = 0*](../secgloss/t-gly.md), [*t = 1*](../secgloss/t-gly.md)y protocolos sin formato.</span><span class="sxs-lookup"><span data-stu-id="30666-122">Requests service and receives data back from a card using [*T=0*](../secgloss/t-gly.md), [*T=1*](../secgloss/t-gly.md), and raw protocols.</span></span> |



 

 

 
