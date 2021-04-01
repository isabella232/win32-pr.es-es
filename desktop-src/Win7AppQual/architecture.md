---
description: Internet Explorer de acoplamiento flexible (LCIE) mejora la confiabilidad del explorador separando sus componentes y aflojando sus interdependencias.
ms.assetid: 7609090E-7E2B-4B1F-80FF-192B30A40244
title: Arquitectura (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6edd27246b7b19765288a280bd467de86d2fe50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818467"
---
# <a name="architecture-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="50278-103">Arquitectura (Guía de calidad de la aplicación Windows 7 y Windows Server 2008 R2)</span><span class="sxs-lookup"><span data-stu-id="50278-103">Architecture (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="50278-104">*Internet Explorer de acoplamiento flexible* (LCIE) mejora la confiabilidad del explorador separando sus componentes y aflojando sus interdependencias.</span><span class="sxs-lookup"><span data-stu-id="50278-104">*Loosely-coupled Internet Explorer* (LCIE) improves the browser’s reliability by separating its components and loosening their interdependence.</span></span>

<span data-ttu-id="50278-105">En concreto, LCIE intenta aislar el marco de Windows Internet Explorer y sus pestañas en procesos independientes.</span><span class="sxs-lookup"><span data-stu-id="50278-105">In particular, LCIE tries to isolate the Windows Internet Explorer frame and its tabs into separate processes.</span></span> <span data-ttu-id="50278-106">En Windows Internet Explorer 8, este aislamiento mejora el rendimiento y la escalabilidad.</span><span class="sxs-lookup"><span data-stu-id="50278-106">In Windows Internet Explorer 8, this isolation improves performance and scalability.</span></span> <span data-ttu-id="50278-107">Este cambio arquitectónico puede afectar a la compatibilidad de extensiones y complementos, incluidos los controles ActiveX, los objetos auxiliares del explorador (BHO) y los componentes de la barra de herramientas de la interfaz de usuario que se crean mediante técnicas de programación anteriores.</span><span class="sxs-lookup"><span data-stu-id="50278-107">This architectural change might affect the compatibility of extensions and add-ons, including ActiveX Controls, Browser Helper Objects (BHOs), and UI toolbar components that are built by using older programming techniques.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50278-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50278-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50278-109">Actualizaciones de diseño que afectan a la compatibilidad entre exploradores</span><span class="sxs-lookup"><span data-stu-id="50278-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



