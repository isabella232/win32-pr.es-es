---
description: Una clave maestra es material de datos clave del que se derivan otras claves.
ms.assetid: c8445f74-659a-470b-9007-07ea98d36dcd
title: Crear la clave maestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35a6aef52525bdce622355ede4ae9723f7cd8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541011"
---
# <a name="creating-the-master-key"></a><span data-ttu-id="7eec1-103">Crear la clave maestra</span><span class="sxs-lookup"><span data-stu-id="7eec1-103">Creating the Master Key</span></span>

<span data-ttu-id="7eec1-104">Una [*clave maestra*](../secgloss/m-gly.md) es material de datos clave del que se derivan otras claves.</span><span class="sxs-lookup"><span data-stu-id="7eec1-104">A [*master key*](../secgloss/m-gly.md) is key data material from which other keys are derived.</span></span> <span data-ttu-id="7eec1-105">Según el protocolo y el conjunto de cifrado usado, la clave maestra puede tener entre 5 y 48 bytes de longitud.</span><span class="sxs-lookup"><span data-stu-id="7eec1-105">Depending on the protocol and cipher suite used, the master key can be from 5 to 48 bytes in length.</span></span> <span data-ttu-id="7eec1-106">Para el [](../secgloss/r-gly.md) / CSP [*Schannel*](../secgloss/s-gly.md) de RSA, la clave maestra la crea el lado cliente y se transfiere al servidor en un sobre RSA.</span><span class="sxs-lookup"><span data-stu-id="7eec1-106">For the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) CSP, the master key is created by the client-side and transferred to the server in an RSA envelope.</span></span> <span data-ttu-id="7eec1-107">En el caso de un CSP [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel, la clave maestra se crea mediante la realización de un intercambio de claves Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="7eec1-107">For a [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel CSP, the master key is created by performing a Diffie-Hellman key exchange.</span></span>

<span data-ttu-id="7eec1-108">El código para crear e intercambiar claves maestras se muestra en:</span><span class="sxs-lookup"><span data-stu-id="7eec1-108">Code for creating and exchanging master keys is demonstrated in:</span></span>

-   [<span data-ttu-id="7eec1-109">Código de cliente de Diffie-Hellman para crear la clave maestra</span><span class="sxs-lookup"><span data-stu-id="7eec1-109">Diffie-Hellman Client Code for Creating the Master Key</span></span>](diffie-hellman-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="7eec1-110">Código de servidor Diffie-Hellman para crear la clave maestra</span><span class="sxs-lookup"><span data-stu-id="7eec1-110">Diffie-Hellman Server Code for Creating the Master Key</span></span>](diffie-hellman-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="7eec1-111">Código de cliente de RSA para crear la clave maestra</span><span class="sxs-lookup"><span data-stu-id="7eec1-111">RSA Client Code for Creating the Master Key</span></span>](rsa-client-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="7eec1-112">Código de servidor RSA para crear la clave maestra</span><span class="sxs-lookup"><span data-stu-id="7eec1-112">RSA Server Code for Creating the Master Key</span></span>](rsa-server-code-for-creating-the-master-key.md)
-   [<span data-ttu-id="7eec1-113">Especificar los algoritmos</span><span class="sxs-lookup"><span data-stu-id="7eec1-113">Specifying the Algorithms</span></span>](specifying-the-algorithms.md)

 

 
