---
description: En función de la taxonomía definida para los esquemas multidifusión y multidifusión independientes del Protocolo de Windows Sockets 2, ATM entra en la categoría de los datos raíz y los planos de control raíz.
ms.assetid: 309afa65-2cc4-4b7b-9968-4c4efb2d10a3
title: Detalles de la función ATM de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e82ca0531272490c2d3189467186535a63d6ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155252"
---
# <a name="winsock-atm-function-details"></a><span data-ttu-id="a9f49-103">Detalles de la función ATM de Winsock</span><span class="sxs-lookup"><span data-stu-id="a9f49-103">Winsock ATM Function Details</span></span>

<span data-ttu-id="a9f49-104">En función de la taxonomía definida para los esquemas multidifusión y multidifusión independientes del Protocolo de Windows Sockets 2, ATM entra en la categoría de los datos raíz y los planos de control raíz.</span><span class="sxs-lookup"><span data-stu-id="a9f49-104">Based on the taxonomy defined for Windows Sockets 2 protocol-independent multipoint/multicast schemes, ATM falls into the category of rooted data and rooted control planes.</span></span> <span data-ttu-id="a9f49-105">(Consulte la especificación de la API de Windows Sockets 2, Apéndice D para obtener más información). Una aplicación que actúa como raíz crearía \_ Sockets raíz de c y los homólogos que se ejecutan en los nodos hoja usarían \_ sockets de hojas de c.</span><span class="sxs-lookup"><span data-stu-id="a9f49-105">(See the Windows Sockets 2 API Specification, Appendix D for more information.) An application acting as the root would create c\_root sockets, and counterparts running on leaf nodes would utilize c\_leaf sockets.</span></span> <span data-ttu-id="a9f49-106">La aplicación raíz usará [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) para agregar nuevos nodos hoja.</span><span class="sxs-lookup"><span data-stu-id="a9f49-106">The root application will use [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) to add new leaf nodes.</span></span> <span data-ttu-id="a9f49-107">Las aplicaciones correspondientes en los nodos hoja habrán establecido sus \_ sockets de hoja c en el modo de escucha.</span><span class="sxs-lookup"><span data-stu-id="a9f49-107">The corresponding applications on the leaf nodes will have set their c\_leaf sockets into the listening mode.</span></span> <span data-ttu-id="a9f49-108">**WSAJoinLeaf** con un \_ socket raíz de c especificado se asignará al mensaje de instalación Q. 2931 (para la primera hoja) o al mensaje de agregar entidad (para cualquier salida subsiguiente).</span><span class="sxs-lookup"><span data-stu-id="a9f49-108">**WSAJoinLeaf** with a c\_root socket specified will be mapped to the Q.2931 SETUP message (for the first leaf) or ADD PARTY message (for any subsequent leaves).</span></span>

> [!Note]  
> <span data-ttu-id="a9f49-109">Los parámetros de QoS especificados en **WSAJoinLeaf** para cualquier salida subsiguiente deben omitirse según la especificación UNI del Foro de ATM.</span><span class="sxs-lookup"><span data-stu-id="a9f49-109">The QoS parameters specified in **WSAJoinLeaf** for any subsequent leaves should be ignored per the ATM Forum UNI specification.</span></span>

 

<span data-ttu-id="a9f49-110">La combinación iniciada por hojas no forma parte del nodo ATM UNI 3,1, pero se admite en la plataforma ATM UNI 4,0.</span><span class="sxs-lookup"><span data-stu-id="a9f49-110">The leaf-initiated join is not part of the ATM UNI 3.1, but is supported in the ATM UNI 4.0.</span></span> <span data-ttu-id="a9f49-111">Por lo tanto, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) con un socket de hoja de c \_ especificado se puede asignar al mensaje unidireccional 4,0 de ATM adecuado.</span><span class="sxs-lookup"><span data-stu-id="a9f49-111">Thus [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) with a c\_leaf socket specified can be mapped to the appropriate ATM UNI 4.0 message.</span></span>

<span data-ttu-id="a9f49-112">El parámetro AAL y la negociación B-LLI se admiten a través de la modificación de la s correspondiente en el parámetro *lpSQOS* después de la invocación de la función de condición especificada en [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span><span class="sxs-lookup"><span data-stu-id="a9f49-112">The AAL Parameter and B-LLI negotiation is supported through the modification of the corresponding IEs in the *lpSQOS* parameter upon the invocation of the condition function specified in [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept).</span></span>

> [!Note]  
> <span data-ttu-id="a9f49-113">Solo se pueden modificar ciertos campos de esas dos s.</span><span class="sxs-lookup"><span data-stu-id="a9f49-113">Only certain fields in those two IEs can be modified.</span></span> <span data-ttu-id="a9f49-114">Consulte el Apéndice C y el Apéndice F del Foro de ATM para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="a9f49-114">See the ATM Forum UNI specification Appendix C and Appendix F for details.</span></span>

 

 

 



