---
description: Biblioteca del Registro sin conexión
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Biblioteca del Registro sin conexión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1aa5acdd7904516608413ff973e60e81c296c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089253"
---
# <a name="offline-registry-library"></a><span data-ttu-id="69807-103">Biblioteca del Registro sin conexión</span><span class="sxs-lookup"><span data-stu-id="69807-103">Offline Registry Library</span></span>

## <a name="purpose"></a><span data-ttu-id="69807-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="69807-104">Purpose</span></span>

<span data-ttu-id="69807-105">La biblioteca del Registro sin conexión (Offreg.dll) se usa para modificar un subárbol del Registro fuera del registro del sistema activo.</span><span class="sxs-lookup"><span data-stu-id="69807-105">The offline registry library (Offreg.dll) is used to modify a registry hive outside the active system registry.</span></span> <span data-ttu-id="69807-106">Esta biblioteca está pensada para escenarios de actualización del Registro, como el mantenimiento de una imagen de sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="69807-106">This library is intended for registry update scenarios such as servicing an operating system image.</span></span> <span data-ttu-id="69807-107">La biblioteca admite formatos de Subárbol del Registro a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="69807-107">The library supports registry hive formats starting with Windows Vista.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="69807-108">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="69807-108">Developer audience</span></span>

<span data-ttu-id="69807-109">Esta tecnología es para fabricantes de equipos originales (OEM), proveedores de software antivirus y antimalware y otros desarrolladores de aplicaciones que deben poder analizar los archivos de Hive del registro sin cargarlos en el registro activo.</span><span class="sxs-lookup"><span data-stu-id="69807-109">This technology is for original equipment manufacturers (OEMs), antivirus and antimalware software vendors, and other application developers who must be able to parse registry hive files without loading them into the active registry.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="69807-110">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="69807-110">Run-time requirements</span></span>

<span data-ttu-id="69807-111">La biblioteca del Registro sin conexión se proporciona como una biblioteca de vínculos dinámicos (DLL) redistribuible binaria.</span><span class="sxs-lookup"><span data-stu-id="69807-111">The offline registry library is provided as a binary redistributable dynamic-link library (DLL).</span></span> <span data-ttu-id="69807-112">Esta biblioteca se ejecuta en las siguientes versiones de Windows:</span><span class="sxs-lookup"><span data-stu-id="69807-112">This library runs on the following versions of Windows:</span></span>

<dl> <span data-ttu-id="69807-113">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="69807-113">Windows Server 2016</span></span>  
<span data-ttu-id="69807-114">Windows 10</span><span class="sxs-lookup"><span data-stu-id="69807-114">Windows 10</span></span>  
<span data-ttu-id="69807-115">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="69807-115">Windows 8.1</span></span>  
<span data-ttu-id="69807-116">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="69807-116">Windows Server 2012 R2</span></span>  
<span data-ttu-id="69807-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="69807-117">Windows 8</span></span>  
<span data-ttu-id="69807-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="69807-118">Windows Server 2012</span></span>  
<span data-ttu-id="69807-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="69807-119">Windows 7</span></span>  
<span data-ttu-id="69807-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="69807-120">Windows Server 2008 R2</span></span>  
<span data-ttu-id="69807-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69807-121">Windows Server 2008</span></span>  
<span data-ttu-id="69807-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69807-122">Windows Vista</span></span>  
</dl>

<span data-ttu-id="69807-123">Las aplicaciones deben vincular a Offreg.dll mediante la vinculación dinámica.</span><span class="sxs-lookup"><span data-stu-id="69807-123">Applications should link to Offreg.dll using dynamic linking.</span></span>

<span data-ttu-id="69807-124">Offreg.dll se proporciona en el Kit para controladores de Windows (WDK) para Windows 10 versiones anteriores del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="69807-124">Offreg.dll is provided in the Windows Driver Kit (WDK) for Windows 10 and earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="69807-125">Para obtener información sobre cómo obtener wdk, vea Cómo obtener [wdk](/windows-hardware/drivers/download-the-wdk) y WLK o visite el sitio web [de suscripciones de MSDN.](https://msdn.microsoft.com/subscriptions/default.aspx)</span><span class="sxs-lookup"><span data-stu-id="69807-125">For information about obtaining the WDK, see [How to Get the WDK and the WLK](/windows-hardware/drivers/download-the-wdk) or visit the [MSDN Subscriptions](https://msdn.microsoft.com/subscriptions/default.aspx) website.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="69807-126">En esta sección</span><span class="sxs-lookup"><span data-stu-id="69807-126">In this section</span></span>

-   [<span data-ttu-id="69807-127">**Acerca de la biblioteca del Registro sin conexión**</span><span class="sxs-lookup"><span data-stu-id="69807-127">**About the Offline Registry Library**</span></span>](about-the-offline-registry-library.md)
-   [<span data-ttu-id="69807-128">**Funciones de la biblioteca del Registro sin conexión**</span><span class="sxs-lookup"><span data-stu-id="69807-128">**Offline Registry Library Functions**</span></span>](offline-registry-library-functions.md)

 

 
