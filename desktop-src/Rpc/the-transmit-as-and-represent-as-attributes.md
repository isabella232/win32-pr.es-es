---
title: Los atributos transmit_as y represent_as
description: En esta sección se describe la implementación de la conversión de tipos de datos de programador mediante los tipos de datos MIDL \ Transmit \_ as \ y \ representarlos \_ como \.
ms.assetid: 2e1af786-f507-453f-bb10-74805ef6b1a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16760091479a306b9dc9c815c7f3a41b25012ca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904659"
---
# <a name="the-transmit_as-and-represent_as-attributes"></a><span data-ttu-id="e481c-103">Los \_ atributos transmitir como y se representan \_ como</span><span class="sxs-lookup"><span data-stu-id="e481c-103">The transmit\_as and represent\_as Attributes</span></span>

<span data-ttu-id="e481c-104">En esta sección se describe la implementación de la conversión de tipos de datos de programador mediante el uso de MIDL **\[** [**\_ como**](/windows/desktop/Midl/transmit-as) **\]** **\[** [**\_**](/windows/desktop/Midl/represent-as) **\]** atributos.</span><span class="sxs-lookup"><span data-stu-id="e481c-104">This section discusses the implementation of programmer data type conversion using the MIDL **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** and **\[**[**represent\_as**](/windows/desktop/Midl/represent-as)**\]** attributes.</span></span> <span data-ttu-id="e481c-105">La discusión se presenta en las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="e481c-105">The discussion is presented in the following sections:</span></span>

-   [<span data-ttu-id="e481c-106">Atributo de **transmisión \_ como**</span><span class="sxs-lookup"><span data-stu-id="e481c-106">The **transmit\_as** Attribute</span></span>](the-transmit-as-attribute.md)
-   [<span data-ttu-id="e481c-107">Tipo para la función de **\_ \_ transmisión**</span><span class="sxs-lookup"><span data-stu-id="e481c-107">The **type\_to\_xmit** Function</span></span>](the-type-to-xmit-function.md)
-   [<span data-ttu-id="e481c-108">El **tipo \_ de la función de \_ transmisión**</span><span class="sxs-lookup"><span data-stu-id="e481c-108">The **type\_from\_xmit** Function</span></span>](the-type-from-xmit-function.md)
-   [<span data-ttu-id="e481c-109">La función de **\_ \_ transmisión libre de tipos**</span><span class="sxs-lookup"><span data-stu-id="e481c-109">The **type\_free\_xmit** Function</span></span>](the-type-free-xmit-function.md)
-   [<span data-ttu-id="e481c-110">La **función \_ Free \_ inst de tipo**</span><span class="sxs-lookup"><span data-stu-id="e481c-110">The **type\_free\_inst** Function</span></span>](the-type-free-inst-function.md)
-   [<span data-ttu-id="e481c-111">El atributo de **representación \_ como**</span><span class="sxs-lookup"><span data-stu-id="e481c-111">The **represent\_as** Attribute</span></span>](the-represent-as-attribute.md)
-   [<span data-ttu-id="e481c-112">El **tipo con nombre de la función \_ \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="e481c-112">The **named\_type\_from\_local** Function</span></span>](the-named-type-from-local-function.md)
-   [<span data-ttu-id="e481c-113">El **tipo con nombre a la función \_ \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="e481c-113">The **named\_type\_to\_local** Function</span></span>](the-named-type-to-local-function.md)
-   [<span data-ttu-id="e481c-114">La **función \_ \_ \_ local de tipo con nombre Free**</span><span class="sxs-lookup"><span data-stu-id="e481c-114">The **named\_type\_free\_local** Function</span></span>](the-named-type-free-local-function.md)
-   [<span data-ttu-id="e481c-115">Función **\_ \_ \_ inst Free de tipo con nombre**</span><span class="sxs-lookup"><span data-stu-id="e481c-115">The **named\_type\_free\_inst** Function</span></span>](the-named-type-free-inst-function.md)

 

 