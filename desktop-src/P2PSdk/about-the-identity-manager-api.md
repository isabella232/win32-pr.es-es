---
description: La API del administrador de identidades del mismo nivel permite crear, enumerar y manipular identidades del mismo nivel en una aplicación del mismo nivel.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Acerca de Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909793"
---
# <a name="about-identity-manager"></a><span data-ttu-id="00d75-103">Acerca de Identity Manager</span><span class="sxs-lookup"><span data-stu-id="00d75-103">About Identity Manager</span></span>

<span data-ttu-id="00d75-104">La API del administrador de identidades del mismo nivel permite crear, enumerar y manipular identidades del mismo nivel en una aplicación del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="00d75-104">The Peer Identity Manager API allows you to create, enumerate, and manipulate peer identities in a peer application.</span></span> <span data-ttu-id="00d75-105">Puede usar las identidades del mismo nivel creadas con esta API como entrada para las API del proveedor de espacios de nombres del Protocolo de resolución de nombres de mismo nivel (PNRP) y de agrupación del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="00d75-105">You can use the peer identities created using this API as input for the Peer Grouping and Peer Name Resolution Protocol (PNRP) Namespace Provider APIs.</span></span>

## <a name="peer-identity-manager-best-practices"></a><span data-ttu-id="00d75-106">Prácticas recomendadas para el administrador de identidades del mismo nivel</span><span class="sxs-lookup"><span data-stu-id="00d75-106">Peer Identity Manager Best Practices</span></span>

<span data-ttu-id="00d75-107">Cada usuario debe tener algunas identidades del mismo nivel que pueden usar para las actividades del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="00d75-107">Each user should have a few peer identities that they can use for the peer activities.</span></span> <span data-ttu-id="00d75-108">Por ejemplo, un usuario podría tener dos identidades del mismo nivel para trabajo y ocio.</span><span class="sxs-lookup"><span data-stu-id="00d75-108">For example, a user might have two peer identities for work and leisure.</span></span>

<span data-ttu-id="00d75-109">Una aplicación del mismo nivel bien diseñada permite al usuario seleccionar la identidad del mismo nivel que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="00d75-109">A well-designed peer application allows a user to select a peer identity to use.</span></span> <span data-ttu-id="00d75-110">Un usuario puede crear una nueva identidad del mismo nivel si ninguna de las identidades del mismo nivel existente es adecuada para usarla con una aplicación.</span><span class="sxs-lookup"><span data-stu-id="00d75-110">A user can create a new peer identity if none of the existing peer identities are appropriate to use with an application.</span></span>

<span data-ttu-id="00d75-111">Una aplicación del mismo nivel bien diseñada también controla el número de identidades que crea.</span><span class="sxs-lookup"><span data-stu-id="00d75-111">A well-designed peer application also controls the number of identities that it creates.</span></span> <span data-ttu-id="00d75-112">Si una aplicación crea una identidad del mismo nivel temporal, la aplicación debe eliminar la identidad del mismo nivel cuando no se necesita la identidad.</span><span class="sxs-lookup"><span data-stu-id="00d75-112">If an application creates a temporary peer identity, the application must delete the peer identity when the identity is not needed.</span></span> <span data-ttu-id="00d75-113">Si una aplicación no realiza este mantenimiento, es posible que el administrador de identidad del mismo nivel no pueda crear identidades del mismo nivel hasta que se quiten algunas identidades del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="00d75-113">If an application does not perform this maintenance, the Peer Identity Manager may not be able to create peer identities until some peer identities are removed.</span></span>

 

 



