---
description: Intercambio de cliente/servidor
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Intercambio de cliente/servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155905"
---
# <a name="clientserver-exchange"></a><span data-ttu-id="c0820-103">Intercambio de cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="c0820-103">Client/Server Exchange</span></span>

<span data-ttu-id="c0820-104">Una vez que un usuario tiene un vale para un servidor, el cliente de estación de trabajo puede establecer una sesión de comunicaciones segura con ese servidor.</span><span class="sxs-lookup"><span data-stu-id="c0820-104">After a user has a ticket to a server, the workstation client can establish a secure communications session with that server.</span></span>

<span data-ttu-id="c0820-105">**Para establecer una sesión de comunicaciones segura con un servidor**</span><span class="sxs-lookup"><span data-stu-id="c0820-105">**To establish a secure communications session with a server**</span></span>

1.  <span data-ttu-id="c0820-106">El cliente envía al servidor un mensaje de tipo KRB \_ AP \_ req (solicitud de aplicación de Kerberos).</span><span class="sxs-lookup"><span data-stu-id="c0820-106">The client sends the server a message of type KRB\_AP\_REQ (Kerberos Application Request).</span></span> <span data-ttu-id="c0820-107">Este mensaje contiene un mensaje de autenticador cifrado con la clave enviada por el [*centro de distribución de claves*](/windows/desktop/SecGloss/k-gly) (KDC) para la sesión con el servidor, el vale para las sesiones con el servidor y una marca que indica si el cliente solicita la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="c0820-107">This message contains an authenticator message that is encrypted with the key sent by the [*Key Distribution Center*](/windows/desktop/SecGloss/k-gly) (KDC) for the session with the server, the ticket for sessions with the server, and a flag that indicates whether the client requests mutual authentication.</span></span> <span data-ttu-id="c0820-108">La configuración de la marca que solicita la autenticación mutua es una de las opciones de configuración de [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="c0820-108">Setting the flag that requests mutual authentication is one of the options in configuring [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="c0820-109">Nunca se pregunta al usuario si se debe usar la autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="c0820-109">The user is never asked whether mutual authentication should be used.</span></span>
2.  <span data-ttu-id="c0820-110">El servidor recibe KRB \_ AP \_ req, descifra el vale y extrae los datos de autorización del usuario y la [*clave de sesión*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="c0820-110">The server receives KRB\_AP\_REQ, decrypts the ticket, and extracts the user's authorization data and the [*session key*](/windows/desktop/SecGloss/s-gly).</span></span>
3.  <span data-ttu-id="c0820-111">El servidor utiliza la clave de sesión del vale para descifrar el mensaje del autenticador del usuario y evalúa la marca de tiempo dentro de.</span><span class="sxs-lookup"><span data-stu-id="c0820-111">The server uses the session key from the ticket to decrypt the user's authenticator message and evaluates the time stamp inside.</span></span>
4.  <span data-ttu-id="c0820-112">Si el mensaje del autenticador es válido, el servidor comprueba la marca de autenticación mutua en la solicitud del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0820-112">If the authenticator message is valid, the server checks the mutual authentication flag in the client's request.</span></span>
5.  <span data-ttu-id="c0820-113">Si se establece la marca de autenticación mutua, el servidor utiliza la clave de sesión para cifrar el tiempo desde el mensaje del autenticador del usuario y devuelve el resultado en un mensaje de tipo KRB \_ AP \_ REP (respuesta de la aplicación Kerberos).</span><span class="sxs-lookup"><span data-stu-id="c0820-113">If the mutual authentication flag is set, the server uses the session key to encrypt the time from the user's authenticator message and returns the result in a message of type KRB\_AP\_REP (Kerberos Application Reply).</span></span>
6.  <span data-ttu-id="c0820-114">Cuando el cliente recibe KRB \_ AP \_ REP, descifra el mensaje del autenticador del servidor con la clave de sesión que comparte con el servidor y compara la hora que devuelve el servicio con la hora del mensaje del autenticador original.</span><span class="sxs-lookup"><span data-stu-id="c0820-114">When the client receives KRB\_AP\_REP, it decrypts the server's authenticator message with the session key it shares with the server and compares the time sent back by the service with the time in its original authenticator message.</span></span> <span data-ttu-id="c0820-115">Si coinciden, el cliente está seguro de que el servicio es original y que la conexión continúa.</span><span class="sxs-lookup"><span data-stu-id="c0820-115">If they match, the client is assured that the service is genuine, and the connection proceeds.</span></span>

 

 
