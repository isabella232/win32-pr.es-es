---
description: .
ms.assetid: 18F74BA7-2729-4EB3-8E6F-4E5A8C17C317
title: Compatibilidad de DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb542331d218ed4c493efde091be3e5efae6aee
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717365"
---
# <a name="depnx-compatibility"></a><span data-ttu-id="7037e-103">Compatibilidad de DEP/NX</span><span class="sxs-lookup"><span data-stu-id="7037e-103">DEP/NX compatibility</span></span>

<span data-ttu-id="7037e-104">De forma predeterminada, en Windows Internet Explorer 7, DEP/NX está deshabilitado por motivos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="7037e-104">By default, in Windows Internet Explorer 7, DEP/NX is disabled for compatibility reasons.</span></span> <span data-ttu-id="7037e-105">Varios complementos populares no son compatibles con DEP/NX y producen un error cuando Windows Internet Explorer los carga con DEP/NX habilitado.</span><span class="sxs-lookup"><span data-stu-id="7037e-105">Several popular add-ons are not compatible with DEP/NX and fail when Windows Internet Explorer loads them with DEP/NX enabled.</span></span>

<span data-ttu-id="7037e-106">Normalmente, estos complementos se compilan con una versión anterior del marco ATL.</span><span class="sxs-lookup"><span data-stu-id="7037e-106">Typically, these add-ons are built by using an older version of the ATL framework.</span></span> <span data-ttu-id="7037e-107">ATL 7,1 y versiones anteriores no están diseñadas con la característica de seguridad de DEP.</span><span class="sxs-lookup"><span data-stu-id="7037e-107">ATL 7.1 and earlier versions are not designed with the DEP security feature.</span></span> <span data-ttu-id="7037e-108">Afortunadamente, las nuevas versiones de Microsoft Windows Service Pack tienen nuevas API de DEP/NX que le permiten usar DEP/NX y conservar la compatibilidad con versiones anteriores de ATL.</span><span class="sxs-lookup"><span data-stu-id="7037e-108">Fortunately, new versions of Microsoft Windows service packs have new DEP/NX APIs that enable you to use DEP/NX and retain compatibility with older ATL versions.</span></span> <span data-ttu-id="7037e-109">Estas nuevas API permiten que Internet Explorer opte por DEP/NX sin provocar errores en los complementos compilados con versiones anteriores de ATL.</span><span class="sxs-lookup"><span data-stu-id="7037e-109">These new APIs enable Internet Explorer to opt into DEP/NX without causing add-ons that are built by using older versions of ATL to fail.</span></span>

<span data-ttu-id="7037e-110">Cuando un complemento no es compatible con DEP/NX y no usa un ATL obsoleto, se puede usar una opción de directiva de grupo para no participar en DEP/NX para Internet Explorer hasta que se implemente una versión actualizada del control roto.</span><span class="sxs-lookup"><span data-stu-id="7037e-110">When an add-on is not DEP/NX-compatible and it does not use an outdated ATL, you can use a Group Policy option to opt out of DEP/NX for Internet Explorer until an updated version of the broken control is deployed.</span></span> <span data-ttu-id="7037e-111">Los administradores locales pueden controlar DEP/NX ejecutando Internet Explorer como administrador y desactivando la opción **Habilitar protección de memoria** en el panel **avanzado** de **Opciones de Internet**.</span><span class="sxs-lookup"><span data-stu-id="7037e-111">Local administrators can control DEP/NX by running Internet Explorer as an administrator and by clearing the **Enable memory protection** option in the **Advanced** pane of **Internet Options**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7037e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7037e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7037e-113">Corregir problemas de compatibilidad en aplicaciones web mediante la vista de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="7037e-113">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
