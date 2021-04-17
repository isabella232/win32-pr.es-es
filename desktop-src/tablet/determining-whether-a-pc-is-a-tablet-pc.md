---
description: En ocasiones, es posible que necesite determinar si la aplicación se ejecuta en un Tablet PC porque puede que desee que las aplicaciones aprovechen las capacidades inherentes de tinta, reconocimiento y lápiz.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Determinar si un equipo es Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716721"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a><span data-ttu-id="0aefa-103">Determinar si un equipo es Tablet PC</span><span class="sxs-lookup"><span data-stu-id="0aefa-103">Determining Whether a PC is a Tablet PC</span></span>

<span data-ttu-id="0aefa-104">En ocasiones, es posible que necesite determinar si la aplicación se ejecuta en un Tablet PC porque puede que desee que las aplicaciones aprovechen las capacidades inherentes de tinta, reconocimiento y lápiz.</span><span class="sxs-lookup"><span data-stu-id="0aefa-104">You may occasionally need to determine whether your application is running on a Tablet PC because you may want your applications to take advantage of inherent ink, recognition, and pen capabilities.</span></span> <span data-ttu-id="0aefa-105">Para ayudarle a determinar si la aplicación tiene acceso a las características de Tablet PC, puede usar la llamada de la API de Windows GetSystemMetrics () tal y como se describe en este tema.</span><span class="sxs-lookup"><span data-stu-id="0aefa-105">To help you determine whether your application has access to the Tablet PC features, you can use the GetSystemMetrics() Windows API call as described in this topic.</span></span>

## <a name="client-side-applications"></a><span data-ttu-id="0aefa-106">Aplicaciones Client-Side</span><span class="sxs-lookup"><span data-stu-id="0aefa-106">Client-Side Applications</span></span>

<span data-ttu-id="0aefa-107">Puede usar las técnicas siguientes para determinar si el código se ejecuta en un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0aefa-107">You can use the following techniques to determine whether your code is running on a Tablet PC.</span></span>

