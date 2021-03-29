---
title: Propiedad HelpModeOn
description: Propiedad HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776459"
---
# <a name="helpmodeon-property"></a><span data-ttu-id="e7a73-103">Propiedad HelpModeOn</span><span class="sxs-lookup"><span data-stu-id="e7a73-103">HelpModeOn Property</span></span>

<span data-ttu-id="e7a73-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7a73-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="e7a73-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="e7a73-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="e7a73-106">Devuelve o establece si el modo de ayuda contextual está activado para el carácter.</span><span class="sxs-lookup"><span data-stu-id="e7a73-106">Returns or sets whether context-sensitive Help mode is on for the character.</span></span>

</dd> <dt>

<span data-ttu-id="e7a73-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="e7a73-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="e7a73-108">\*agente. ***Caracteres ("*** CharacterID \* *"). HelpModeOn* \*  \[  =  *booleano*\]</span><span class="sxs-lookup"><span data-stu-id="e7a73-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").HelpModeOn** \[ = *boolean*\]</span></span>



| <span data-ttu-id="e7a73-109">Parte</span><span class="sxs-lookup"><span data-stu-id="e7a73-109">Part</span></span>      | <span data-ttu-id="e7a73-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7a73-110">Description</span></span>                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7a73-111">*boolean*</span><span class="sxs-lookup"><span data-stu-id="e7a73-111">*boolean*</span></span> | <span data-ttu-id="e7a73-112">Expresión booleana que especifica si el modo de ayuda contextual está activado.</span><span class="sxs-lookup"><span data-stu-id="e7a73-112">A Boolean expression specifying whether context-sensitive Help mode is on.</span></span> <span data-ttu-id="e7a73-113">**True** El modo de ayuda está activado.</span><span class="sxs-lookup"><span data-stu-id="e7a73-113">**True** Help mode is on.</span></span> <br/> <span data-ttu-id="e7a73-114">**False** (valor predeterminado) el modo de ayuda está desactivado.</span><span class="sxs-lookup"><span data-stu-id="e7a73-114">**False** (Default) Help mode is off.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7a73-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7a73-115">Remarks</span></span>

<span data-ttu-id="e7a73-116">Cuando se establece esta propiedad en **true**, el puntero del mouse cambia a la imagen de ayuda contextual cuando se mueve sobre el carácter o sobre el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="e7a73-116">When you set this property to **True**, the mouse pointer changes to the context-sensitive Help image when moved over the character or over the pop-up menu for the character.</span></span> <span data-ttu-id="e7a73-117">Cuando el usuario hace clic o arrastra el carácter o hace clic en un elemento del menú emergente del carácter, el servidor desencadena el evento [**HelpComplete**](helpcomplete-event.md) y sale del modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="e7a73-117">When the user clicks or drags the character or clicks an item in the character's pop-up menu, the server triggers the [**HelpComplete**](helpcomplete-event.md) event and exits Help mode.</span></span>

<span data-ttu-id="e7a73-118">En el modo de ayuda, el servidor no envía los eventos [**click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)y [**Command**](command-event.md) , a menos que establezca la propiedad [**AutoPopupMenu**](autopopupmenu-property.md) en **true**.</span><span class="sxs-lookup"><span data-stu-id="e7a73-118">In Help mode, the server does not send the [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md), and [**Command**](command-event.md) events, unless you set the [**AutoPopupMenu**](autopopupmenu-property.md) property to **True**.</span></span> <span data-ttu-id="e7a73-119">En ese caso, el servidor enviará el evento de **clic** (no saldrá del modo de ayuda), sino solo el botón secundario del mouse para que pueda mostrar el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="e7a73-119">In that case, the server will send the **Click** event (does not exit Help mode), but only for the right mouse button to enable you to display the pop-up menu.</span></span>

<span data-ttu-id="e7a73-120">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="e7a73-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7a73-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e7a73-121">See Also</span></span>

[<span data-ttu-id="e7a73-122">**Evento HelpComplete**</span><span class="sxs-lookup"><span data-stu-id="e7a73-122">**HelpComplete event**</span></span>](helpcomplete-event.md)


 

 





