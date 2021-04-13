---
title: Gadgets de escritorio quitados
description: Gadgets de escritorio quitados
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- gadgets
- Gadgets de escritorio
- Windows Sidebar
- Barra lateral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104421502"
---
# <a name="desktop-gadgets-removed"></a><span data-ttu-id="27e52-107">Gadgets de escritorio quitados</span><span class="sxs-lookup"><span data-stu-id="27e52-107">Desktop gadgets removed</span></span>

## <a name="platforms"></a><span data-ttu-id="27e52-108">Plataformas</span><span class="sxs-lookup"><span data-stu-id="27e52-108">Platforms</span></span>

 <span data-ttu-id="27e52-109">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="27e52-109">**Clients** - Windows 8</span></span>  
<span data-ttu-id="27e52-110">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="27e52-110">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="27e52-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="27e52-111">Description</span></span>

<span data-ttu-id="27e52-112">Desde el punto de vista de la funcionalidad, los gadgets ya están en desuso y se configuran mediante nuevas aplicaciones y iconos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="27e52-112">From a functionality standpoint, Gadgets have already been deprecated and are outclassed by new live tiles and apps.</span></span> <span data-ttu-id="27e52-113">Los gadgets también presentan un riesgo de seguridad para los usuarios.</span><span class="sxs-lookup"><span data-stu-id="27e52-113">Gadgets also present a security risk to users.</span></span> <span data-ttu-id="27e52-114">Como plataforma, existen vulnerabilidades en las que incluso se podrían aprovechar los gadgets benignos.</span><span class="sxs-lookup"><span data-stu-id="27e52-114">As a platform, vulnerabilities exist such that even benign Gadgets could be exploited.</span></span> <span data-ttu-id="27e52-115">Por lo tanto, para mantener Windows 8 como nuestro sistema operativo más moderno y seguro, hemos optado por quitar completamente los gadgets del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="27e52-115">Therefore, in order to uphold Windows 8 as our most modern and secure operating system, we have chosen to remove Gadgets from the operating system entirely.</span></span> <span data-ttu-id="27e52-116">Se notificará a los usuarios de Windows 7 con gadgets en el escritorio y se desinstalarán los gadgets.</span><span class="sxs-lookup"><span data-stu-id="27e52-116">Windows 7 users with Gadgets on their Desktop will be notified and Gadgets will be uninstalled.</span></span>

## <a name="manifestation"></a><span data-ttu-id="27e52-117">Manifestación</span><span class="sxs-lookup"><span data-stu-id="27e52-117">Manifestation</span></span>

<span data-ttu-id="27e52-118">Los gadgets de escritorio no estarán disponibles en el escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="27e52-118">Desktop Gadgets will not be available on the Windows Desktop.</span></span>

## <a name="mitigation"></a><span data-ttu-id="27e52-119">Mitigación</span><span class="sxs-lookup"><span data-stu-id="27e52-119">Mitigation</span></span>

<span data-ttu-id="27e52-120">La estructura de carpetas y la API de gadgets de escritorio permanecerán en su lugar para Windows 8.</span><span class="sxs-lookup"><span data-stu-id="27e52-120">The Desktop Gadgets API and folder structure will remain in place for Windows 8.</span></span> <span data-ttu-id="27e52-121">Las aplicaciones que instalan y ejecutan gadgets mediante programación con esta API seguirán ejecutándose sin errores (aunque los propios gadgets no lo están).</span><span class="sxs-lookup"><span data-stu-id="27e52-121">Applications which programmatically install and run Gadgets using this API will continue to run without fail (although the Gadgets themselves will not).</span></span>

## <a name="solution"></a><span data-ttu-id="27e52-122">Solución</span><span class="sxs-lookup"><span data-stu-id="27e52-122">Solution</span></span>

<span data-ttu-id="27e52-123">Los desarrolladores de aplicaciones de escritorio no deben empaquetar gadgets en sus instaladores.</span><span class="sxs-lookup"><span data-stu-id="27e52-123">Desktop app developers should not package Gadgets in their installers.</span></span> <span data-ttu-id="27e52-124">Estos gadgets solo ocuparán espacio para el usuario y no podrán ejecutarse en el sistema.</span><span class="sxs-lookup"><span data-stu-id="27e52-124">These Gadgets will just take up space for the user and will not be able to be run in the system.</span></span>

## <a name="tests"></a><span data-ttu-id="27e52-125">Pruebas</span><span class="sxs-lookup"><span data-stu-id="27e52-125">Tests</span></span>

<span data-ttu-id="27e52-126">Los desarrolladores pueden probar la compatibilidad de este cambio deshabilitando el componente opcional para los gadgets de escritorio en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="27e52-126">Developers are able to test compatibility of this change by disabling the optional component for Desktop Gadgets in Windows 7.</span></span> <span data-ttu-id="27e52-127">Para deshabilitar los gadgets en un equipo con Windows 7, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="27e52-127">To disable Gadgets on a Windows 7 PC, follow the steps below:</span></span>

1.  <span data-ttu-id="27e52-128">Navegue para activar o desactivar las características de Windows desde el panel de control.</span><span class="sxs-lookup"><span data-stu-id="27e52-128">Navigate to Turn Windows Features on or off from the Control Panel.</span></span>
2.  <span data-ttu-id="27e52-129">Desactive la casilla situada junto a "plataforma de gadgets de Windows".</span><span class="sxs-lookup"><span data-stu-id="27e52-129">Uncheck the box next to “Windows Gadget Platform”.</span></span>
3.  <span data-ttu-id="27e52-130">Haga clic en aceptar y siga las instrucciones en pantalla adicionales.</span><span class="sxs-lookup"><span data-stu-id="27e52-130">Click OK and follow any additional on-screen instructions.</span></span>

## <a name="resources"></a><span data-ttu-id="27e52-131">Recursos</span><span class="sxs-lookup"><span data-stu-id="27e52-131">Resources</span></span>

[<span data-ttu-id="27e52-132">Vulnerabilidades en los gadgets podrían permitir la ejecución remota de código</span><span class="sxs-lookup"><span data-stu-id="27e52-132">Vulnerabilities in Gadgets Could Allow Remote Code Execution</span></span>](https://support.microsoft.com/kb/2719662)

 

 




