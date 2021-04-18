---
description: ATM entra en la categoría de los datos raíz y los planos de control raíz.
ms.assetid: 8e355efe-2903-49c1-a9b3-792b07bd2995
title: Punto de ATM a multipoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba17616feadfe1c8bf87ee8468dd967af73452c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715145"
---
# <a name="atm-point-to-multipoint"></a><span data-ttu-id="450f0-103">Punto de ATM a multipoint</span><span class="sxs-lookup"><span data-stu-id="450f0-103">ATM Point to Multipoint</span></span>

<span data-ttu-id="450f0-104">ATM entra en la categoría de los datos raíz y los planos de control raíz.</span><span class="sxs-lookup"><span data-stu-id="450f0-104">ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="450f0-105">Una aplicación que actúa como raíz crearía \_ Sockets raíz de c y los homólogos que se ejecutan en los nodos hoja usarían \_ sockets de hojas de c.</span><span class="sxs-lookup"><span data-stu-id="450f0-105">An application acting as the root would create c\_root sockets and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="450f0-106">La aplicación raíz usa [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para agregar nuevos nodos hoja.</span><span class="sxs-lookup"><span data-stu-id="450f0-106">The root application uses [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="450f0-107">Las aplicaciones correspondientes en los nodos de hoja habrán establecido sus \_ sockets de hoja de c en modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="450f0-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into listen mode.</span></span> <span data-ttu-id="450f0-108">**WSAJoinLeaf** con un \_ socket raíz de c especificado se asigna al mensaje Q. 2931 ADDPARTY.</span><span class="sxs-lookup"><span data-stu-id="450f0-108">**WSAJoinLeaf** with a c\_root socket specified is mapped to the Q.2931 ADDPARTY message.</span></span> <span data-ttu-id="450f0-109">La combinación iniciada por hoja no se admite en el UNI 3,1 de ATM, pero se admite en la plataforma ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="450f0-109">The leaf-initiated join is not supported in ATM UNI 3.1, but is supported in ATM UNI 4.0.</span></span> <span data-ttu-id="450f0-110">Por lo tanto, **WSAJoinLeaf** con un socket de hoja de c \_ especificado se asigna al mensaje unidireccional 4,0 de ATM adecuado.</span><span class="sxs-lookup"><span data-stu-id="450f0-110">Thus **WSAJoinLeaf** with a c\_leaf socket specified is mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="450f0-111">Existen consideraciones adicionales que se deben tener en cuenta para los puntos de Multipoint ATM:</span><span class="sxs-lookup"><span data-stu-id="450f0-111">There are additional considerations to bear in mind for ATM point-to-multipoint:</span></span>

-   <span data-ttu-id="450f0-112">La adición de nuevas hojas a la sesión de punto a multipunto de ATM solo se basa en la invitación.</span><span class="sxs-lookup"><span data-stu-id="450f0-112">The addition of new leaves to the ATM point-to-multipoint session is invitation-based only.</span></span> <span data-ttu-id="450f0-113">Los invitados raíz salen (que ya tienen la llamada de función [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) ) mediante una llamada a la función [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) .</span><span class="sxs-lookup"><span data-stu-id="450f0-113">The root invites leaves — which have already their [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) function call — by calling the [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) function.</span></span>
-   <span data-ttu-id="450f0-114">El flujo de datos en una sesión de punto a multipunto de ATM es solo de raíz a lugar de salida; las hojas no pueden usar la misma sesión para enviar información a la raíz.</span><span class="sxs-lookup"><span data-stu-id="450f0-114">The flow of data in an ATM point-to-multipoint session is from root-to-leaves only; leaves cannot use the same session to send information to the root.</span></span>
-   <span data-ttu-id="450f0-115">Solo se permite una hoja por cada adaptador ATM.</span><span class="sxs-lookup"><span data-stu-id="450f0-115">Only one leaf per ATM adapter is allowed.</span></span>

 

 



