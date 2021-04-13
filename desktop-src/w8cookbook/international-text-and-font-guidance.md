---
title: Guía de texto y fuentes internacionales
description: Guía de texto y fuentes internacionales
ms.assetid: 0540C9AD-8774-4F0F-B013-48C3EAE59BF2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2f9d94c53e4db45666d28a7c23a0e883043ba27
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420732"
---
# <a name="international-text-and-font-guidance"></a><span data-ttu-id="afffe-103">Guía de texto y fuentes internacionales</span><span class="sxs-lookup"><span data-stu-id="afffe-103">International text and font guidance</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="afffe-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="afffe-104">Affected Platforms</span></span>

<dl> <span data-ttu-id="afffe-105">Clientes: Windows 8 \| Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="afffe-105">Clients - Windows 8 \| Windows 8.1</span></span>  
<span data-ttu-id="afffe-106">Servidores: Windows Server 2012 \| Windows server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="afffe-106">Servers - Windows Server 2012 \| Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="afffe-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="afffe-107">Description</span></span>

<span data-ttu-id="afffe-108">Como antes de Windows 2000, se ha agregado compatibilidad con la presentación de texto para nuevos scripts en cada versión principal de Windows.</span><span class="sxs-lookup"><span data-stu-id="afffe-108">Since before Windows 2000, text-display support for new scripts has been added in each major release of Windows.</span></span> <span data-ttu-id="afffe-109">Puede encontrar descripciones de los cambios realizados en cada versión principal en el artículo [compatibilidad con fuentes y scripts para Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) en el [centro de desarrollo de go global](https://msdn.microsoft.com/goglobal/default).</span><span class="sxs-lookup"><span data-stu-id="afffe-109">You can find descriptions of the changes made in each major release in the [Script and Font Support for Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx) article at the [Go Global Development Center](https://msdn.microsoft.com/goglobal/default).</span></span>

<span data-ttu-id="afffe-110">Tenga en cuenta que la compatibilidad con un script puede requerir ciertos cambios en los componentes de la pila de texto, así como los cambios en las fuentes.</span><span class="sxs-lookup"><span data-stu-id="afffe-110">Note that support for a script may require certain changes to text stack components as well as changes to fonts.</span></span> <span data-ttu-id="afffe-111">El sistema operativo Windows tiene muchos componentes de pila de texto: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32 y otros.</span><span class="sxs-lookup"><span data-stu-id="afffe-111">The Windows operating system has many text stack components: DirectWrite, GDI, Uniscribe, GDI+, WPF, RichEdit, ComCtl32, and others.</span></span> <span data-ttu-id="afffe-112">La información proporcionada pertenece principalmente a GDI y a DirectWrite.</span><span class="sxs-lookup"><span data-stu-id="afffe-112">The information provided pertains primarily to GDI and DirectWrite.</span></span> <span data-ttu-id="afffe-113">También se aplica a los marcos de interfaz de usuario, como RichEdit o el agente de representación de MSHTML, que se usan para las aplicaciones de la tienda de Windows 8 y para representar el contenido Web, aunque dichos componentes pueden presentar ciertas diferencias.</span><span class="sxs-lookup"><span data-stu-id="afffe-113">It is also generally applicable to UI frameworks such as RichEdit or the MSHTML rendering agent used for Windows 8 Store apps and for rendering web content, though those components may exhibit certain differences.</span></span>

## <a name="best-practices"></a><span data-ttu-id="afffe-114">Prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="afffe-114">Best Practices</span></span>

<span data-ttu-id="afffe-115">**Orientación tipográfica para desarrolladores**</span><span class="sxs-lookup"><span data-stu-id="afffe-115">**Typography guidance for developers**</span></span>

<span data-ttu-id="afffe-116">La tipografía está en el corazón del lenguaje de diseño de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="afffe-116">Typography is at the heart of the Microsoft design language.</span></span> <span data-ttu-id="afffe-117">Cada uno de los principios de diseño de Microsoft refuerza la importancia de la tipografía.</span><span class="sxs-lookup"><span data-stu-id="afffe-117">Each of the Microsoft design principles reinforces the importance of typography.</span></span> <span data-ttu-id="afffe-118">Por primera vez, los desarrolladores de aplicaciones tienen un conjunto de marcos que admiten características tipográficas avanzadas.</span><span class="sxs-lookup"><span data-stu-id="afffe-118">For the first time, app developers have a set of frameworks that support advanced typographic features.</span></span> <span data-ttu-id="afffe-119">Vaya a [Mostrar y editar texto](/previous-versions/windows/apps/hh465442(v=win.10)) para obtener información sobre cómo usar JavaScript y HTML para mostrar y editar texto en aplicaciones de la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="afffe-119">Go to [Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10)) for information about how to use JavaScript and HTML to display and edit text in Windows Store apps.</span></span>

