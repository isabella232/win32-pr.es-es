---
title: Detección del reproductor
description: Detección del reproductor
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player tiendas en línea, detectar jugadores
- tiendas en línea, detectar jugadores
- tipo 1 tiendas en línea, detección de reproductores
- tipo 2 tiendas en línea, detección de reproductores
- Windows Media Player tiendas en línea, detección del reproductor
- tiendas en línea, detección del reproductor
- tipo 1 almacenes en línea, detección del reproductor
- tipo 2 tiendas en línea, detección del reproductor
- detección del reproductor
- detección de reproductores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994305"
---
# <a name="detecting-the-player"></a><span data-ttu-id="07a5c-113">Detección del reproductor</span><span class="sxs-lookup"><span data-stu-id="07a5c-113">Detecting the Player</span></span>

<span data-ttu-id="07a5c-114">Al crear una página web para la tienda en línea, puede decidir que quiere que los usuarios puedan ver la página en un explorador Web o en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="07a5c-114">When creating a webpage for your online store, you may decide that you want users to be able to view the page in a Web browser or in Windows Media Player.</span></span> <span data-ttu-id="07a5c-115">Puede usar un script de ASP para determinar si la página web está hospedada en el reproductor.</span><span class="sxs-lookup"><span data-stu-id="07a5c-115">You can use an ASP script to determine whether your webpage is hosted in the Player.</span></span>

<span data-ttu-id="07a5c-116">En el código de ejemplo siguiente se recupera el parámetro de versión de la cadena de consulta de dirección URL para determinar si la página se hospeda en Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="07a5c-116">The following example code retrieves the version parameter from the URL query string to determine whether the page is hosted in Windows Media Player:</span></span>


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



<span data-ttu-id="07a5c-117">Tenga en cuenta que en el código anterior se supone que el parámetro Version existe en la cadena de consulta cuando se hospeda en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="07a5c-117">Note that the preceding code assumes that the version parameter exists in the query string when hosted in Windows Media Player.</span></span> <span data-ttu-id="07a5c-118">Esto es así para las páginas abiertas por el usuario, pero puede que no sea cierto para las páginas abiertas mediante **external. NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="07a5c-118">This is true for pages opened by the user, but may not be true for pages opened by using **External.NavigateTaskPaneURL**.</span></span> <span data-ttu-id="07a5c-119">Para que la cadena de consulta de la versión exista al navegar mediante programación, debe agregar el parámetro Version a la llamada al método o anexar dinámicamente la versión a la dirección URL base del elemento **Navigate** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="07a5c-119">For the version query string to exist when navigating programmatically, you must add the version parameter to the method call or dynamically append the version to the base URL of the **Navigate** element of your ServiceInfo document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07a5c-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="07a5c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a5c-121">**Creación dinámica del documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="07a5c-121">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="07a5c-122">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="07a5c-122">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="07a5c-123">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="07a5c-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




