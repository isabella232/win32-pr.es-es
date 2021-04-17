---
description: .
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Usar la etiqueta meta para garantizar compatibilidad futura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e965711053a7108c69295ac737953a05536a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717301"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a><span data-ttu-id="8896c-103">Usar la etiqueta meta para garantizar compatibilidad futura</span><span class="sxs-lookup"><span data-stu-id="8896c-103">Use the Meta Tag to Ensure Future Compatibility</span></span>

<span data-ttu-id="8896c-104">Windows Internet Explorer 8 le permite controlar los modos de compatibilidad de documentos, por lo que puede indicar al explorador que represente las páginas web de la misma manera que las versiones anteriores del explorador.</span><span class="sxs-lookup"><span data-stu-id="8896c-104">Windows Internet Explorer 8 enables you to control document compatibility modes, so you can instruct the browser to render webpages in the same way as older browser versions.</span></span> <span data-ttu-id="8896c-105">También puede elegir cuándo actualizar la página web, mientras sigue siendo utilizable y funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="8896c-105">You can also choose when to update the webpage, while it continues to be usable and function correctly.</span></span>

## <a name="setting-the-meta-element"></a><span data-ttu-id="8896c-106">Establecer el elemento meta</span><span class="sxs-lookup"><span data-stu-id="8896c-106">Setting the Meta Element</span></span>

<span data-ttu-id="8896c-107">El elemento **meta** incluye un atributo de **contenido** que le permite especificar el modo en el que se representa el contenido para la página web, como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="8896c-107">The **meta** element includes a **content** attribute that enables you to specify the mode that content is rendered in for the webpage, as the following table shows.</span></span>



| <span data-ttu-id="8896c-108">Value</span><span class="sxs-lookup"><span data-stu-id="8896c-108">Value</span></span> | <span data-ttu-id="8896c-109">Modo de representación</span><span class="sxs-lookup"><span data-stu-id="8896c-109">Rendering mode</span></span>                                                 |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="8896c-110">IE = 9</span><span class="sxs-lookup"><span data-stu-id="8896c-110">IE=9</span></span>  | <span data-ttu-id="8896c-111">Usar el modo de representación de estándares de Windows Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="8896c-111">Use the Windows Internet Explorer 9 standards rendering mode</span></span>   |
| <span data-ttu-id="8896c-112">IE = 8</span><span class="sxs-lookup"><span data-stu-id="8896c-112">IE=8</span></span>  | <span data-ttu-id="8896c-113">Usar el modo de representación de estándares de Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="8896c-113">Use the Internet Explorer 8 standards rendering mode</span></span>           |
| <span data-ttu-id="8896c-114">IE = 7</span><span class="sxs-lookup"><span data-stu-id="8896c-114">IE=7</span></span>  | <span data-ttu-id="8896c-115">Usar el modo de representación de estándares de Windows Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="8896c-115">Use the Windows Internet Explorer 7 standards rendering mode</span></span>   |
| <span data-ttu-id="8896c-116">IE=5</span><span class="sxs-lookup"><span data-stu-id="8896c-116">IE=5</span></span>  | <span data-ttu-id="8896c-117">Usar el modo de representación de estándares de Microsoft Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="8896c-117">Use the Microsoft Internet Explorer 5 standards rendering mode</span></span> |



 

<span data-ttu-id="8896c-118">Para obtener más información sobre la compatibilidad y el encabezado X-UA-compatible, vea [definir la compatibilidad de documentos](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) en MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="8896c-118">For more information about compatibility and the X-UA-Compatible header, see [Defining Document Compatibility](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in the MSDN Library.</span></span>

<span data-ttu-id="8896c-119">En el ejemplo de código siguiente se muestra cómo forzar la representación de una página web en el modo Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="8896c-119">The following code example demonstrates how to force a webpage to be rendered in Internet Explorer 8 mode.</span></span>


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a><span data-ttu-id="8896c-120">Usar un encabezado HTTP</span><span class="sxs-lookup"><span data-stu-id="8896c-120">Using an HTTP Header</span></span>

<span data-ttu-id="8896c-121">Muchos sitios web contienen miles (o decenas de miles) de páginas web individuales, por lo que no resulta práctico establecer el elemento **meta** en cada documento.</span><span class="sxs-lookup"><span data-stu-id="8896c-121">Many websites contain thousands (or tens of thousands) of individual webpages so setting the **meta** element on each document is impractical.</span></span> <span data-ttu-id="8896c-122">Si desea establecer el elemento **meta** para todas las páginas o una colección de páginas seleccionadas por carpeta, puede ajustar la configuración del servidor en su lugar y agregar los metadatos compatibles con X-UA en el [encabezado HTTP](/previous-versions/cc817572(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="8896c-122">If you want to set the **meta** element for all pages or a collection of pages that are selected by folder, you can adjust your server configuration instead and add the X-UA-Compatible metadata in the [HTTP header](/previous-versions/cc817572(v=msdn.10)).</span></span>

<span data-ttu-id="8896c-123">En el caso de los sitios que requieren diferentes valores de elemento **meta** para las páginas del mismo servidor, hay varias herramientas que generan e insertan automáticamente el elemento **meta** adecuado.</span><span class="sxs-lookup"><span data-stu-id="8896c-123">For sites that require different **meta** element values for pages on the same server, there are several tools that automatically generate and insert the appropriate **meta** element for you.</span></span> <span data-ttu-id="8896c-124">Por ejemplo, la utilidad de [herramientas Web de ArtInSoft](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) de Aggiorno inserta y quita la característica de etiqueta de compatibilidad de Internet Explorer 8 y puede ayudar a su sitio a cumplir estándares de compatibilidad específicos.</span><span class="sxs-lookup"><span data-stu-id="8896c-124">For example, the [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) utility from Aggiorno inserts and removes the Internet Explorer 8 compatibility tag feature and can help your site meet specific compatibility standards.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8896c-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8896c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8896c-126">Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="8896c-126">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
