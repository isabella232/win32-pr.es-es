---
title: La ventana de caracteres
description: La ventana de caracteres
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421660"
---
# <a name="the-character-window"></a><span data-ttu-id="d0eba-103">La ventana de caracteres</span><span class="sxs-lookup"><span data-stu-id="d0eba-103">The Character Window</span></span>

<span data-ttu-id="d0eba-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d0eba-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="d0eba-105">El agente de Microsoft muestra los caracteres animados en sus propias ventanas que siempre aparecen en la parte superior del orden z de la ventana (es decir, siempre visible).</span><span class="sxs-lookup"><span data-stu-id="d0eba-105">Microsoft Agent displays animated characters in their own windows that always appear at the top of the window z-order (that is, always on top).</span></span> <span data-ttu-id="d0eba-106">Un usuario puede mover la ventana de un carácter arrastrando el carácter con el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="d0eba-106">A user can move a character's window by dragging the character with the left mouse button.</span></span> <span data-ttu-id="d0eba-107">La imagen de caracteres se mueve con el puntero.</span><span class="sxs-lookup"><span data-stu-id="d0eba-107">The character image moves with the pointer.</span></span> <span data-ttu-id="d0eba-108">Además, una aplicación puede desplace un carácter mediante el método [**moveTo**](moveto-method.md) .</span><span class="sxs-lookup"><span data-stu-id="d0eba-108">In addition, an application can move a character using the [**MoveTo**](moveto-method.md) method.</span></span>

<span data-ttu-id="d0eba-109">Cuando el usuario hace clic con el botón secundario en un carácter, aparece un menú emergente que muestra los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="d0eba-109">When the user right-clicks a character, a pop-up menu appears that displays the following commands:</span></span>

<span data-ttu-id="d0eba-110">Abra la \| ventana de comandos cerrar <span class="underline">V</span>oz</span><span class="sxs-lookup"><span data-stu-id="d0eba-110">Open \| Close <span class="underline">V</span>oice Commands Window</span></span>

<span data-ttu-id="d0eba-111">IDE de <span class="underline">H</span></span><span class="sxs-lookup"><span data-stu-id="d0eba-111"><span class="underline">H</span>ide</span></span>

<span data-ttu-id="d0eba-112">----------------------------…</span><span class="sxs-lookup"><span data-stu-id="d0eba-112">----------------------------…</span></span>

<span data-ttu-id="d0eba-113">Get-Help\*</span><span class="sxs-lookup"><span data-stu-id="d0eba-113">Command\*</span></span>


<span data-ttu-id="d0eba-114">*OtherHostingApplicationCaption\*\**</span><span class="sxs-lookup"><span data-stu-id="d0eba-114">*OtherHostingApplicationCaption\*\**</span></span>

<span data-ttu-id="d0eba-115">\*Los comandos enumerados se basan en el cliente de entrada-activo.</span><span class="sxs-lookup"><span data-stu-id="d0eba-115">\*Commands listed are based on the input-active client.</span></span> <span data-ttu-id="d0eba-116">Para obtener más información sobre la definición de comandos que aparecen en el menú emergente, vea la introducción a la interfaz de programación de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="d0eba-116">For more information on defining commands that appear in the pop-up menu, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="d0eba-117">\*\*Las entradas que se muestran son todas las demás aplicaciones que hospedan el carácter actualmente.</span><span class="sxs-lookup"><span data-stu-id="d0eba-117">\*\*Entries listed are all other applications currently hosting the character.</span></span> <span data-ttu-id="d0eba-118">Para obtener más información sobre la definición de esta entrada, vea la introducción a la interfaz de programación del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d0eba-118">For more information on defining this entry, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="d0eba-119">El \| comando abrir cerrar la ventana comandos de voz controla la presentación de la ventana comandos del carácter activo actual.</span><span class="sxs-lookup"><span data-stu-id="d0eba-119">The Open \| Close Voice Commands Window command controls the display of the Commands Window of the current active character.</span></span> <span data-ttu-id="d0eba-120">Si los servicios de reconocimiento de voz están deshabilitados, este comando está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="d0eba-120">If speech recognition services are disabled, this command is disabled.</span></span> <span data-ttu-id="d0eba-121">Si no están instalados los servicios de reconocimiento de voz, este comando no aparece.</span><span class="sxs-lookup"><span data-stu-id="d0eba-121">If speech recognition services are not installed, this command does not appear.</span></span>

<span data-ttu-id="d0eba-122">El comando Hide oculta el carácter.</span><span class="sxs-lookup"><span data-stu-id="d0eba-122">The Hide command hides the character.</span></span> <span data-ttu-id="d0eba-123">La animación asignada al estado **ocultar** del carácter se reproduce y oculta el carácter.</span><span class="sxs-lookup"><span data-stu-id="d0eba-123">The animation assigned to the character's **Hiding** state plays and hides the character.</span></span> <span data-ttu-id="d0eba-124">La letra "H" en Hide es la tecla de acceso del comando (mnemotécnico).</span><span class="sxs-lookup"><span data-stu-id="d0eba-124">The letter "H" in hide is the command's access key (mnemonic).</span></span>

<span data-ttu-id="d0eba-125">Los comandos de las aplicaciones que hospedan el carácter actualmente siguen el comando Hide, precedido por un separador.</span><span class="sxs-lookup"><span data-stu-id="d0eba-125">The commands for the application(s) currently hosting the character follow the Hide command, preceded by a separator.</span></span> <span data-ttu-id="d0eba-126">A continuación, los nombres de otras aplicaciones que utilizan el carácter aparecen, también precedidos por un separador.</span><span class="sxs-lookup"><span data-stu-id="d0eba-126">Then the names of other applications using the character appear, also preceded by a separator.</span></span>

 

 




