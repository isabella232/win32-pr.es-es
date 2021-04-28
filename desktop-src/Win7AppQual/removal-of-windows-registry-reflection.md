---
description: Eliminación de la reflexión del Registro de Windows
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Eliminación de la reflexión del Registro de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeab0109cbbac988c89d6add91fa899cea9169ad
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116263"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="769cb-103">Eliminación de la reflexión del Registro de Windows</span><span class="sxs-lookup"><span data-stu-id="769cb-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="769cb-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="769cb-104">Platform</span></span>

<span data-ttu-id="769cb-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="769cb-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="769cb-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="769cb-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="769cb-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="769cb-107">Feature Impact</span></span>

 <span data-ttu-id="769cb-108">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="769cb-108">**Severity** - Low</span></span>  
<span data-ttu-id="769cb-109">**Frecuencia:** baja</span><span class="sxs-lookup"><span data-stu-id="769cb-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="769cb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="769cb-110">Description</span></span>

<span data-ttu-id="769cb-111">El proceso de reflexión del Registro copia las claves y los valores del Registro entre dos vistas del Registro para mantenerlos sincronizados. En instalaciones anteriores de Windows de 64 bits, el proceso reflejaba un subconjunto de las claves del Registro redirigidas entre las vistas de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="769cb-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="769cb-112">Sin embargo, la implementación de esto produjo algunas incoherencias en el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="769cb-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="769cb-113">(Para obtener más información sobre la reflexión del Registro, consulte el artículo de MSDN correspondiente en la sección Vínculos a *otros* recursos a continuación).</span><span class="sxs-lookup"><span data-stu-id="769cb-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="769cb-114">A partir de Windows 7, hemos quitado completamente la reflexión del Registro y combinado las claves que solían reflejarse:</span><span class="sxs-lookup"><span data-stu-id="769cb-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="769cb-115">Clases de software HKEY \_ LOCAL \_ MACHINE \\ \\</span><span class="sxs-lookup"><span data-stu-id="769cb-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="769cb-116">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ COM3</span><span class="sxs-lookup"><span data-stu-id="769cb-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="769cb-117">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="769cb-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="769cb-118">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Ole</span><span class="sxs-lookup"><span data-stu-id="769cb-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="769cb-119">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Rpc</span><span class="sxs-lookup"><span data-stu-id="769cb-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="769cb-120">Clases de software HKEY \_ USERS \\ \* \\ \\</span><span class="sxs-lookup"><span data-stu-id="769cb-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="769cb-121">Clases HKEY \_ USERS \\ \* \_</span><span class="sxs-lookup"><span data-stu-id="769cb-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="769cb-122">De hecho, esto proporciona el mismo comportamiento de reflexión, ya que los cambios en estas claves están disponibles inmediatamente para las aplicaciones de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="769cb-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="769cb-123">Las claves reflejadas condicionalmente permanecen divididas:</span><span class="sxs-lookup"><span data-stu-id="769cb-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="769cb-124">HKEY \_ LOCAL \_ MACHINE \\ Software \\ Classes \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="769cb-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="769cb-125">Interfaz de clases \_ de software HKEY LOCAL \_ MACHINE \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="769cb-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="769cb-126">HKEY \_ USERS Clases de software \\ \* \\ \\ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="769cb-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="769cb-127">Interfaz de clases \_ \\ \* \\ de software \\ \\ HKEY USERS</span><span class="sxs-lookup"><span data-stu-id="769cb-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="769cb-128">\_CLSID de \\ \* \_ clases \\ HKEY USERS</span><span class="sxs-lookup"><span data-stu-id="769cb-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="769cb-129">HKEY \_ USERS \\ \* \_ (interfaz de \\ clases)</span><span class="sxs-lookup"><span data-stu-id="769cb-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="769cb-130">Se usan para mantener los datos que no se deben compartir entre aplicaciones de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="769cb-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="769cb-131">Manifestación</span><span class="sxs-lookup"><span data-stu-id="769cb-131">Manifestation</span></span>

<span data-ttu-id="769cb-132">Las claves CLSID e Interface de la lista anterior ya no se reflejan mientras se redirigen.</span><span class="sxs-lookup"><span data-stu-id="769cb-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="769cb-133">Aunque este es el comportamiento deseado en la mayoría de los casos, es posible que las aplicaciones puedan tomar una dependencia de su comportamiento reflejado en Vista.</span><span class="sxs-lookup"><span data-stu-id="769cb-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="769cb-134">Las funciones que permiten a las aplicaciones controlar la reflexión (RegDisableReflectionKey y RegEnableReflectionKey) no son operaciones en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="769cb-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="769cb-135">Mitigación del impacto</span><span class="sxs-lookup"><span data-stu-id="769cb-135">Mitigation of Impact</span></span>

<span data-ttu-id="769cb-136">COM es el principal consumidor de la reflexión del Registro.</span><span class="sxs-lookup"><span data-stu-id="769cb-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="769cb-137">COM y otros consumidores se actualizaron para dar cabida a este cambio.</span><span class="sxs-lookup"><span data-stu-id="769cb-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="769cb-138">Este cambio no afecta a las aplicaciones que usan las API COM estándar.</span><span class="sxs-lookup"><span data-stu-id="769cb-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="769cb-139">Solución</span><span class="sxs-lookup"><span data-stu-id="769cb-139">Solution</span></span>

<span data-ttu-id="769cb-140">Aplique una de las siguientes opciones si se basa en la reflexión del Registro para sincronizar vistas de 32 bits y 64 bits:</span><span class="sxs-lookup"><span data-stu-id="769cb-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="769cb-141">Creación explícita de claves en ambas vistas durante la instalación</span><span class="sxs-lookup"><span data-stu-id="769cb-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="769cb-142">Sacar las claves del ámbito de las claves reflejadas</span><span class="sxs-lookup"><span data-stu-id="769cb-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="769cb-143">Comprobación de ambas vistas del Registro al consultar una clave reflejada</span><span class="sxs-lookup"><span data-stu-id="769cb-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="769cb-144">**Nota:** Las \_ marcas KEY WOW64 \_ 32KEY y KEY \_ WOW64 \_ 64KEY no se pueden combinar</span><span class="sxs-lookup"><span data-stu-id="769cb-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="769cb-145">Aplique una de las siguientes opciones si se basa en las funciones RegDisableReflectionKey para deshabilitar la reflexión del Registro:</span><span class="sxs-lookup"><span data-stu-id="769cb-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="769cb-146">Crear claves en ambas vistas explícitamente durante la instalación</span><span class="sxs-lookup"><span data-stu-id="769cb-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="769cb-147">Sacar las claves del ámbito de las claves reflejadas</span><span class="sxs-lookup"><span data-stu-id="769cb-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="769cb-148">Uso de subclaves específicas de la plataforma (como x86, amd64 e ia64) para separar los datos específicos de bits</span><span class="sxs-lookup"><span data-stu-id="769cb-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="769cb-149">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="769cb-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="769cb-150">Artículo reflexión del Registro</span><span class="sxs-lookup"><span data-stu-id="769cb-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="769cb-151">Lista de claves redirigidas en el artículo Redirector del Registro</span><span class="sxs-lookup"><span data-stu-id="769cb-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="769cb-152">Procedimientos recomendados para Wow64</span><span class="sxs-lookup"><span data-stu-id="769cb-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="769cb-153">Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.</span><span class="sxs-lookup"><span data-stu-id="769cb-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
