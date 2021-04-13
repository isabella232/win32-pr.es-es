---
description: Antes de que el subsistema de tarjeta inteligente pueda encontrar una tarjeta inteligente, la tarjeta inteligente debe incorporarse al sistema.
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: Presentación de tarjetas inteligentes en el sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278572"
---
# <a name="introducing-smart-cards-to-the-system"></a><span data-ttu-id="c5ba8-103">Presentación de tarjetas inteligentes en el sistema</span><span class="sxs-lookup"><span data-stu-id="c5ba8-103">Introducing Smart Cards to the System</span></span>

<span data-ttu-id="c5ba8-104">Antes de que el [*subsistema de tarjeta inteligente*](../secgloss/s-gly.md) pueda encontrar una [*tarjeta inteligente*](../secgloss/s-gly.md), la tarjeta inteligente debe incorporarse al sistema.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-104">Before the [*smart card subsystem*](../secgloss/s-gly.md) can find a [*smart card*](../secgloss/s-gly.md), the smart card must be introduced to the system.</span></span> <span data-ttu-id="c5ba8-105">Normalmente, esto se realiza con una herramienta de configuración de tarjeta inteligente proporcionada por el fabricante de la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-105">This is typically done with a smart card setup tool provided by the card manufacturer.</span></span> <span data-ttu-id="c5ba8-106">La herramienta puede ser un programa en un disquete (con la tarjeta inteligente), un control ActiveX disponible en un sitio web, etc.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-106">The tool could come as a program on a floppy disk (with the smart card), an ActiveX control available on a website, and so on.</span></span>

<span data-ttu-id="c5ba8-107">La herramienta de instalación debe proporcionar los siguientes datos sobre la tarjeta:</span><span class="sxs-lookup"><span data-stu-id="c5ba8-107">The setup tool must provide the following pieces of information about the card:</span></span>

-   <span data-ttu-id="c5ba8-108">Su [*cadena ATR*](../secgloss/a-gly.md)y una máscara opcional que se usará como ayuda para identificar la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-108">Its [*ATR string*](../secgloss/a-gly.md), and an optional mask to use as an aid in identifying the card.</span></span>
-   <span data-ttu-id="c5ba8-109">Una lista de interfaces de tarjeta inteligente que admite la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-109">A list of smart card interfaces supported by the card.</span></span>
-   <span data-ttu-id="c5ba8-110">Nombre para mostrar de la tarjeta que se va a usar para identificar la tarjeta al usuario.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-110">A display name for the card, to be used in identifying the card to the user.</span></span> <span data-ttu-id="c5ba8-111">En la mayoría de los casos, el usuario lo proporcionará a la herramienta de instalación.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-111">In most cases, the user will supply this to the setup tool.</span></span>
-   <span data-ttu-id="c5ba8-112">[*Proveedor de servicios principal*](../secgloss/p-gly.md) asociado a la tarjeta (opcional) que se utilizará al obtener acceso a la tarjeta a través de interfaces com.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-112">The [*primary service provider*](../secgloss/p-gly.md) associated with the card (optional), to be used when accessing the card through COM interfaces.</span></span>

<span data-ttu-id="c5ba8-113">Para simplificar las herramientas de instalación y garantizar la integridad de la [*base de datos de tarjeta inteligente*](../secgloss/s-gly.md), el subsistema de tarjeta inteligente proporciona las dos funciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-113">To simplify setup tools, and to ensure the integrity of the [*smart card database*](../secgloss/s-gly.md), the smart card subsystem provides the following two functions.</span></span> <span data-ttu-id="c5ba8-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduce una tarjeta inteligente en la base de datos y [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) la quita de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c5ba8-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduces a smart card into the database and [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) removes it from the database.</span></span>

 

 
