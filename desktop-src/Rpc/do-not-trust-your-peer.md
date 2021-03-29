---
title: No confíe en su equipo del mismo nivel
description: '\ 0034; no confíe en su equipo del mismo nivel \ 0034; es una regla de seguridad básica, pero a menudo se pasa por alto.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775499"
---
# <a name="do-not-trust-your-peer"></a><span data-ttu-id="3503c-103">No confíe en su equipo del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="3503c-103">Do Not Trust Your Peer</span></span>

<span data-ttu-id="3503c-104">"No confiar en el equipo del mismo nivel" es una regla de seguridad básica, pero a menudo se pasa por alto.</span><span class="sxs-lookup"><span data-stu-id="3503c-104">"Do not trust your peer" is a basic security rule, but it is often overlooked.</span></span> <span data-ttu-id="3503c-105">No asuma que la otra parte de una comunicación se comportará correctamente y no asumirá que el homólogo pasará los datos esperados.</span><span class="sxs-lookup"><span data-stu-id="3503c-105">Do not assume the other party in a communication will behave properly, and do not assume your peer will pass the data you expect.</span></span> <span data-ttu-id="3503c-106">MIDL y RPC realizan algunas comprobaciones en su nombre, pero no todas las comprobaciones.</span><span class="sxs-lookup"><span data-stu-id="3503c-106">MIDL and RPC perform some checks on your behalf, but not all checks.</span></span>

<span data-ttu-id="3503c-107">Sepa qué aspecto de los parámetros se comprueban mediante MIDL o RPC, y qué aspectos debe comprobar usted mismo.</span><span class="sxs-lookup"><span data-stu-id="3503c-107">Know which aspect of the parameters are verified by MIDL or RPC, and which aspects you must verify yourself.</span></span> <span data-ttu-id="3503c-108">Por ejemplo, para los identificadores de contexto in/out, RPC comprueba que el identificador de contexto no es un valor no NULL válido.</span><span class="sxs-lookup"><span data-stu-id="3503c-108">For example, for in/out context handles, RPC verifies the context handle is not an invalid non-null value.</span></span> <span data-ttu-id="3503c-109">Permite valores NULL y valores válidos, pero muchos desarrolladores no saben que los valores NULL se permiten.</span><span class="sxs-lookup"><span data-stu-id="3503c-109">It allows null values and valid values, but many developers are not aware that null values are let through.</span></span> <span data-ttu-id="3503c-110">Esto es algo que se debe comprobar.</span><span class="sxs-lookup"><span data-stu-id="3503c-110">This is something to check for.</span></span>

<span data-ttu-id="3503c-111">Aunque en general confíe en el equipo del mismo nivel, asegúrese de no introducir nuevas rutas de acceso por las que una máquina principal o máquina en peligro puede atacar a otras máquinas.</span><span class="sxs-lookup"><span data-stu-id="3503c-111">Even if you generally trust your peer, be sure not to introduce new paths by which a compromised machine or principal account can attack other machines.</span></span> <span data-ttu-id="3503c-112">Imagine que un usuario elige su cumpleaños como su contraseña y lo adivina un atacante.</span><span class="sxs-lookup"><span data-stu-id="3503c-112">Imagine that a user chooses his birthday as his password, and it is guessed by an attacker.</span></span> <span data-ttu-id="3503c-113">Incluso después de que se autentiquen las solicitudes del usuario y se permita el acceso a sus datos, asegúrese de que las vulnerabilidades explotables no existan, como saturaciones de la pila, lo que puede permitir que un atacante tome el control del servidor y amplíe la brecha de seguridad.</span><span class="sxs-lookup"><span data-stu-id="3503c-113">Even after requests from the user are authenticated and access to his data is allowed, make sure exploitable vulnerabilities do not exist, such stack overruns that may allow an attacker to take control of your server and extend the security breach.</span></span>

 

 




