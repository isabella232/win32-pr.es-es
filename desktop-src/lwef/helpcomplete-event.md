---
title: Evento HelpComplete
description: Evento HelpComplete
ms.assetid: d805f089-154f-4b39-9d78-a02b732f87ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3984f4b67eaed6bc9226685e927c35e151c11e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695593"
---
# <a name="helpcomplete-event"></a><span data-ttu-id="69d46-103">Evento HelpComplete</span><span class="sxs-lookup"><span data-stu-id="69d46-103">HelpComplete Event</span></span>

<span data-ttu-id="69d46-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="69d46-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="69d46-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="69d46-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="69d46-106">Indica que se ha salido del modo de ayuda contextual.</span><span class="sxs-lookup"><span data-stu-id="69d46-106">Indicates that context-sensitive Help mode has been exited.</span></span>

</dd> <dt>

<span data-ttu-id="69d46-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="69d46-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="69d46-108">**Sub** *Agent. \* \* \* (ByVal* \*  \*CharacterID \* *, ByVal* \*  \*nombre \* \* *, ByVal* \*  *causa \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="69d46-108">**Sub** *agent.\*\*\*(ByVal*\* *CharacterID\*\*\*, ByVal*\* *Name\*\*\*, ByVal*\* *Cause\*\*\*)*\*</span></span>



| <span data-ttu-id="69d46-109">Parte</span><span class="sxs-lookup"><span data-stu-id="69d46-109">Part</span></span>          | <span data-ttu-id="69d46-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="69d46-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69d46-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="69d46-111">*CharacterID*</span></span> | <span data-ttu-id="69d46-112">Devuelve el identificador del carácter en el que se hizo clic como una cadena.</span><span class="sxs-lookup"><span data-stu-id="69d46-112">Returns the ID of the clicked character as a string.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="69d46-113">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="69d46-113">*Name*</span></span>        | <span data-ttu-id="69d46-114">Devuelve un valor de cadena que identifica el nombre (ID.) del comando.</span><span class="sxs-lookup"><span data-stu-id="69d46-114">Returns a string value identifying the name (ID) of the command.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="69d46-115">*Causa*</span><span class="sxs-lookup"><span data-stu-id="69d46-115">*Cause*</span></span>       | <span data-ttu-id="69d46-116">Devuelve un valor que indica lo que hizo que se completara el modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="69d46-116">Returns a value that indicates what caused the Help mode to complete.</span></span> <span data-ttu-id="69d46-117">1 el usuario seleccionó un comando proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="69d46-117">1 The user selected a command supplied by your application.</span></span><br/> <span data-ttu-id="69d46-118">2 el usuario seleccionó el objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) de otro cliente.</span><span class="sxs-lookup"><span data-stu-id="69d46-118">2 The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span><br/> <span data-ttu-id="69d46-119">3 el usuario seleccionó el comando abrir comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="69d46-119">3 The user selected the Open Voice Commands command.</span></span><br/> <span data-ttu-id="69d46-120">4 el usuario seleccionó el comando cerrar comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="69d46-120">4 The user selected the Close Voice Commands command.</span></span><br/> <span data-ttu-id="69d46-121">5 el usuario seleccionó el comando show *nombredecarácter* .</span><span class="sxs-lookup"><span data-stu-id="69d46-121">5 The user selected the Show *CharacterName* command.</span></span><br/> <span data-ttu-id="69d46-122">6 el usuario seleccionó el comando ocultar *nombredecarácter* .</span><span class="sxs-lookup"><span data-stu-id="69d46-122">6 The user selected the Hide *CharacterName* command.</span></span><br/> <span data-ttu-id="69d46-123">7 el usuario seleccionó (hizo clic en) el carácter.</span><span class="sxs-lookup"><span data-stu-id="69d46-123">7 The user selected (clicked) the character.</span></span><br/> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="69d46-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69d46-124">Remarks</span></span>

<span data-ttu-id="69d46-125">Normalmente, el modo de ayuda se completa cuando el usuario hace clic o arrastra el carácter o selecciona un comando en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="69d46-125">Typically, Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="69d46-126">Al hacer clic en otro carácter o en cualquier otro lugar de la pantalla, no se cancela el modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="69d46-126">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="69d46-127">El cliente que establece el modo de ayuda para el carácter puede cancelar el modo de ayuda estableciendo [**HelpModeOn**](helpmodeon-property.md) en **false**.</span><span class="sxs-lookup"><span data-stu-id="69d46-127">The client that set Help mode for the character can cancel Help mode by setting [**HelpModeOn**](helpmodeon-property.md) to **False**.</span></span> <span data-ttu-id="69d46-128">(Esto no desencadena el evento **HelpComplete** ).</span><span class="sxs-lookup"><span data-stu-id="69d46-128">(This does not trigger the **HelpComplete** event.)</span></span>

<span data-ttu-id="69d46-129">Cuando el usuario selecciona un comando en el menú emergente del carácter en el modo de ayuda, el servidor quita el menú, llama a ayuda con el [**HelpContextID**](helpcontextid-property.md)especificado del comando y envía este evento.</span><span class="sxs-lookup"><span data-stu-id="69d46-129">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="69d46-130">La información contextual (también conocida como esto?) La ventana de ayuda se muestra en la ubicación del puntero.</span><span class="sxs-lookup"><span data-stu-id="69d46-130">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="69d46-131">Si el usuario selecciona el comando por entrada de voz, se muestra la ventana de ayuda sobre el carácter.</span><span class="sxs-lookup"><span data-stu-id="69d46-131">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="69d46-132">Si el carácter está fuera de la pantalla, la ventana se muestra en la pantalla más cercana a la posición actual del carácter.</span><span class="sxs-lookup"><span data-stu-id="69d46-132">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="69d46-133">Si el servidor devuelve el nombre como una cadena vacía (""), indica que el usuario seleccionó un comando proporcionado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="69d46-133">If the server returns Name as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="69d46-134">Este evento solo se envía a la aplicación cliente que coloca el carácter en modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="69d46-134">This event is sent only to the client application that places the character in Help mode.</span></span>

### <a name="see-also"></a><span data-ttu-id="69d46-135">Consulte también</span><span class="sxs-lookup"><span data-stu-id="69d46-135">See Also</span></span>

<span data-ttu-id="69d46-136">[**Propiedad HelpModeOn**](helpmodeon-property.md), [ **propiedad HelpContextID**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="69d46-136">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

