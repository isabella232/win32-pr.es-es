---
title: Requisitos de seguridad de la función de administración de red
description: La llamada a algunas de las funciones de administración de red no requiere la pertenencia al grupo especial.
ms.assetid: 846a5b81-d5bf-4275-a898-38e6ba308b8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b0987509294f03b8737aae5e721abf5dbdd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533423"
---
# <a name="network-management-function-security-requirements"></a><span data-ttu-id="328c1-103">Requisitos de seguridad de la función de administración de red</span><span class="sxs-lookup"><span data-stu-id="328c1-103">Network management function security requirements</span></span>

<span data-ttu-id="328c1-104">La llamada a algunas de las funciones de administración de red no requiere la pertenencia al grupo especial.</span><span class="sxs-lookup"><span data-stu-id="328c1-104">Calling some of the network management functions does not require special group membership.</span></span> <span data-ttu-id="328c1-105">Otras funciones requieren que los usuarios tengan un nivel de privilegios específico para ejecutarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="328c1-105">Other functions require that users have a specific privilege level to execute successfully.</span></span> <span data-ttu-id="328c1-106">Cuando sea aplicable, en la sección Comentarios de la página de referencia de una función se indica el nivel de privilegios que debe tener un usuario para ejecutar la función concreta.</span><span class="sxs-lookup"><span data-stu-id="328c1-106">When applicable, the Remarks section on a function's reference page indicates the privilege level a user must have to execute the particular function.</span></span>

<span data-ttu-id="328c1-107">Los requisitos de seguridad que se aplican a los controladores de dominio de Active Directory pueden diferir de los que se aplican a los servidores y las estaciones de trabajo.</span><span class="sxs-lookup"><span data-stu-id="328c1-107">Security requirements that apply to Active Directory domain controllers can differ from those that apply to servers and workstations.</span></span>

<span data-ttu-id="328c1-108">Para obtener más información y una lista de las funciones afectadas, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="328c1-108">For more information, and a list of affected functions, see the following topics:</span></span>

-   [<span data-ttu-id="328c1-109">Requisitos de las funciones de administración de red en los controladores de dominio de Active Directory</span><span class="sxs-lookup"><span data-stu-id="328c1-109">Requirements for Network Management functions on Active Directory domain controllers</span></span>](requirements-for-network-management-functions-on-active-directory-domain-controllers.md)
-   [<span data-ttu-id="328c1-110">Requisitos para las funciones de administración de redes en servidores y estaciones de trabajo</span><span class="sxs-lookup"><span data-stu-id="328c1-110">Requirements for Network Management functions on servers and workstations</span></span>](requirements-for-network-management-functions-on-servers-and-workstations.md)

<span data-ttu-id="328c1-111">Para obtener más información sobre cómo controlar el acceso a los objetos protegibles, vea [Access Control](/windows/desktop/SecAuthZ/access-control), [privilegios](/windows/desktop/SecAuthZ/privileges)y [objetos protegibles](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="328c1-111">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span>

<span data-ttu-id="328c1-112">Para obtener más información acerca de los descriptores de seguridad específicos que se usan durante las comprobaciones de acceso, vea la página de referencia de funciones individuales.</span><span class="sxs-lookup"><span data-stu-id="328c1-112">For more information about specific security descriptors that are used during access checks, see the individual function reference page.</span></span> <span data-ttu-id="328c1-113">Para obtener más información sobre cómo llamar a funciones que requieran privilegios de administrador, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="328c1-113">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 