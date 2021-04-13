---
title: Propiedad DefaultAction
description: La propiedad DefaultAction de un objeto describe el método principal de manipulación del objeto desde el punto de vista del usuario. La propiedad DefaultAction de un objeto debe ser un verbo o una frase de verbo corta.
ms.assetid: 8242c0af-b42e-44a4-8807-d6740fa1a24a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73dc032037c331a2022f227cb8e8547dd8bce9d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356815"
---
# <a name="defaultaction-property"></a><span data-ttu-id="c6590-104">Propiedad DefaultAction</span><span class="sxs-lookup"><span data-stu-id="c6590-104">DefaultAction Property</span></span>

<span data-ttu-id="c6590-105">La propiedad **DEFAULTACTION** de un objeto describe el método principal de manipulación del objeto desde el punto de vista del usuario.</span><span class="sxs-lookup"><span data-stu-id="c6590-105">An object's **DefaultAction** property describes the object's primary method of manipulation from the user's viewpoint.</span></span> <span data-ttu-id="c6590-106">La propiedad **DEFAULTACTION** de un objeto debe ser un verbo o una frase de verbo corta.</span><span class="sxs-lookup"><span data-stu-id="c6590-106">An object's **DefaultAction** property should be a verb or a short verb phrase.</span></span>

<span data-ttu-id="c6590-107">La propiedad **DEFAULTACTION** se recupera llamando a [**IAccessible:: get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span><span class="sxs-lookup"><span data-stu-id="c6590-107">The **DefaultAction** property is retrieved by calling [**IAccessible::get\_accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction).</span></span>

<span data-ttu-id="c6590-108">Para realizar la acción predeterminada de un objeto, los clientes llaman a [**IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span><span class="sxs-lookup"><span data-stu-id="c6590-108">To perform an object's default action, clients call [**IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction).</span></span>

<span data-ttu-id="c6590-109">No todos los objetos tienen acciones predeterminadas y algunos objetos tienen una acción predeterminada relacionada con su propiedad [**Value**](value-property.md) , como en los ejemplos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c6590-109">Not all objects have default actions, and some objects have a default action that is related to its [**Value**](value-property.md) property, such as in the following examples:</span></span>

-   <span data-ttu-id="c6590-110">Una casilla seleccionada tiene una acción predeterminada de "desactivar" y un valor de "activado".</span><span class="sxs-lookup"><span data-stu-id="c6590-110">A selected check box has a default action of "Uncheck" and a value of "Checked."</span></span>
-   <span data-ttu-id="c6590-111">Una casilla desactivada tiene una acción predeterminada de "comprobar" y un valor de "desactivada".</span><span class="sxs-lookup"><span data-stu-id="c6590-111">A cleared check box has a default action of "Check" and a value of "Unchecked."</span></span>
-   <span data-ttu-id="c6590-112">Un botón con la etiqueta "Imprimir" tiene una acción predeterminada de "presionar", sin ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c6590-112">A button labeled "Print" has a default action of "Press," with no value.</span></span>
-   <span data-ttu-id="c6590-113">Un control de texto estático o un control de edición que muestra "Printer" no tiene ninguna acción predeterminada, pero tiene un valor de "Printer".</span><span class="sxs-lookup"><span data-stu-id="c6590-113">A static text control or an edit control that shows "Printer" has no default action, but has a value of "Printer."</span></span>

 

 




