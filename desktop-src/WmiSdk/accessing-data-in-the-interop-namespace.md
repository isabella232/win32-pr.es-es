---
description: Los proveedores de asociación permiten a los clientes de Instrumental de administración de Windows (WMI) atravesar y recuperar perfiles y las instancias de clase asociadas de distintos espacios de nombres.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Obtener acceso a los datos en el espacio de nombres Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002832"
---
# <a name="accessing-data-in-the-interop-namespace"></a><span data-ttu-id="9e121-103">Obtener acceso a los datos en el espacio de nombres Interop</span><span class="sxs-lookup"><span data-stu-id="9e121-103">Accessing Data in the Interop Namespace</span></span>

<span data-ttu-id="9e121-104">Los proveedores de asociación permiten a los clientes de Instrumental de administración de Windows (WMI) atravesar y recuperar perfiles y las instancias de clase asociadas de distintos espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="9e121-104">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>

<span data-ttu-id="9e121-105">Los proveedores y las clases de asociación residen en el \\ \\ espacio de nombres de \\ interoperabilidad raíz.</span><span class="sxs-lookup"><span data-stu-id="9e121-105">Association providers and classes reside in the \\\\root\\interop namespace.</span></span> <span data-ttu-id="9e121-106">Para obtener más información, vea cruce seguro de la [asociación entre espacios de nombres](cross-namespace-association-traversal.md) y [escritura de un proveedor de asociaciones](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="9e121-106">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) and [Writing an Association Provider](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="9e121-107">Los proveedores de asociación exponen perfiles estándar, como un perfil de energía.</span><span class="sxs-lookup"><span data-stu-id="9e121-107">Association providers expose standard profiles, like a power profile.</span></span> <span data-ttu-id="9e121-108">En los ejemplos siguientes se usa el perfil de energía para mostrar cómo detectar y obtener acceso a los datos a través del espacio de nombres de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="9e121-108">The following examples use the power profile to illustrate how to discover and access data through the interop namespace.</span></span>

<span data-ttu-id="9e121-109">Windows PowerShell proporciona un mecanismo sencillo para atravesar la Asociación adecuada, recuperar un perfil de dispositivo y llamar a un método.</span><span class="sxs-lookup"><span data-stu-id="9e121-109">Windows PowerShell provides a simple mechanism to traverse through the appropriate association, retrieve a device profile, and call a method.</span></span>

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a><span data-ttu-id="9e121-110">Enumerar perfiles en el espacio de nombres root/Interop</span><span class="sxs-lookup"><span data-stu-id="9e121-110">Enumerating profiles in the root/interop namespace</span></span>

<span data-ttu-id="9e121-111">El siguiente comando de Windows PowerShell enumera los perfiles compatibles con el forzado de la tarea de administración distribuida ([DMTF](https://www.dmtf.org/standards/wsman)) en un equipo con Windows 7:</span><span class="sxs-lookup"><span data-stu-id="9e121-111">The following Windows PowerShell command enumerates the Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman))-supported profiles on a Windows 7 computer:</span></span>


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a><span data-ttu-id="9e121-112">Recuperación de instancias de un perfil de dispositivo específico</span><span class="sxs-lookup"><span data-stu-id="9e121-112">Retrieving instances of a specific device profile</span></span>

<span data-ttu-id="9e121-113">El siguiente comando de Windows PowerShell devuelve todas las instancias de un perfil especificado a través de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):</span><span class="sxs-lookup"><span data-stu-id="9e121-113">The following Windows PowerShell command returns all instances of a specified profile through [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):</span></span>


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a><span data-ttu-id="9e121-114">Asignación del perfil de energía a una variable</span><span class="sxs-lookup"><span data-stu-id="9e121-114">Assigning the power profile to a variable</span></span>

<span data-ttu-id="9e121-115">El siguiente comando de Windows PowerShell asigna la instancia de Perfil de energía a una variable:</span><span class="sxs-lookup"><span data-stu-id="9e121-115">The following Windows PowerShell command assigns the power profile instance to a variable:</span></span>


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a><span data-ttu-id="9e121-116">Enumerar los planes de energía de un equipo</span><span class="sxs-lookup"><span data-stu-id="9e121-116">Enumerating the power plans on a computer</span></span>

<span data-ttu-id="9e121-117">El siguiente comando de Windows PowerShell enumera los planes de Perfil de energía disponibles:</span><span class="sxs-lookup"><span data-stu-id="9e121-117">The following Windows PowerShell command enumerates the available power profile plans:</span></span>


```PowerShell
$pplan
```



## <a name="calling-a-method"></a><span data-ttu-id="9e121-118">Llamar a un método</span><span class="sxs-lookup"><span data-stu-id="9e121-118">Calling a method</span></span>

<span data-ttu-id="9e121-119">El siguiente comando de Windows PowerShell llama al método [**Activar**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) para el plan de energía:</span><span class="sxs-lookup"><span data-stu-id="9e121-119">The following Windows PowerShell command calls the [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) method for the power plan:</span></span>


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a><span data-ttu-id="9e121-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e121-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e121-121">Cruce seguro de la asociación entre espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="9e121-121">Cross Namespace Association Traversal</span></span>](cross-namespace-association-traversal.md)
</dt> <dt>

[<span data-ttu-id="9e121-122">Escribir un proveedor de asociación</span><span class="sxs-lookup"><span data-stu-id="9e121-122">Writing an Association Provider</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

<span data-ttu-id="9e121-123">[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e121-123">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="9e121-124">[**Win32 \_ PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9e121-124">[**Win32\_PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span></span>
</dt> </dl>

 

 
