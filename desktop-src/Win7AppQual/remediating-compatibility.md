---
description: Compatibilidad de DEP/NX
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilidad de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b46c9143ee96b8599c10d4c70276d36e20a08
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116443"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="2471c-103">Compatibilidad de DEP/NX</span><span class="sxs-lookup"><span data-stu-id="2471c-103">DEP/NX compatibility</span></span>

<span data-ttu-id="2471c-104">De forma predeterminada, en Windows Internet Explorer 7, DEP/NX está deshabilitado por motivos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="2471c-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="2471c-105">Varios complementos populares no son compatibles con DEP/NX y se producirá un error cuando Windows Internet Explorer los cargue con DEP/NX habilitado.</span><span class="sxs-lookup"><span data-stu-id="2471c-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="2471c-106">Normalmente, estos complementos se construyen mediante una versión anterior del marco ATL.</span><span class="sxs-lookup"><span data-stu-id="2471c-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="2471c-107">ATL 7.1 y versiones anteriores no están diseñados con la característica de seguridad DEP.</span><span class="sxs-lookup"><span data-stu-id="2471c-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="2471c-108">Afortunadamente, las nuevas versiones de Service Pack de Microsoft Windows tienen nuevas API de DEP/NX que le permiten usar DEP/NX y conservar la compatibilidad con versiones anteriores de ATL.</span><span class="sxs-lookup"><span data-stu-id="2471c-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="2471c-109">Estas nuevas API permiten a Internet Explorer participar en DEP/NX sin provocar un error en los complementos creados mediante versiones anteriores de ATL.</span><span class="sxs-lookup"><span data-stu-id="2471c-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="2471c-110">Cuando un complemento no es compatible con DEP/NX y no usa un ATL obsoleto, puede usar una opción de directiva de grupo para no participar en DEP/NX para Internet Explorer hasta que se implemente una versión actualizada del control roto.</span><span class="sxs-lookup"><span data-stu-id="2471c-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="2471c-111">Los administradores locales pueden controlar DEP/NX ejecutando Internet Explorer como  administrador y desactivando  la opción Habilitar protección de memoria en el panel Opciones **avanzadas de Internet**.</span><span class="sxs-lookup"><span data-stu-id="2471c-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2471c-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2471c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2471c-113">Corregir problemas de compatibilidad en aplicaciones web mediante Vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="2471c-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
