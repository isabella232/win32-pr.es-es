---
description: Control de versiones (Guía de calidad de aplicaciones de Windows 7 y Windows Server 2008 R2)
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Control de versiones (Guía de calidad de aplicaciones de Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c3bc1f63dc236c706fd8d9bd6a6053371dd363
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103703"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="a1e71-103">Control de versiones (Guía de calidad de aplicaciones de Windows 7 y Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="a1e71-103">Versioning (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="a1e71-104">Uno de los problemas de compatibilidad de aplicaciones más comunes para Windows Internet Explorer cadenas del Agente de usuario (UA) y vectores de versión.</span><span class="sxs-lookup"><span data-stu-id="a1e71-104">One of the most common application compatibility issues for Windows Internet Explorer is User Agent (UA) Strings and Version Vectors.</span></span> <span data-ttu-id="a1e71-105">Windows Internet Explorer 8 presenta una nueva cadena ua para ayudar a las aplicaciones a detectar qué versión están ejecutando los usuarios.</span><span class="sxs-lookup"><span data-stu-id="a1e71-105">Windows Internet Explorer 8 introduces a new UA String to help applications detect which version that users are running.</span></span> <span data-ttu-id="a1e71-106">Además de aumentar simplemente el valor MSIE asociado a Internet Explorer en la cadena UA, Internet Explorer 8 agrega un valor Trident/4.0 para ayudarle a detectar si Internet Explorer 8 se ejecuta en modo Vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="a1e71-106">In addition to simply increasing the MSIE value that is associated with Internet Explorer in the UA String, Internet Explorer 8 adds a Trident/4.0 value to help you detect if Internet Explorer 8 is running in Compatibility View mode.</span></span> <span data-ttu-id="a1e71-107">Estos cambios, además de las comprobaciones de versiones codificadas de forma rígida, pueden presentar problemas de compatibilidad entre exploradores.</span><span class="sxs-lookup"><span data-stu-id="a1e71-107">These changes, plus hardcoded version checks, can potentially introduce compatibility issues between browsers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1e71-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a1e71-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1e71-109">Diseñar actualizaciones que afectan a la compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="a1e71-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



