---
title: Elemento de arco VML
description: Elemento de arco VML
ms.assetid: 46b5b78a-9a69-432b-9008-0ce7a658b9dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd35d59349e10f38495807ceb3f08dc254c117e2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359361"
---
# <a name="vml-arc-element"></a><span data-ttu-id="8980c-103">Elemento de arco VML</span><span class="sxs-lookup"><span data-stu-id="8980c-103">VML Arc Element</span></span>

<span data-ttu-id="8980c-104">En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8980c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8980c-105">Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.</span><span class="sxs-lookup"><span data-stu-id="8980c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8980c-106">A partir del 2011 de diciembre, este tema se ha archivado.</span><span class="sxs-lookup"><span data-stu-id="8980c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8980c-107">Como resultado, ya no se mantiene de forma activa.</span><span class="sxs-lookup"><span data-stu-id="8980c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8980c-108">Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8980c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8980c-109">Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8980c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8980c-110">Forma de arco predefinida.</span><span class="sxs-lookup"><span data-stu-id="8980c-110">Predefined arc shape.</span></span>

<span data-ttu-id="8980c-111">**Arc** usa [los atributos](msdn-online-vml-endangle-attribute.md) [startAngle](msdn-online-vml-startangle-attribute.md) y imponed.</span><span class="sxs-lookup"><span data-stu-id="8980c-111">**Arc** uses the [startangle](msdn-online-vml-startangle-attribute.md) and [endangle](msdn-online-vml-endangle-attribute.md) attributes.</span></span>

<span data-ttu-id="8980c-112">A continuación se encuentra el código mínimo necesario para generar una imagen.</span><span class="sxs-lookup"><span data-stu-id="8980c-112">The following is the minimum code needed to produce an image.</span></span>


```HTML
   <v:arc
   style="top:10;left:10;width:200;height:200"
   startangle="90" endangle="270">
   </v:arc>
```





 

 