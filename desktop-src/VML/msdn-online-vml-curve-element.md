---
title: Elemento Curve de VML
description: Elemento Curve de VML
ms.assetid: 37197ef0-7597-465a-bc37-7ffcde2e736b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15b9e04086652bf9dde7d7e7f5ebdea0992f774c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271278"
---
# <a name="vml-curve-element"></a><span data-ttu-id="971d9-103">Elemento Curve de VML</span><span class="sxs-lookup"><span data-stu-id="971d9-103">VML Curve Element</span></span>

<span data-ttu-id="971d9-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="971d9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="971d9-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="971d9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="971d9-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="971d9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="971d9-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="971d9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="971d9-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="971d9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="971d9-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="971d9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="971d9-110">Forma de curva predefinida.</span><span class="sxs-lookup"><span data-stu-id="971d9-110">Predefined curve shape.</span></span>

<span data-ttu-id="971d9-111">La **curva** usa los atributos [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [Control1](msdn-online-vml-control1-attribute.md)y [control2](msdn-online-vml-control2-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="971d9-111">**Curve** uses the [to](to-attribute--curve--vml.md), [from](from-attribute--curve--vml.md), [control1](msdn-online-vml-control1-attribute.md), and [control2](msdn-online-vml-control2-attribute.md) attributes.</span></span>

<span data-ttu-id="971d9-112">A continuación se encuentra el código mínimo necesario para generar una imagen.</span><span class="sxs-lookup"><span data-stu-id="971d9-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:curve
   from="10pt,10pt" to="100pt,10pt"
   control1="40pt,30pt" control2="70pt,30pt">
   </v:curve>
```





 

 