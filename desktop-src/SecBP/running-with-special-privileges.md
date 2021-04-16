---
description: Algunas funciones requieren privilegios especiales para ejecutarse correctamente.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Ejecutar con privilegios especiales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669739"
---
# <a name="running-with-special-privileges"></a><span data-ttu-id="2e1dd-103">Ejecutar con privilegios especiales</span><span class="sxs-lookup"><span data-stu-id="2e1dd-103">Running with Special Privileges</span></span>

<span data-ttu-id="2e1dd-104">Algunas funciones requieren [privilegios](/windows/desktop/SecAuthZ/privileges) especiales para ejecutarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-104">Some functions require special [privileges](/windows/desktop/SecAuthZ/privileges) to run correctly.</span></span> <span data-ttu-id="2e1dd-105">En algunos casos, la función solo puede ser ejecutada por determinados usuarios o por miembros de determinados grupos.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-105">In some cases, the function can only be run by certain users or by members of certain groups.</span></span> <span data-ttu-id="2e1dd-106">El requisito más común es que el usuario sea un administrador local.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-106">The most common requirement is that the user be a local administrator.</span></span> <span data-ttu-id="2e1dd-107">Otras funciones requieren que la cuenta del usuario tenga habilitados los privilegios específicos.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-107">Other functions require the user's account to have specific privileges enabled.</span></span>

<span data-ttu-id="2e1dd-108">Para reducir la posibilidad de que el código no autorizado pueda obtener el control, el sistema debe ejecutarse con los privilegios mínimos necesarios.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-108">To reduce the possibility of unauthorized code being able to get control, the system should run with the least privilege necessary.</span></span> <span data-ttu-id="2e1dd-109">Las aplicaciones que necesitan llamar a funciones que requieren privilegios especiales pueden dejar el sistema abierto para atacar a los hackers.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-109">Applications that need to call functions that require special privileges can leave the system open to attack by hackers.</span></span> <span data-ttu-id="2e1dd-110">Dichas aplicaciones deben diseñarse para que se ejecuten durante breves períodos de tiempo y deben informar al usuario de las implicaciones de seguridad implicadas.</span><span class="sxs-lookup"><span data-stu-id="2e1dd-110">Such applications should be designed to run for short periods of time and should inform the user of the security implications involved.</span></span>

<span data-ttu-id="2e1dd-111">Para obtener información sobre cómo ejecutar como usuarios diferentes y cómo habilitar los privilegios en la aplicación, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2e1dd-111">For information about how to run as different users and how to enable privileges in your application, see the following topics:</span></span><dl>

[<span data-ttu-id="2e1dd-112">Ejecutar con privilegios de administrador</span><span class="sxs-lookup"><span data-stu-id="2e1dd-112">Running with Administrator Privileges</span></span>](running-with-administrator-privileges.md)  
[<span data-ttu-id="2e1dd-113">Solicitar credenciales al usuario</span><span class="sxs-lookup"><span data-stu-id="2e1dd-113">Asking the User for Credentials</span></span>](asking-the-user-for-credentials.md)  
[<span data-ttu-id="2e1dd-114">Cambiar los privilegios de un token</span><span class="sxs-lookup"><span data-stu-id="2e1dd-114">Changing Privileges in a Token</span></span>](changing-privileges-in-a-token.md)  
[<span data-ttu-id="2e1dd-115">Asignación de privilegios a una cuenta</span><span class="sxs-lookup"><span data-stu-id="2e1dd-115">Assigning Privileges to an Account</span></span>](assigning-privileges-to-an-account.md)  
</dl>

 

 
