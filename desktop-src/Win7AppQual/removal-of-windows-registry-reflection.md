---
description: .
ms.assetid: 4b42d44d-cde8-4d96-96c5-24b7ab7e4cec
title: Eliminación de la reflexión del registro de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c610cb0b6ce446e3105fd61cb940028f478892ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707119"
---
# <a name="removal-of-windows-registry-reflection"></a><span data-ttu-id="c1e3f-103">Eliminación de la reflexión del registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c1e3f-103">Removal of Windows Registry Reflection</span></span>

## <a name="platform"></a><span data-ttu-id="c1e3f-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="c1e3f-104">Platform</span></span>

<span data-ttu-id="c1e3f-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="c1e3f-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="c1e3f-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c1e3f-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="c1e3f-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="c1e3f-107">Feature Impact</span></span>

 <span data-ttu-id="c1e3f-108">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="c1e3f-108">**Severity** - Low</span></span>  
<span data-ttu-id="c1e3f-109">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="c1e3f-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="c1e3f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1e3f-110">Description</span></span>

<span data-ttu-id="c1e3f-111">El proceso de reflexión del registro copia las claves y los valores del registro entre dos vistas del registro para mantenerlas sincronizadas. En las instalaciones anteriores de 64 bits de Windows, el proceso reflejaba un subconjunto de las claves del registro Redirigido entre las vistas de 32 bits y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-111">The registry reflection process copies registry keys and values between two registry views to keep them in synch. In previous 64-bit installations of Windows, the process reflected a subset of the redirected registry keys between the 32-bit and 64-bit views.</span></span> <span data-ttu-id="c1e3f-112">Sin embargo, la implementación de esto causó algunas incoherencias en el estado del registro.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-112">However, the implementation of this caused some inconsistencies in the state of the registry.</span></span> <span data-ttu-id="c1e3f-113">(Para obtener más información sobre la reflexión del registro, consulte el artículo de MSDN correspondiente en la sección *vínculos a otros recursos* a continuación).</span><span class="sxs-lookup"><span data-stu-id="c1e3f-113">(For details on Registry Reflection, please refer to the corresponding MSDN article in the *Links to Other Resources* section below.)</span></span>

<span data-ttu-id="c1e3f-114">A partir de Windows 7, hemos quitado la reflexión del registro por completo y combinado las claves que solían reflejarse:</span><span class="sxs-lookup"><span data-stu-id="c1e3f-114">Starting with Windows 7, we have removed registry reflection completely and merged the keys that used to be reflected:</span></span>

-   <span data-ttu-id="c1e3f-115">HKEY \_ \_ clases de \\ software de máquina local \\</span><span class="sxs-lookup"><span data-stu-id="c1e3f-115">HKEY\_LOCAL\_MACHINE\\Software\\Classes</span></span>
-   <span data-ttu-id="c1e3f-116">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ com3</span><span class="sxs-lookup"><span data-stu-id="c1e3f-116">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\COM3</span></span>
-   <span data-ttu-id="c1e3f-117">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ EventSystem</span><span class="sxs-lookup"><span data-stu-id="c1e3f-117">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\EventSystem</span></span>
-   <span data-ttu-id="c1e3f-118">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE</span><span class="sxs-lookup"><span data-stu-id="c1e3f-118">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Ole</span></span>
-   <span data-ttu-id="c1e3f-119">HKEY \_ local \_ Machine \\ software \\ Microsoft \\ RPC</span><span class="sxs-lookup"><span data-stu-id="c1e3f-119">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Rpc</span></span>
-   <span data-ttu-id="c1e3f-120">\_Clases de \\ \* \\ software \\ de usuarios HKEY</span><span class="sxs-lookup"><span data-stu-id="c1e3f-120">HKEY\_USERS\\\*\\Software\\Classes</span></span>
-   <span data-ttu-id="c1e3f-121">\_Clases de usuarios HKEY \\ \* \_</span><span class="sxs-lookup"><span data-stu-id="c1e3f-121">HKEY\_USERS\\\*\_Classes</span></span>