<span data-ttu-id="afffe-120">**Métricas de fuentes**</span><span class="sxs-lookup"><span data-stu-id="afffe-120">**Font metrics**</span></span>

<span data-ttu-id="afffe-121">Las métricas de fuente son un área de importancia especial para los desarrolladores de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="afffe-121">Font metrics are an area of particular importance to application developers.</span></span> <span data-ttu-id="afffe-122">Los archivos de fuente contienen varios valores relacionados con las métricas verticales y horizontales.</span><span class="sxs-lookup"><span data-stu-id="afffe-122">Font files contain various values related to vertical and horizontal metrics.</span></span> <span data-ttu-id="afffe-123">Estos valores están documentados en la [especificación OpenType](https://www.microsoft.com/typography/otspec/) y se exponen a través de una variedad de API que se encuentran en la [estructura de \_ \_ métricas de fuentes DWRITE](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) y en la [estructura TEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span><span class="sxs-lookup"><span data-stu-id="afffe-123">These values are documented in the [OpenType specification](https://www.microsoft.com/typography/otspec/) and these are exposed via a variety of APIs found at [DWRITE\_FONT\_METRICS structure](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) and at [TEXTMETRIC Structure](/windows/win32/api/wingdi/ns-wingdi-textmetrica).</span></span>

## <a name="resources"></a><span data-ttu-id="afffe-124">Recursos</span><span class="sxs-lookup"><span data-stu-id="afffe-124">Resources</span></span>

-   [<span data-ttu-id="afffe-125">Compatibilidad con scripts y fuentes para Windows</span><span class="sxs-lookup"><span data-stu-id="afffe-125">Script and Font Support for Windows</span></span>](https://msdn.microsoft.com/goglobal/bb688099.aspx)
-   [<span data-ttu-id="afffe-126">Vaya al centro de desarrollo global</span><span class="sxs-lookup"><span data-stu-id="afffe-126">Go Global Development Center</span></span>](https://msdn.microsoft.com/goglobal/default)
-   <span data-ttu-id="afffe-127">[Mostrar y editar texto](/previous-versions/windows/apps/hh465442(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="afffe-127">[Displaying and editing text](/previous-versions/windows/apps/hh465442(v=win.10))</span></span>
-   [<span data-ttu-id="afffe-128">Especificación OpenType</span><span class="sxs-lookup"><span data-stu-id="afffe-128">OpenType specification</span></span>](https://www.microsoft.com/typography/otspec/)
-   [<span data-ttu-id="afffe-129">DWRITE \_ estructura de las \_ métricas de fuente</span><span class="sxs-lookup"><span data-stu-id="afffe-129">DWRITE\_FONT\_METRICS structure</span></span>](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)
-   [<span data-ttu-id="afffe-130">Estructura TEXTMETRIC</span><span class="sxs-lookup"><span data-stu-id="afffe-130">TEXTMETRIC Structure</span></span>](/windows/win32/api/wingdi/ns-wingdi-textmetrica)

 

 