-   [<span data-ttu-id="0aefa-108">Uso de GetSystemMetrics (SM \_ TABLETPC)</span><span class="sxs-lookup"><span data-stu-id="0aefa-108">Using GetSystemMetrics (SM\_TABLETPC)</span></span>](/windows)
-   [<span data-ttu-id="0aefa-109">Usar la presencia de archivos binarios de la plataforma de tableta</span><span class="sxs-lookup"><span data-stu-id="0aefa-109">Using the Presence of Tablet Platform Binaries</span></span>](#using-the-presence-of-tablet-platform-binaries)
-   [<span data-ttu-id="0aefa-110">Aplicaciones basadas en Web</span><span class="sxs-lookup"><span data-stu-id="0aefa-110">Web-Based Applications</span></span>](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a><span data-ttu-id="0aefa-111">Uso de GetSystemMetrics (SM \_ TABLETPC)</span><span class="sxs-lookup"><span data-stu-id="0aefa-111">Using GetSystemMetrics (SM\_TABLETPC)</span></span>

### <a name="windows-xp-tablet-pc-edition"></a><span data-ttu-id="0aefa-112">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="0aefa-112">Windows XP Tablet PC Edition</span></span>

<span data-ttu-id="0aefa-113">En Microsoft Windows XP Tablet PC Edition, utilice la función GetSystemMetrics (SM \_ TABLETPC) para determinar si un equipo es un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0aefa-113">In Microsoft Windows XP Tablet PC Edition, use the GetSystemMetrics(SM\_TABLETPC) function to determine whether a computer is a Tablet PC.</span></span> <span data-ttu-id="0aefa-114">GetSystemMetrics (SM \_ TABLETPC) está diseñado para que devuelva true en un equipo con Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="0aefa-114">GetSystemMetrics(SM\_TABLETPC) is designed to return TRUE on a computer running Windows XP Tablet PC Edition.</span></span>

### <a name="windows-vista"></a><span data-ttu-id="0aefa-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0aefa-115">Windows Vista</span></span>

<span data-ttu-id="0aefa-116">En Windows Vista, ya no hay un SDK de Tablet PC diferente.</span><span class="sxs-lookup"><span data-stu-id="0aefa-116">In Windows Vista, there is no longer a distinct Tablet PC SDK.</span></span> <span data-ttu-id="0aefa-117">El Windows SDK contiene ahora una sección denominada "Tablet PC y tecnología táctil" y la lógica de GetSystemMetrics (SM \_ TABLETPC) ha cambiado para reflejar esto.</span><span class="sxs-lookup"><span data-stu-id="0aefa-117">The Windows SDK now contains a section called "Tablet PC and Touch Technology" and the logic of GetSystemMetrics(SM\_TABLETPC) has been changed to reflect this.</span></span> <span data-ttu-id="0aefa-118">GetSystemMetrics (SM \_ TABLETPC) ahora devuelve true si se cumplen todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="0aefa-118">GetSystemMetrics(SM\_TABLETPC) now returns true if all of the following are true:</span></span>

-   <span data-ttu-id="0aefa-119">Hay un digitalizador integrado, ya sea Pen o Touch, en el sistema.</span><span class="sxs-lookup"><span data-stu-id="0aefa-119">There is an integrated digitizer, either pen or touch, on the system.</span></span>
-   <span data-ttu-id="0aefa-120">El componente opcional de Tablet PC está instalado.</span><span class="sxs-lookup"><span data-stu-id="0aefa-120">The Tablet PC optional component is installed.</span></span> <span data-ttu-id="0aefa-121">Este componente contiene características como el panel de entrada de Tablet PC y Windows Journal.</span><span class="sxs-lookup"><span data-stu-id="0aefa-121">This component contains features such as Tablet PC Input Panel and Windows Journal.</span></span>
-   <span data-ttu-id="0aefa-122">El equipo tiene licencia para usar el componente opcional.</span><span class="sxs-lookup"><span data-stu-id="0aefa-122">The computer is licensed to use the optional component.</span></span> <span data-ttu-id="0aefa-123">Las versiones Premium de Windows Vista, como Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise y Windows Vista Ultimate, tienen licencia para usar el componente opcional.</span><span class="sxs-lookup"><span data-stu-id="0aefa-123">Premium versions of Windows Vista—such as Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise, and Windows Vista Ultimate—are licensed to use the optional component.</span></span>
-   <span data-ttu-id="0aefa-124">Se está ejecutando el servicio de entrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0aefa-124">Tablet PC Input Service is running.</span></span> <span data-ttu-id="0aefa-125">El servicio de entrada de Tablet PC es un nuevo servicio para Windows Vista que controla la entrada de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0aefa-125">Tablet PC Input Service is a new service for Windows Vista that controls Tablet PC input.</span></span>

<span data-ttu-id="0aefa-126">Con esta mayor precisión, GetSystemMetrics (SM \_ TABLETPC) sigue siendo la forma recomendada de determinar si un equipo que ejecuta Windows Vista es un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0aefa-126">With this increased accuracy, GetSystemMetrics(SM\_TABLETPC) continues to be the recommended way to determine whether a computer running Windows Vista is a Tablet PC.</span></span>

### <a name="using-the-presence-of-tablet-platform-binaries"></a><span data-ttu-id="0aefa-127">Usar la presencia de archivos binarios de la plataforma de tableta</span><span class="sxs-lookup"><span data-stu-id="0aefa-127">Using the Presence of Tablet Platform Binaries</span></span>

<span data-ttu-id="0aefa-128">En Windows XP Tablet PC Edition y Windows Vista, puede buscar la presencia de los archivos binarios de tinta, como inkobj.dll y Microsoft.Ink.dll, y usar su funcionalidad compatible si están presentes.</span><span class="sxs-lookup"><span data-stu-id="0aefa-128">In both Windows XP Tablet PC Edition and Windows Vista, you can search for the presence of the ink binaries—such as inkobj.dll and Microsoft.Ink.dll—and use their supported functionality if they are present.</span></span>

<span data-ttu-id="0aefa-129">En Windows Vista, los archivos binarios de la plataforma de Tablet PC se instalan de forma predeterminada en todas las versiones de cliente.</span><span class="sxs-lookup"><span data-stu-id="0aefa-129">In Windows Vista, the Tablet PC Platform binaries are installed on all client versions by default.</span></span> <span data-ttu-id="0aefa-130">La funcionalidad de entrada y de entrada manuscrita está disponible en esas versiones.</span><span class="sxs-lookup"><span data-stu-id="0aefa-130">Input and inking functionality are available on those versions.</span></span> <span data-ttu-id="0aefa-131">El reconocimiento solo está disponible en las versiones Premium de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0aefa-131">Recognition is available only in premium versions of Windows Vista.</span></span>

### <a name="web-based-applications"></a><span data-ttu-id="0aefa-132">Aplicaciones Web-Based</span><span class="sxs-lookup"><span data-stu-id="0aefa-132">Web-Based Applications</span></span>

<span data-ttu-id="0aefa-133">En Windows Vista, la cadena User-Agent indicada por Internet Explorer incluye "Tablet PC 2,0" si, según GetSystemMetrics (SM \_ TABLETPC), el dispositivo es un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="0aefa-133">In Windows Vista, the user-agent string reported by Internet Explorer includes "Tablet PC 2.0" if, according to GetSystemMetrics(SM\_TABLETPC), the device is a Tablet PC.</span></span>

<span data-ttu-id="0aefa-134">En Windows XP Tablet PC Edition 2005, la cadena User-Agent incluye Tablet PC 1,7.</span><span class="sxs-lookup"><span data-stu-id="0aefa-134">In Windows XP Tablet PC Edition 2005, the user-agent string includes Tablet PC 1.7.</span></span> <span data-ttu-id="0aefa-135">La cadena User-Agent tiene un aspecto similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="0aefa-135">The user-agent string looks something like the following:</span></span>

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

<span data-ttu-id="0aefa-136">Use este valor para determinar si el equipo cliente es un Tablet PC y admite controles de entrada de lápiz basados en Web.</span><span class="sxs-lookup"><span data-stu-id="0aefa-136">Use this value to determine whether the client computer is a Tablet PC and supports Web-based inking controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0aefa-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0aefa-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aefa-138">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="0aefa-138">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
