---
description: LSA almacena la información de la Directiva de seguridad local en un conjunto de objetos. La aplicación puede consultar o editar la Directiva de seguridad local mediante el acceso a estos objetos.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Objetos de directiva de LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002075"
---
# <a name="lsa-policy-objects"></a><span data-ttu-id="3991a-104">Objetos de directiva de LSA</span><span class="sxs-lookup"><span data-stu-id="3991a-104">LSA Policy Objects</span></span>

<span data-ttu-id="3991a-105">LSA almacena la información de la Directiva de seguridad local en un conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="3991a-105">The LSA stores local security policy information in a set of objects.</span></span> <span data-ttu-id="3991a-106">La aplicación puede consultar o editar la Directiva de seguridad local mediante el acceso a estos objetos.</span><span class="sxs-lookup"><span data-stu-id="3991a-106">Your application can query or edit the local security policy by accessing these objects.</span></span>

<span data-ttu-id="3991a-107">El conjunto consta de los cuatro objetos siguientes:</span><span class="sxs-lookup"><span data-stu-id="3991a-107">The set consists of the following four objects:</span></span>

-   <span data-ttu-id="3991a-108">La [Directiva](policy-object.md) contiene información global de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="3991a-108">[Policy](policy-object.md) contains global policy information.</span></span>
-   <span data-ttu-id="3991a-109">[TrustedDomain](trusteddomain-object.md) contiene información sobre un dominio de confianza.</span><span class="sxs-lookup"><span data-stu-id="3991a-109">[TrustedDomain](trusteddomain-object.md) contains information about a trusted domain.</span></span>
-   <span data-ttu-id="3991a-110">[Cuenta](account-object.md) contiene información acerca de un usuario, grupo o cuenta de grupo local.</span><span class="sxs-lookup"><span data-stu-id="3991a-110">[Account](account-object.md) contains information about a user, group, or local group account.</span></span>
-   <span data-ttu-id="3991a-111">Los [datos privados](private-data-object.md) contienen información protegida, como las contraseñas de las cuentas de servidor.</span><span class="sxs-lookup"><span data-stu-id="3991a-111">[Private Data](private-data-object.md) contains protected information, such as server account passwords.</span></span> <span data-ttu-id="3991a-112">Esta información se almacena como cadenas cifradas.</span><span class="sxs-lookup"><span data-stu-id="3991a-112">This information is stored as encrypted strings.</span></span>

<span data-ttu-id="3991a-113">Para obtener más información sobre cómo usar las funciones de directiva de LSA para administrar la información almacenada en estos objetos, vea uso de la [Directiva de LSA](using-lsa-policy.md).</span><span class="sxs-lookup"><span data-stu-id="3991a-113">For more information on how to use the LSA Policy functions to manage the information stored in these objects, see [Using LSA Policy](using-lsa-policy.md).</span></span>

 

 



