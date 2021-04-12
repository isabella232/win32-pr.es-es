---
description: .
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: Subconjunto de .NET 2,0 Now en Server Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e0f836ca7afaef920429df17ef8be845ce92e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279629"
---
# <a name="subset-of-net-20-now-on-server-core"></a><span data-ttu-id="65ae7-103">Subconjunto de .NET 2,0 Now en Server Core</span><span class="sxs-lookup"><span data-stu-id="65ae7-103">Subset of .NET 2.0 Now on Server Core</span></span>

## <a name="platform"></a><span data-ttu-id="65ae7-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="65ae7-104">Platform</span></span>

<span data-ttu-id="65ae7-105">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65ae7-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="65ae7-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="65ae7-106">Feature Impact</span></span>

 <span data-ttu-id="65ae7-107">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="65ae7-107">**Severity** - Low</span></span>  
<span data-ttu-id="65ae7-108">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="65ae7-108">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="65ae7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="65ae7-109">Description</span></span>

<span data-ttu-id="65ae7-110">La opción de instalación Server Core para Windows Server 2008 R2 ahora incluye un subconjunto del .NET Framework 2,0.</span><span class="sxs-lookup"><span data-stu-id="65ae7-110">The Server Core installation option for Windows Server 2008 R2 now includes a subset of the .NET Framework 2.0.</span></span> <span data-ttu-id="65ae7-111">El subconjunto es la funcionalidad de .NET 2,0 que se alinea con la funcionalidad de Server Core. no se ha agregado ningún binario a Server Core base para permitir que cualquier parte de .NET 2,0 funcione.</span><span class="sxs-lookup"><span data-stu-id="65ae7-111">The subset is the functionality in .NET 2.0 that aligns with the functionality in Server Core; no binaries were added to the Server Core base to allow any portion of .NET 2.0 to function.</span></span>

<span data-ttu-id="65ae7-112">No había compatibilidad con .NET en la opción de instalación Server Core para Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="65ae7-112">There was no .NET support in the Server Core installation option for Windows Server 2008.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="65ae7-113">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="65ae7-113">Manifestation of Impact</span></span>

<span data-ttu-id="65ae7-114">Esto permite que algunas aplicaciones basadas en .NET 2,0 se ejecuten en Server Core en Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="65ae7-114">This allows some .NET 2.0 based-applications to run on Server Core in Windows Server 2008 R2.</span></span>

## <a name="testing"></a><span data-ttu-id="65ae7-115">Prueba</span><span class="sxs-lookup"><span data-stu-id="65ae7-115">Testing</span></span>

<span data-ttu-id="65ae7-116">Compruebe que las clases .NET que usa el código se incluyen en Server Core.</span><span class="sxs-lookup"><span data-stu-id="65ae7-116">Verify that the .NET classes your code uses is included in Server Core.</span></span> <span data-ttu-id="65ae7-117">Pruebe también las aplicaciones que ejecutan este código en Server Core.</span><span class="sxs-lookup"><span data-stu-id="65ae7-117">Also test any applications that run this code on Server Core.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="65ae7-118">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="65ae7-118">Links to Other Resources</span></span>

-   <span data-ttu-id="65ae7-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65ae7-119">[Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))</span></span>
-   [<span data-ttu-id="65ae7-120">Blog de Server Core</span><span class="sxs-lookup"><span data-stu-id="65ae7-120">Server Core Blog</span></span>](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   <span data-ttu-id="65ae7-121">*Vea también* la sección Server Core del *SDK de Windows Server 2008 R2* cuando esté disponible</span><span class="sxs-lookup"><span data-stu-id="65ae7-121">*See also* the Server Core section of the *Windows Server 2008 R2 SDK* when it becomes available</span></span>

> [!Note]  
> <span data-ttu-id="65ae7-122">Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.</span><span class="sxs-lookup"><span data-stu-id="65ae7-122">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