<span data-ttu-id="c1e3f-122">De hecho, esto proporciona el mismo comportamiento de reflexión, ya que los cambios en estas claves inmediatamente están disponibles para las aplicaciones de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-122">Effectively, this provides the same reflection behavior, since changes to these keys immediately are available for both 32-bit and 64-bit applications.</span></span>

<span data-ttu-id="c1e3f-123">Las claves que se reflejaron condicionalmente permanecen divididas:</span><span class="sxs-lookup"><span data-stu-id="c1e3f-123">The keys that were reflected conditionally remain split:</span></span>

-   <span data-ttu-id="c1e3f-124">HKEY \_ \_ clases de software de máquina local \\ \\ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="c1e3f-124">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="c1e3f-125">HKEY \_ \_ interfaz de \\ clases de software de máquina \\ local \\</span><span class="sxs-lookup"><span data-stu-id="c1e3f-125">HKEY\_LOCAL\_MACHINE\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="c1e3f-126">\_Clases de software de usuarios HKEY \\ \* \\ \\ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="c1e3f-126">HKEY\_USERS\\\*\\Software\\Classes\\CLSID</span></span>
-   <span data-ttu-id="c1e3f-127">La \_ \\ \* \\ interfaz de \\ clases de software \\ de usuarios HKEY</span><span class="sxs-lookup"><span data-stu-id="c1e3f-127">HKEY\_USERS\\\*\\Software\\Classes\\Interface</span></span>
-   <span data-ttu-id="c1e3f-128">\_Clases de usuarios HKEY \\ \* \_ \\ CLSID</span><span class="sxs-lookup"><span data-stu-id="c1e3f-128">HKEY\_USERS\\\*\_Classes\\CLSID</span></span>
-   <span data-ttu-id="c1e3f-129">\_Clase HKEY users ( \\ \* \_ \\ interfaz)</span><span class="sxs-lookup"><span data-stu-id="c1e3f-129">HKEY\_USERS\\\*\_Classes\\Interface</span></span>

<span data-ttu-id="c1e3f-130">Se usan para mantener los datos que no se deben compartir entre las aplicaciones de 32 bits y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-130">They are used to keep the data that should not be shared between 32-bit and 64-bit applications.</span></span>

## <a name="manifestation"></a><span data-ttu-id="c1e3f-131">Manifestación</span><span class="sxs-lookup"><span data-stu-id="c1e3f-131">Manifestation</span></span>

<span data-ttu-id="c1e3f-132">Las claves CLSID y de interfaz de la lista anterior no se reflejan ya mientras se redirigen.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-132">CLSID and Interface keys from the list above are not reflected anymore while they are still redirected.</span></span> <span data-ttu-id="c1e3f-133">Aunque este es el comportamiento deseado en la mayoría de los casos, es posible que las aplicaciones tomen una dependencia del comportamiento reflejado en vista.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-133">While this is the desired behavior in most of cases, it is possible that applications could take a dependency on their reflected behavior in Vista.</span></span>

<span data-ttu-id="c1e3f-134">Las funciones que permiten a las aplicaciones controlar la reflexión (RegDisableReflectionKey y RegEnableReflectionKey) no son operaciones en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-134">The functions allowing applications to control reflection (RegDisableReflectionKey and RegEnableReflectionKey) are no-ops in Windows 7.</span></span>

## <a name="mitigation-of-impact"></a><span data-ttu-id="c1e3f-135">Mitigación del impacto</span><span class="sxs-lookup"><span data-stu-id="c1e3f-135">Mitigation of Impact</span></span>

