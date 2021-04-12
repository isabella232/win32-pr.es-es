---
title: Propiedad KeyboardShortcut
description: La propiedad KeyboardShortcut describe una tecla o combinación de teclas que activa un objeto accesible especificado.
ms.assetid: 42587468-f069-4ef1-868e-ac6a285e1715
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002c925151f3f1acc136190d7807d7bc814d30b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268802"
---
# <a name="keyboardshortcut-property"></a><span data-ttu-id="3815b-103">Propiedad KeyboardShortcut</span><span class="sxs-lookup"><span data-stu-id="3815b-103">KeyboardShortcut Property</span></span>

<span data-ttu-id="3815b-104">La propiedad **KeyboardShortcut** describe una tecla o combinación de teclas que activa un objeto accesible especificado.</span><span class="sxs-lookup"><span data-stu-id="3815b-104">The **KeyboardShortcut** property describes a key or key combination that activates a specified accessible object.</span></span>

<span data-ttu-id="3815b-105">La propiedad **KeyboardShortcut** se recupera llamando a [**IAccessible:: get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span><span class="sxs-lookup"><span data-stu-id="3815b-105">The **KeyboardShortcut** property is retrieved by calling [**IAccessible::get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut).</span></span>

<span data-ttu-id="3815b-106">La cadena recuperada describe una *tecla de método abreviado* (también denominada *acelerador de teclado*) o una tecla de acceso (también denominada tecla de *acceso* ). </span><span class="sxs-lookup"><span data-stu-id="3815b-106">The retrieved string describes a *shortcut key* (also called a *keyboard accelerator*) or an *access key* (also called a *mnemonic*).</span></span> <span data-ttu-id="3815b-107">Una tecla de acceso es un carácter subrayado en el texto de un menú, un elemento de menú o una etiqueta de un control, como un botón de inserción.</span><span class="sxs-lookup"><span data-stu-id="3815b-107">An access key is an underlined character in the text of a menu, menu item, or label of a control such as a push button.</span></span>

<span data-ttu-id="3815b-108">La cadena recuperada debe contener el nombre de la clave, junto con la tecla modificadora o las teclas.</span><span class="sxs-lookup"><span data-stu-id="3815b-108">The retrieved string must contain the name of the key along with the modifier key or keys.</span></span> <span data-ttu-id="3815b-109">La cadena debe tener el formato siguiente para que los clientes puedan analizarla con facilidad: el nombre de la clave del \[ \[ modificador. \] + \[ .. \] + \] .</span><span class="sxs-lookup"><span data-stu-id="3815b-109">The string must be in the following format so that clients can easily parse it: \[\[modifier key\]+\[...\]+\] key name.</span></span>

<span data-ttu-id="3815b-110">Entre los ejemplos se incluyen ALT + F, CTRL + ALT + 4, WIN + F1, CTRL + ALT + MAYÚS + retroceso o simplemente retroceso.</span><span class="sxs-lookup"><span data-stu-id="3815b-110">Examples include ALT+F, CTRL+ALT+4, WIN+F1, CTRL+ALT+SHIFT+BACKSPACE, or simply BACKSPACE.</span></span>

<span data-ttu-id="3815b-111">En la tabla siguiente se enumeran las teclas modificadoras.</span><span class="sxs-lookup"><span data-stu-id="3815b-111">The following table lists modifier keys.</span></span>



| <span data-ttu-id="3815b-112">Tecla modificadora</span><span class="sxs-lookup"><span data-stu-id="3815b-112">Modifier key</span></span> | <span data-ttu-id="3815b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3815b-113">Description</span></span>                        |
|--------------|------------------------------------|
| <span data-ttu-id="3815b-114">ALT</span><span class="sxs-lookup"><span data-stu-id="3815b-114">ALT</span></span>          | <span data-ttu-id="3815b-115">Tecla modificadora alternativa</span><span class="sxs-lookup"><span data-stu-id="3815b-115">Alternate modifier key</span></span>             |
| <span data-ttu-id="3815b-116">CTRL</span><span class="sxs-lookup"><span data-stu-id="3815b-116">CTRL</span></span>         | <span data-ttu-id="3815b-117">Tecla modificador de control</span><span class="sxs-lookup"><span data-stu-id="3815b-117">Control modifier key</span></span>               |
| <span data-ttu-id="3815b-118">Mayús</span><span class="sxs-lookup"><span data-stu-id="3815b-118">SHIFT</span></span>        | <span data-ttu-id="3815b-119">Shift (tecla modificador)</span><span class="sxs-lookup"><span data-stu-id="3815b-119">Shift modifier key</span></span>                 |
| <span data-ttu-id="3815b-120">SUERTE</span><span class="sxs-lookup"><span data-stu-id="3815b-120">WIN</span></span>          | <span data-ttu-id="3815b-121">Tecla del logotipo de Windows</span><span class="sxs-lookup"><span data-stu-id="3815b-121">Windows logo key</span></span>                   |
| <span data-ttu-id="3815b-122">FN</span><span class="sxs-lookup"><span data-stu-id="3815b-122">FN</span></span>           | <span data-ttu-id="3815b-123">Tecla de función en equipos portátiles</span><span class="sxs-lookup"><span data-stu-id="3815b-123">Function key on portable computers</span></span> |



 

<span data-ttu-id="3815b-124">No debe localizar cadenas de métodos abreviados de teclado.</span><span class="sxs-lookup"><span data-stu-id="3815b-124">Do not localize keyboard shortcut strings.</span></span>

## <a name="handling-objects-that-have-both-key-types"></a><span data-ttu-id="3815b-125">Controlar objetos que tienen ambos tipos de clave</span><span class="sxs-lookup"><span data-stu-id="3815b-125">Handling Objects That Have Both Key Types</span></span>

<span data-ttu-id="3815b-126">Si un objeto tiene una tecla de método abreviado y una tecla de acceso, la propiedad **KeyboardShortcut** devuelve la tecla de acceso.</span><span class="sxs-lookup"><span data-stu-id="3815b-126">If an object has both a shortcut key and an access key, the **KeyboardShortcut** property returns the access key.</span></span> <span data-ttu-id="3815b-127">La tecla de acceso es la que un usuario presionaría cuando el objeto o el elemento primario del objeto tenga el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="3815b-127">The access key is the one a user would press when the object or the object's parent has the keyboard focus.</span></span> <span data-ttu-id="3815b-128">Por ejemplo, el elemento de menú **Imprimir** puede tener una tecla de método abreviado (Ctrl + P) y una tecla de acceso (P).</span><span class="sxs-lookup"><span data-stu-id="3815b-128">For example, the **Print** menu item might have both a shortcut key (CTRL+P) and an access key (P).</span></span> <span data-ttu-id="3815b-129">Si un usuario presiona CTRL + P mientras el menú está activo, no sucede nada.</span><span class="sxs-lookup"><span data-stu-id="3815b-129">If a user presses CTRL+P while the menu is active, nothing happens.</span></span> <span data-ttu-id="3815b-130">Pero si un usuario presiona P mientras el menú está activo, invoca el cuadro de diálogo **Imprimir** de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3815b-130">But if a user presses P while the menu is active, it invokes the application's **Print** dialog box.</span></span> <span data-ttu-id="3815b-131">En este caso, la propiedad **KeyboardShortcut** es "P" para reflejar lo que el usuario debe presionar cuando el menú tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="3815b-131">In this case, the **KeyboardShortcut** property is "P" to reflect what the user must press when the menu has the keyboard focus.</span></span>

 

 




