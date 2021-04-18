---
description: Las aplicaciones cliente y los scripts que tienen acceso a los proveedores estándar de 32 bits de WMI continúan funcionando con normalidad cuando se ejecutan en un sistema operativo de 64 bits.
ms.assetid: 68819bea-a48d-4de1-a50d-f03ae04775f5
ms.tgt_platform: multiple
title: Obtener y proporcionar datos en un equipo de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe7d8ff5430a7c47b652bfbcca05d2f53ba857d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567121"
---
# <a name="getting-and-providing-data-on-a-64-bit-computer"></a><span data-ttu-id="30378-103">Obtener y proporcionar datos en un equipo de 64 bits</span><span class="sxs-lookup"><span data-stu-id="30378-103">Getting and Providing Data on a 64-bit Computer</span></span>

<span data-ttu-id="30378-104">Las aplicaciones cliente y los scripts que tienen acceso a los proveedores estándar de 32 bits de WMI continúan funcionando con normalidad cuando se ejecutan en un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="30378-104">Client applications and scripts that access standard WMI 32-bit providers continue to operate normally when running on a 64-bit operating system.</span></span> <span data-ttu-id="30378-105">Solo dos proveedores preinstalados, el [proveedor del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) y el [proveedor de vistas](view-provider.md), tienen versiones de 64 bits que se ejecutan en paralelo con las versiones de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="30378-105">Only two preinstalled providers, the [System Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider) and the [View provider](view-provider.md), have 64-bit versions which run side-by-side with the 32-bit versions.</span></span> <span data-ttu-id="30378-106">Sin embargo, una aplicación de 32 bits que solicita instancias de Modelo de controlador de Windows de 32 bits (WDM) recibe las instancias de la clase WDM de 64 bits predeterminada en un sistema operativo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="30378-106">However, a 32-bit application that requests 32-bit Windows Driver Model (WDM) instances receives the default 64-bit WDM class instances on a 64-bit operating system.</span></span>

## <a name="accessing-default-and-nondefault-provider-data"></a><span data-ttu-id="30378-107">Acceder a los datos de proveedor predeterminados y no predeterminados</span><span class="sxs-lookup"><span data-stu-id="30378-107">Accessing Default and Nondefault Provider Data</span></span>

<span data-ttu-id="30378-108">Por lo general, los escritores de proveedores no incluyen las versiones de 32 y 64 bits de un proveedor en el mismo sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="30378-108">Generally, provider writers do not include both 32-bit and 64-bit versions of a provider in the same operating system.</span></span> <span data-ttu-id="30378-109">Si no existe ningún proveedor de 64 bits, un proveedor de 32 bits puede continuar ejecutándose a través de las funciones de WOW64.</span><span class="sxs-lookup"><span data-stu-id="30378-109">If no 64-bit provider exists, a 32-bit provider can continue to run through the facilities of WOW64.</span></span> <span data-ttu-id="30378-110">Un proveedor de 64 bits puede proporcionar igualmente datos a una aplicación de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="30378-110">A 64-bit provider can likewise supply data to a 32-bit application.</span></span> <span data-ttu-id="30378-111">Para obtener más información, vea [proporcionar datos WMI en una plataforma de 64 bits](providing-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="30378-111">For more information, see [Providing WMI Data on a 64-bit Platform](providing-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="30378-112">Si existen dos versiones, las aplicaciones cliente y los scripts pueden usar los parámetros de contexto disponibles en la [API de com](com-api-for-wmi.md) y la [API de scripting](scripting-api-for-wmi.md) para conectarse explícitamente a un proveedor de WMI específico no predeterminado, si está disponible.</span><span class="sxs-lookup"><span data-stu-id="30378-112">If two versions exist, client applications and scripts can use the context parameters available in the [COM API](com-api-for-wmi.md) and the [Scripting API](scripting-api-for-wmi.md) to connect explicitly to a specific nondefault WMI provider, if it is available.</span></span> <span data-ttu-id="30378-113">Para obtener más información, consulte [solicitar datos WMI en una plataforma de 64 bits](requesting-wmi-data-on-a-64-bit-platform.md).</span><span class="sxs-lookup"><span data-stu-id="30378-113">For more information, see [Requesting WMI Data on a 64-bit Platform](requesting-wmi-data-on-a-64-bit-platform.md).</span></span>

<span data-ttu-id="30378-114">En el diagrama siguiente se muestran las conexiones predeterminadas y no predeterminadas, utilizando el registro como ejemplo para el que dos proveedores pueden existir en paralelo en una plataforma de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="30378-114">The following diagram shows the default and nondefault connections, using the registry as an example for which two providers can exist side-by-side on a 64-bit platform.</span></span>

![conexiones predeterminadas y no predeterminadas en una plataforma de 64 bits](images/32-64bit-registry.png)

## <a name="related-topics"></a><span data-ttu-id="30378-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30378-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30378-117">Solicitar datos WMI en una plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="30378-117">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="30378-118">Proporcionar datos WMI en una plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="30378-118">Providing WMI Data on a 64-bit Platform</span></span>](providing-wmi-data-on-a-64-bit-platform.md)
</dt> </dl>

 

 