<span data-ttu-id="c1e3f-136">COM es el consumidor principal de la reflexión del registro.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-136">COM is the major consumer of registry reflection.</span></span> <span data-ttu-id="c1e3f-137">COM y otros consumidores se actualizaron para dar cabida a este cambio.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-137">COM and other consumers were updated to accommodate this change.</span></span> <span data-ttu-id="c1e3f-138">Este cambio no afecta a las aplicaciones que usan las API COM estándar.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-138">This change does not affect applications that use standard COM APIs..</span></span>

## <a name="solution"></a><span data-ttu-id="c1e3f-139">Solución</span><span class="sxs-lookup"><span data-stu-id="c1e3f-139">Solution</span></span>

<span data-ttu-id="c1e3f-140">Aplique una de las siguientes opciones si se basa en la reflexión del registro para sincronizar las vistas de 32 bits y 64 bits:</span><span class="sxs-lookup"><span data-stu-id="c1e3f-140">Apply one of the following options if you are relying on registry reflection to synchronize 32bit and 64bit views:</span></span>

-   <span data-ttu-id="c1e3f-141">Crear claves en ambas vistas explícitamente durante la instalación</span><span class="sxs-lookup"><span data-stu-id="c1e3f-141">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="c1e3f-142">Sacar las claves del ámbito de las claves reflejadas</span><span class="sxs-lookup"><span data-stu-id="c1e3f-142">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="c1e3f-143">Comprobar ambas vistas del registro cuando se consulta una clave reflejada</span><span class="sxs-lookup"><span data-stu-id="c1e3f-143">Check both views of the registry when querying for a reflected key</span></span>

    <span data-ttu-id="c1e3f-144">**Nota:** \_No se \_ \_ pueden combinar las marcas de 32KEY de la clave WOW64 y 64KEY de la clave WOW64 \_</span><span class="sxs-lookup"><span data-stu-id="c1e3f-144">**Note:** KEY\_WOW64\_32KEY and KEY\_WOW64\_64KEY flags cannot be combined</span></span>

<span data-ttu-id="c1e3f-145">Aplique una de las siguientes opciones si confía en las funciones de RegDisableReflectionKey para deshabilitar la reflexión del registro:</span><span class="sxs-lookup"><span data-stu-id="c1e3f-145">Apply one of the following options if you are relying on RegDisableReflectionKey functions to disable registry reflection:</span></span>

-   <span data-ttu-id="c1e3f-146">Crear claves en ambas vistas explícitamente durante la instalación</span><span class="sxs-lookup"><span data-stu-id="c1e3f-146">Create keys in both views explicitly during installation</span></span>
-   <span data-ttu-id="c1e3f-147">Sacar las claves del ámbito de las claves reflejadas</span><span class="sxs-lookup"><span data-stu-id="c1e3f-147">Move the keys out of the scope of reflected keys</span></span>
-   <span data-ttu-id="c1e3f-148">Usar subclaves específicas de la plataforma (como x86, AMD64 e ia64) para separar datos específicos de bits</span><span class="sxs-lookup"><span data-stu-id="c1e3f-148">Use platform-specific subkeys (like x86, amd64 and ia64) to separate bitness-specific data</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="c1e3f-149">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="c1e3f-149">Links to Other Resources</span></span>

-   [<span data-ttu-id="c1e3f-150">Artículo sobre la reflexión del registro</span><span class="sxs-lookup"><span data-stu-id="c1e3f-150">Registry Reflection article</span></span>](../winprog64/registry-reflection.md)
-   [<span data-ttu-id="c1e3f-151">Lista de claves redirigidas en el artículo redirector del registro</span><span class="sxs-lookup"><span data-stu-id="c1e3f-151">Redirected keys list within Registry Redirector article</span></span>](../winprog64/registry-redirector.md)
-   [<span data-ttu-id="c1e3f-152">Prácticas recomendadas para WOW64</span><span class="sxs-lookup"><span data-stu-id="c1e3f-152">Best Practices for Wow64</span></span>](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)

> [!Note]  
> <span data-ttu-id="c1e3f-153">Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.</span><span class="sxs-lookup"><span data-stu-id="c1e3f-153">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
