---
title: El objeto Balloon
description: El objeto Balloon
ms.assetid: d5b52310-0b4e-4fe3-a481-53687be4a89c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0c94803e9efadde1ae4a8410273ed49437291a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104270905"
---
# <a name="the-balloon-object"></a><span data-ttu-id="89623-103">El objeto Balloon</span><span class="sxs-lookup"><span data-stu-id="89623-103">The Balloon Object</span></span>

<span data-ttu-id="89623-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="89623-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="89623-105">El agente de Microsoft admite la subtítulos de texto del método [**Speak**](speak-method.md) mediante un globo de palabras de dibujo.</span><span class="sxs-lookup"><span data-stu-id="89623-105">Microsoft Agent supports textual captioning of [**Speak**](speak-method.md) method using a cartoon word balloon.</span></span> <span data-ttu-id="89623-106">El método de [**reflexión**](think-method.md) le permite mostrar texto sin salida de audio en un globo de palabra "pensamiento".</span><span class="sxs-lookup"><span data-stu-id="89623-106">The [**Think**](think-method.md) method enables you to display text without audio output in a "thought" word balloon.</span></span>

<span data-ttu-id="89623-107">Los valores predeterminados de la ventana de globo de palabras iniciales de un carácter se definen y compilan en el editor de caracteres del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="89623-107">A character's initial word balloon window defaults are defined and compiled in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="89623-108">Una vez que se ejecuta, el usuario puede invalidar las propiedades [**habilitadas**](enabled-property.md) y de [**fuente**](https://www.bing.com/search?q=**Font**) del globo.</span><span class="sxs-lookup"><span data-stu-id="89623-108">Once running, the balloon's [**Enabled**](enabled-property.md) and [**Font**](https://www.bing.com/search?q=**Font**) properties may be overridden by the user.</span></span> <span data-ttu-id="89623-109">Si un usuario cambia las propiedades del globo de palabras, afectan a todos los caracteres.</span><span class="sxs-lookup"><span data-stu-id="89623-109">If a user changes the word balloon's properties, they affect all characters.</span></span> <span data-ttu-id="89623-110">Tanto el globo de palabras [**Speak**](speak-method.md) como el de [**reflexión**](think-method.md) usan la misma configuración de propiedades para el tamaño.</span><span class="sxs-lookup"><span data-stu-id="89623-110">Both the [**Speak**](speak-method.md) and [**Think**](think-method.md) word balloons use the same property settings for size.</span></span> <span data-ttu-id="89623-111">Puede tener acceso a las propiedades del globo de palabras de un carácter a través del objeto de [**globo**](/windows/desktop/lwef/the-balloon-object) , que es un elemento secundario del objeto de [**carácter**](/windows/desktop/lwef/the-characters-object) .</span><span class="sxs-lookup"><span data-stu-id="89623-111">You can access the properties for a character's word balloon through the [**Balloon**](/windows/desktop/lwef/the-balloon-object) object, which is a child of the [**Character**](/windows/desktop/lwef/the-characters-object) object.</span></span>

<span data-ttu-id="89623-112">El objeto [**Balloon**](/windows/desktop/lwef/the-balloon-object) admite las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="89623-112">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object supports the following properties:</span></span>

-   [<span data-ttu-id="89623-113">**BackColor**</span><span class="sxs-lookup"><span data-stu-id="89623-113">**BackColor**</span></span>](backcolor-property.md)
-   [<span data-ttu-id="89623-114">**BorderColor**</span><span class="sxs-lookup"><span data-stu-id="89623-114">**BorderColor**</span></span>](bordercolor-property.md)
-   [<span data-ttu-id="89623-115">**CharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="89623-115">**CharsPerLine**</span></span>](charsperline-property.md)
-   [<span data-ttu-id="89623-116">**habilitado**</span><span class="sxs-lookup"><span data-stu-id="89623-116">**Enabled**</span></span>](enabled-property.md)
-   [<span data-ttu-id="89623-117">**FontCharSet**</span><span class="sxs-lookup"><span data-stu-id="89623-117">**FontCharSet**</span></span>](fontcharset-property.md)
-   [<span data-ttu-id="89623-118">**FontName**</span><span class="sxs-lookup"><span data-stu-id="89623-118">**FontName**</span></span>](fontname-property-bal.md)
-   [<span data-ttu-id="89623-119">**FontBold**</span><span class="sxs-lookup"><span data-stu-id="89623-119">**FontBold**</span></span>](fontbold-property.md)
-   [<span data-ttu-id="89623-120">**FontItalic**</span><span class="sxs-lookup"><span data-stu-id="89623-120">**FontItalic**</span></span>](fontitalic-property.md)
-   [<span data-ttu-id="89623-121">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="89623-121">**FontSize**</span></span>](fontsize-property-bal.md)
-   [<span data-ttu-id="89623-122">**FontStrikeThru**</span><span class="sxs-lookup"><span data-stu-id="89623-122">**FontStrikeThru**</span></span>](fontstrikethru-property.md)
-   [<span data-ttu-id="89623-123">**FontUnderline**</span><span class="sxs-lookup"><span data-stu-id="89623-123">**FontUnderline**</span></span>](fontunderline-property.md)
-   [<span data-ttu-id="89623-124">**ForeColor**</span><span class="sxs-lookup"><span data-stu-id="89623-124">**ForeColor**</span></span>](forecolor-property.md)
-   [<span data-ttu-id="89623-125">**NumberOfLines**</span><span class="sxs-lookup"><span data-stu-id="89623-125">**NumberOfLines**</span></span>](numberoflines-property.md)
-   [<span data-ttu-id="89623-126">**Estilo**</span><span class="sxs-lookup"><span data-stu-id="89623-126">**Style**</span></span>](style-property.md)
-   [<span data-ttu-id="89623-127">**Visible**</span><span class="sxs-lookup"><span data-stu-id="89623-127">**Visible**</span></span>](visible-property-bal.md)

 

 