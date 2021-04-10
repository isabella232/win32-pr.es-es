---
title: Scripting de objetos COM en aplicaciones personalizadas
description: Scripting de objetos COM en aplicaciones personalizadas
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268664"
---
# <a name="scripting-com-objects-in-custom-applications"></a><span data-ttu-id="d509d-103">Scripting de objetos COM en aplicaciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="d509d-103">Scripting COM Objects in Custom Applications</span></span>

<span data-ttu-id="d509d-104">Microsoft proporciona varios entornos para el scripting de objetos COM: páginas Active Server, Windows Script Host, etc.</span><span class="sxs-lookup"><span data-stu-id="d509d-104">Microsoft provides several environments for scripting COM objects: Active Server Pages, Windows Script Host, and so on.</span></span> <span data-ttu-id="d509d-105">Los fabricantes de software independientes (ISV) también pueden conceder licencias a los motores de scripting de Microsoft para su uso en sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="d509d-105">Independent software vendors (ISVs) can also license Microsoft scripting engines for use in their applications.</span></span> <span data-ttu-id="d509d-106">Por ejemplo, un ISV que crea un procesador de textos podría querer agregar un lenguaje de macros a la aplicación para que los usuarios puedan automatizar las tareas sencillas.</span><span class="sxs-lookup"><span data-stu-id="d509d-106">For example, an ISV creating a word processor might want to add a macro language to the application so users could automate simple tasks.</span></span> <span data-ttu-id="d509d-107">Mediante el uso de la licencia de un motor de scripting, el ISV puede usar un lenguaje como VBScript o JScript como lenguaje de macros de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d509d-107">By licensing a scripting engine, the ISV can use a language such as VBScript or JScript as the application's macro language.</span></span>

<span data-ttu-id="d509d-108">Además de las licencias de los motores de scripting de VBScript y JScript, los ISV pueden escribir sus propios motores de scripting ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d509d-108">In addition to licensing VBScript and JScript scripting engines, ISVs can write their own ActiveX scripting engines.</span></span> <span data-ttu-id="d509d-109">Estos motores de scripts se pueden conectar a cualquier entorno de host que admita el estándar del motor de scripting de ActiveX.</span><span class="sxs-lookup"><span data-stu-id="d509d-109">These scripting engines can then be plugged into any host environment that supports the ActiveX scripting engine standard.</span></span> <span data-ttu-id="d509d-110">Por ejemplo, un ISV puede escribir un motor de scripts de PerlScript e instalarlo en un servidor ASP, lo que permite al servidor ASP procesar scripts PerlScript.</span><span class="sxs-lookup"><span data-stu-id="d509d-110">For example, an ISV might write a PerlScript scripting engine and install it on an ASP server, thus enabling the ASP server to process PerlScript scripts.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d509d-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d509d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d509d-112">Scripting con objetos COM</span><span class="sxs-lookup"><span data-stu-id="d509d-112">Scripting with COM Objects</span></span>](scripting-with-com-objects.md)
</dt> </dl>

 

 




