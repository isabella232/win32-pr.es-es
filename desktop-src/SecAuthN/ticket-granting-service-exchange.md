---
description: Una vez que se ha establecido un vale de concesión de vales (TGT) y una clave de sesión para el cliente, el cliente puede solicitar una clave de sesión independiente y un vale para el servicio.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Intercambio del servicio de concesión de vales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666826"
---
# <a name="ticket-granting-service-exchange"></a><span data-ttu-id="16f21-103">Intercambio del servicio de concesión de vales</span><span class="sxs-lookup"><span data-stu-id="16f21-103">Ticket-Granting Service Exchange</span></span>

<span data-ttu-id="16f21-104">Una vez que se ha establecido un vale de concesión de vales (TGT) y una [*clave de sesión*](../secgloss/s-gly.md) para el cliente, el cliente puede solicitar una clave de sesión independiente y un vale para el servicio.</span><span class="sxs-lookup"><span data-stu-id="16f21-104">After a ticket-granting ticket (TGT) and [*session key*](../secgloss/s-gly.md) have been established for the client, the client can request a separate session key and ticket for the service.</span></span>

<span data-ttu-id="16f21-105">**Para solicitar un vale para otro servicio**</span><span class="sxs-lookup"><span data-stu-id="16f21-105">**To request a ticket for another service**</span></span>

1.  <span data-ttu-id="16f21-106">El cliente Kerberos de la estación de trabajo del usuario solicita [*credenciales*](../secgloss/c-gly.md) para el servicio mediante el envío del [*centro de distribución de claves*](../secgloss/k-gly.md) (KDC), un mensaje de tipo KRB \_ TGS \_ req (solicitud de servicio de Kerberos Ticket-Granting).</span><span class="sxs-lookup"><span data-stu-id="16f21-106">The Kerberos client on the user's workstation requests [*credentials*](../secgloss/c-gly.md) for the service by sending, to the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC), a message of type KRB\_TGS\_REQ (Kerberos Ticket-Granting Service Request).</span></span> <span data-ttu-id="16f21-107">Este mensaje consta de la identidad del servicio para el que el cliente solicita credenciales, un mensaje de autenticador cifrado con la nueva clave de [*sesión*](../secgloss/s-gly.md)de inicio de sesión del usuario y el TGT obtenido del [intercambio del servicio de autenticación](authentication-service-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="16f21-107">This message consists of the identity of the service for which the client is requesting credentials, an authenticator message encrypted with the user's new logon [*session key*](../secgloss/s-gly.md), and the TGT obtained from the [Authentication Service Exchange](authentication-service-exchange.md).</span></span>
2.  <span data-ttu-id="16f21-108">Cuando el KDC recibe un req de KRB \_ TGS \_ , el KDC descifra el TGT con su clave secreta y extrae la clave de sesión de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="16f21-108">When the KDC receives a KRB\_TGS\_REQ, the KDC decrypts the TGT with its secret key and extracts the user's logon session key.</span></span>
3.  <span data-ttu-id="16f21-109">El KDC usa la [*clave de sesión*](../secgloss/s-gly.md) de inicio de sesión para descifrar el mensaje del autenticador del usuario y lo evalúa.</span><span class="sxs-lookup"><span data-stu-id="16f21-109">The KDC uses the logon [*session key*](../secgloss/s-gly.md) to decrypt the user's authenticator message and evaluates it.</span></span> <span data-ttu-id="16f21-110">Si el autenticador pasa la prueba, el KDC extrae los datos de autorización del usuario del TGT e invent una clave de sesión para que el usuario lo comparta con el servidor solicitado.</span><span class="sxs-lookup"><span data-stu-id="16f21-110">If the authenticator passes the test, the KDC extracts the user's authorization data from the TGT and invents a session key for the user to share with the requested server.</span></span>
4.  <span data-ttu-id="16f21-111">El KDC cifra una copia de la clave de sesión de servicio con la clave de sesión de inicio de sesión del usuario.</span><span class="sxs-lookup"><span data-stu-id="16f21-111">The KDC encrypts one copy of the service session key with the user's logon session key.</span></span>
5.  <span data-ttu-id="16f21-112">El KDC inserta otra copia de la clave de sesión de servicio en un vale, junto con los datos de autorización del usuario, y cifra el vale con la [*clave maestra*](../secgloss/m-gly.md)del servidor.</span><span class="sxs-lookup"><span data-stu-id="16f21-112">The KDC embeds another copy of the service session key in a ticket, along with the user's authorization data, and encrypts the ticket with the server's [*master key*](../secgloss/m-gly.md).</span></span>
6.  <span data-ttu-id="16f21-113">El KDC envía estas credenciales de vuelta al cliente respondiendo con un mensaje de tipo KRB \_ TGS \_ REP (respuesta del servicio de Kerberos Ticket-Granting).</span><span class="sxs-lookup"><span data-stu-id="16f21-113">The KDC sends these credentials back to the client by replying with a message of type KRB\_TGS\_REP (Kerberos Ticket-Granting Service Reply).</span></span>
7.  <span data-ttu-id="16f21-114">Cuando el cliente recibe la respuesta, descifra la clave de sesión de servicio con la clave de sesión de inicio de sesión del usuario y almacena la clave de sesión de servicio en su caché de vales.</span><span class="sxs-lookup"><span data-stu-id="16f21-114">When the client receives the reply, it decrypts the service session key with the user's logon session key and stores the service session key in its ticket cache.</span></span>
8.  <span data-ttu-id="16f21-115">El cliente extrae el vale en el servidor y lo almacena en su caché de vales.</span><span class="sxs-lookup"><span data-stu-id="16f21-115">The client extracts the ticket to the server and stores that in its ticket cache.</span></span>

 

 
