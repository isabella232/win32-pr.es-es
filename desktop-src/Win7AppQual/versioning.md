---
description: .
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Control de versiones (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2da50dae53fd2309f1a5de10996c57a2b4ac29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707493"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="37b1c-103">Control de versiones (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="37b1c-103">Versioning (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="37b1c-104">Uno de los problemas de compatibilidad de aplicaciones más comunes para Windows Internet Explorer son las cadenas de agente de usuario (UA) y los vectores de versión.</span><span class="sxs-lookup"><span data-stu-id="37b1c-104">One of the most common application compatibility issues for Windows Internet Explorer is User Agent (UA) Strings and Version Vectors.</span></span> <span data-ttu-id="37b1c-105">Windows Internet Explorer 8 introduce una nueva cadena de UA para ayudar a las aplicaciones a detectar qué versión están ejecutando los usuarios.</span><span class="sxs-lookup"><span data-stu-id="37b1c-105">Windows Internet Explorer 8 introduces a new UA String to help applications detect which version that users are running.</span></span> <span data-ttu-id="37b1c-106">Además de simplemente aumentar el valor de MSIE que está asociado con Internet Explorer en la cadena UA, Internet Explorer 8 agrega un valor Trident/4.0 para ayudarle a detectar si Internet Explorer 8 se está ejecutando en modo de vista de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="37b1c-106">In addition to simply increasing the MSIE value that is associated with Internet Explorer in the UA String, Internet Explorer 8 adds a Trident/4.0 value to help you detect if Internet Explorer 8 is running in Compatibility View mode.</span></span> <span data-ttu-id="37b1c-107">Estos cambios, además de las comprobaciones de versión codificadas, pueden introducir problemas de compatibilidad entre exploradores.</span><span class="sxs-lookup"><span data-stu-id="37b1c-107">These changes, plus hardcoded version checks, can potentially introduce compatibility issues between browsers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37b1c-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37b1c-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37b1c-109">Actualizaciones de diseño que afectan a la compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="37b1c-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



