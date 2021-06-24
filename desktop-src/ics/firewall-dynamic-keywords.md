---
title: Palabras clave dinámicas de firewall
description: Las API de palabras clave dinámicas del firewall se usan para administrar direcciones de palabras clave dinámicas Firewall de Windows Defender.
keywords:
- Palabras clave dinámicas de firewall
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: e60526d8a7889af3173913774790bdd209121040
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112681209"
---
# <a name="firewall-dynamic-keywords"></a><span data-ttu-id="3a25b-104">Palabras clave dinámicas de firewall</span><span class="sxs-lookup"><span data-stu-id="3a25b-104">Firewall dynamic keywords</span></span>

<span data-ttu-id="3a25b-105">Las API de palabras clave dinámicas del firewall se usan para administrar direcciones de *palabras clave dinámicas* [Firewall de Windows Defender](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span><span class="sxs-lookup"><span data-stu-id="3a25b-105">You use the firewall dynamic keywords APIs to manage *dynamic keyword addresses* in [Windows Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span></span> <span data-ttu-id="3a25b-106">Una dirección de palabra clave dinámica se usa para crear un conjunto de direcciones IP a las que pueden hacer referencia una o varias reglas de firewall.</span><span class="sxs-lookup"><span data-stu-id="3a25b-106">A dynamic keyword address is used to create a set of IP addresses to which one or more firewall rules can refer.</span></span> <span data-ttu-id="3a25b-107">Las direcciones de palabras clave dinámicas admiten IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="3a25b-107">Dynamic keyword addresses support both IPv4 and IPv6.</span></span>

> [!NOTE]
> <span data-ttu-id="3a25b-108">Para obtener contenido de referencia de API para las API introducidas en este tema, consulte Referencia [de palabras clave dinámicas de firewall.](firewall-dynamic-keywords-reference.md)</span><span class="sxs-lookup"><span data-stu-id="3a25b-108">For API reference content for the APIs introduced in this topic, see [Firewall dynamic keywords reference](firewall-dynamic-keywords-reference.md).</span></span>

## <a name="operations-on-dynamic-keyword-addresses"></a><span data-ttu-id="3a25b-109">Operaciones en direcciones de palabras clave dinámicas</span><span class="sxs-lookup"><span data-stu-id="3a25b-109">Operations on dynamic keyword addresses</span></span>

<span data-ttu-id="3a25b-110">Con las API de palabras clave dinámicas del firewall, puede realizar las siguientes operaciones.</span><span class="sxs-lookup"><span data-stu-id="3a25b-110">With the Firewall dynamic keywords APIs, you can perform the following operations.</span></span>

* <span data-ttu-id="3a25b-111">Adición de direcciones de palabras clave dinámicas</span><span class="sxs-lookup"><span data-stu-id="3a25b-111">Add dynamic keyword addresses</span></span>
* <span data-ttu-id="3a25b-112">Eliminación de direcciones de palabras clave dinámicas</span><span class="sxs-lookup"><span data-stu-id="3a25b-112">Delete dynamic keyword addresses</span></span>
* <span data-ttu-id="3a25b-113">Enumerar direcciones de palabras clave dinámicas por identificador o por tipo</span><span class="sxs-lookup"><span data-stu-id="3a25b-113">Enumerate dynamic keyword addresses by ID, or by type</span></span>
* <span data-ttu-id="3a25b-114">Actualización de direcciones de palabras clave dinámicas</span><span class="sxs-lookup"><span data-stu-id="3a25b-114">Update dynamic keyword addresses</span></span>
* <span data-ttu-id="3a25b-115">Suscripción y control de notificaciones de cambio de dirección de palabras clave dinámicas</span><span class="sxs-lookup"><span data-stu-id="3a25b-115">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="3a25b-116">Hay ejemplos de código para todas esas operaciones más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="3a25b-116">There are code examples for all of those operations later in this topic.</span></span>

<span data-ttu-id="3a25b-117">Una vez que haya agregado una dirección de palabra clave dinámica, se conserva en los reinicios.</span><span class="sxs-lookup"><span data-stu-id="3a25b-117">Once you've added a dynamic keyword address, it persists across reboots.</span></span> <span data-ttu-id="3a25b-118">Debe eliminar una dirección de palabra clave dinámica una vez que haya terminado con el objeto .</span><span class="sxs-lookup"><span data-stu-id="3a25b-118">You must delete a dynamic keyword address once you're done with the object.</span></span>

<span data-ttu-id="3a25b-119">Hay dos clases de direcciones de palabras clave dinámicas, como se describe en las dos secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="3a25b-119">There are two classes of dynamic keyword addresses, as described in the next two sections.</span></span>

## <a name="autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="3a25b-120">Direcciones de palabras clave dinámicas de AutoResolve</span><span class="sxs-lookup"><span data-stu-id="3a25b-120">AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="3a25b-121">El primer tipo es *AutoResolve*, donde el campo de palabra clave representa un nombre que se puede resolver y las direcciones IP no se definen al crearse. </span><span class="sxs-lookup"><span data-stu-id="3a25b-121">The first type is *AutoResolve*, where the *keyword* field represents a resolvable name, and the IP addresses aren't defined upon creation.</span></span>

<span data-ttu-id="3a25b-122">Estos objetos están diseñados para que sus direcciones IP se resuelvan automáticamente.</span><span class="sxs-lookup"><span data-stu-id="3a25b-122">These objects are intended to have their IP addresses resolved automatically.</span></span> <span data-ttu-id="3a25b-123">Es decir, no a través de un administrador en el momento de la creación del objeto; ni a través del propio sistema operativo (SO).</span><span class="sxs-lookup"><span data-stu-id="3a25b-123">That is, not through an admin at object creation time; nor through the operating system (OS) itself.</span></span> <span data-ttu-id="3a25b-124">Un componente fuera del servicio de firewall debe realizar la resolución de direcciones IP para estos objetos y actualizarlos correctamente.</span><span class="sxs-lookup"><span data-stu-id="3a25b-124">A component outside of the firewall service must do the IP address resolution for these objects, and update them appropriately.</span></span> <span data-ttu-id="3a25b-125">La implementación de este componente está fuera del ámbito de este contenido.</span><span class="sxs-lookup"><span data-stu-id="3a25b-125">The implementation of such a component is outside the scope of this content.</span></span>

<span data-ttu-id="3a25b-126">Una dirección de palabra clave dinámica se indica como *AutoResolve* estableciendo la marca FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE en el objeto al llamar **a** la función [**FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="3a25b-126">A dynamic keyword address is indicated as being *AutoResolve* by setting the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag in the object when calling the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span> <span data-ttu-id="3a25b-127">El *campo de* palabra clave debe usarse para representar el valor que se resuelve, es decir, un nombre de dominio completo &mdash; (FQDN) o nombre de host.</span><span class="sxs-lookup"><span data-stu-id="3a25b-127">The *keyword* field should be used to represent the value being resolved&mdash;that is, a fully qualified domain name (FQDN) or hostname.</span></span> <span data-ttu-id="3a25b-128">El *campo de* direcciones debe ser NULL inicialmente para estos objetos.</span><span class="sxs-lookup"><span data-stu-id="3a25b-128">The *addresses* field must initially be NULL for these objects.</span></span> <span data-ttu-id="3a25b-129">Estos objetos no tendrán sus direcciones IP persistentes en los ciclos de arranque y debe volver a evaluar o volver a rellenar sus direcciones durante el siguiente ciclo de arranque.</span><span class="sxs-lookup"><span data-stu-id="3a25b-129">These objects won't have their IP addresses persisted across boot cycles, and you should re-evaluate/re-populate their addresses during the next boot cycle.</span></span>

> [!NOTE]
> <span data-ttu-id="3a25b-130">Los objetos de dirección de palabras clave dinámicas AutoResolve desencadenan notificaciones [**en FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) y [**FWDeleteDynamicKeywordAddress0,**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)pero [**no en FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span><span class="sxs-lookup"><span data-stu-id="3a25b-130">AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) and [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), but not [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="non-autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="3a25b-131">Direcciones de palabras clave dinámicas que no son de AutoResolve</span><span class="sxs-lookup"><span data-stu-id="3a25b-131">Non-AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="3a25b-132">El segundo tipo no *es AutoResolve,* donde el campo de palabra clave es cualquier cadena y las direcciones se definen en el momento de la creación. </span><span class="sxs-lookup"><span data-stu-id="3a25b-132">The second type is *non-AutoResolve*, where the *keyword* field is any string, and the addresses are defined at creation time.</span></span>

<span data-ttu-id="3a25b-133">Estos objetos se usan para almacenar un conjunto de direcciones IP, subredes o intervalos.</span><span class="sxs-lookup"><span data-stu-id="3a25b-133">These objects are used to store a set of IP address, subnets, or ranges.</span></span> <span data-ttu-id="3a25b-134">El *campo de* palabra clave aquí se usa para mayor comodidad de administración y se puede establecer en cualquier cadena.</span><span class="sxs-lookup"><span data-stu-id="3a25b-134">The *keyword* field here is used for management convenience, and it can be set to any string.</span></span> <span data-ttu-id="3a25b-135">El *campo de* direcciones debe ser distinto de NULL tras la creación.</span><span class="sxs-lookup"><span data-stu-id="3a25b-135">The *addresses* field must be non-NULL upon creation.</span></span> <span data-ttu-id="3a25b-136">Las direcciones de estos objetos se conservan en los reinicios.</span><span class="sxs-lookup"><span data-stu-id="3a25b-136">Addresses for these objects are persisted across reboots.</span></span>

> [!NOTE]
> <span data-ttu-id="3a25b-137">Los objetos de dirección de palabras clave dinámicas que no son AutoResolve desencadenan notificaciones [**en FWAddDynamicKeywordAddress0,**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)y [**también FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span><span class="sxs-lookup"><span data-stu-id="3a25b-137">Non-AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), and also [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="more-about-dynamic-keyword-addresses"></a><span data-ttu-id="3a25b-138">Más información sobre las direcciones de palabras clave dinámicas</span><span class="sxs-lookup"><span data-stu-id="3a25b-138">More about dynamic keyword addresses</span></span> 

<span data-ttu-id="3a25b-139">Todas las direcciones de palabras clave dinámicas deben tener un [**identificador GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) único para representarlas.</span><span class="sxs-lookup"><span data-stu-id="3a25b-139">All dynamic keyword addresses must have a unique [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) identifier to represent them.</span></span>

<span data-ttu-id="3a25b-140">La API [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) entrega notificaciones a un cliente cuando cambian las direcciones de palabras clave dinámicas.</span><span class="sxs-lookup"><span data-stu-id="3a25b-140">The [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) API delivers notifications to a client when dynamic keyword addresses change.</span></span> <span data-ttu-id="3a25b-141">No se entrega ninguna carga al cliente que describa exactamente lo que ha cambiado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="3a25b-141">There's no payload delivered to the client describing exactly what changed on the system.</span></span> <span data-ttu-id="3a25b-142">Si necesita saber qué objetos han cambiado, debe consultar el estado actual de los objetos en el sistema mediante las API [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) o [**FWEnumDynamicKeywordAddressesByType0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0)</span><span class="sxs-lookup"><span data-stu-id="3a25b-142">If you need to know what objects changed, then you should query the current state of objects on the system using the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) or [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) APIs.</span></span> <span data-ttu-id="3a25b-143">Puede usar las distintas marcas para solicitar notificaciones solo para un subconjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="3a25b-143">You can use the various flags to request notifications for only a subset of objects.</span></span> <span data-ttu-id="3a25b-144">Si no usa marcas, se entregarán notificaciones de cambio para todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="3a25b-144">If you use no flags, then change notifications will be delivered for all objects.</span></span>

<span data-ttu-id="3a25b-145">Una regla de firewall puede usar direcciones de palabra clave dinámicas en lugar de definir explícitamente direcciones IP para su condición de dirección remota.</span><span class="sxs-lookup"><span data-stu-id="3a25b-145">A firewall rule can use dynamic keyword addresses instead of explicitly defining IP addresses for its remote address condition.</span></span> <span data-ttu-id="3a25b-146">Una regla de firewall puede usar direcciones de palabras clave dinámicas e intervalos de direcciones remotas definidos estáticamente.</span><span class="sxs-lookup"><span data-stu-id="3a25b-146">A firewall rule can use both dynamic keyword addresses and statically defined remote address ranges.</span></span> <span data-ttu-id="3a25b-147">Un único objeto de dirección de palabra clave dinámica se puede volver a usar en varias reglas de firewall.</span><span class="sxs-lookup"><span data-stu-id="3a25b-147">A single dynamic keyword address object can be re-used across multiple firewall rules.</span></span> <span data-ttu-id="3a25b-148">Si una regla de firewall no tiene ninguna dirección remota configurada (es decir, configurada solo con objetos AutoResolve que aún no se han resuelto), la regla no se aplicará.</span><span class="sxs-lookup"><span data-stu-id="3a25b-148">If a firewall rule doesn't have any configured remote addresses (that is, configured with only AutoResolve objects which have not yet been resolved), then the rule won't be enforced.</span></span> <span data-ttu-id="3a25b-149">Además, si una regla usa varias direcciones de palabra clave dinámicas, la regla se aplicará para todas las direcciones que se resuelven actualmente, incluso si hay otros objetos que aún no se han resuelto.</span><span class="sxs-lookup"><span data-stu-id="3a25b-149">Furthermore, if a rule uses multiple dynamic keyword addresses, then the rule will be enforced for all addresses that are currently resolved, even if there are other objects that are not yet resolved.</span></span> <span data-ttu-id="3a25b-150">Cuando se actualiza una dirección de palabra clave dinámica, todos los objetos de regla asociados también tendrán sus direcciones remotas actualizadas.</span><span class="sxs-lookup"><span data-stu-id="3a25b-150">When a dynamic keyword address is updated, all associated rule objects will have their remote addresses updated as well.</span></span>

<span data-ttu-id="3a25b-151">El propio sistema operativo (SO) no aplica ninguna dependencia entre una regla y una dirección de palabra clave dinámica.</span><span class="sxs-lookup"><span data-stu-id="3a25b-151">The operating system (OS) itself doesn't enforce any dependencies between a rule and a dynamic keyword address.</span></span> <span data-ttu-id="3a25b-152">Esto significa que cualquiera de los objetos se puede crear primero; la regla puede hacer referencia a los IDs de direcciones de palabras clave dinámicas que aún no existen (en cuyo caso, no se aplicará &mdash; la regla).</span><span class="sxs-lookup"><span data-stu-id="3a25b-152">This means that either object can be created first&mdash;the rule can reference dynamic keyword address IDs that don't yet exist (in which case, the rule won't be enforced).</span></span> <span data-ttu-id="3a25b-153">Además, puede eliminar una dirección de palabra clave dinámica incluso si está en uso por una regla de firewall.</span><span class="sxs-lookup"><span data-stu-id="3a25b-153">Furthermore, you can delete a dynamic keyword address even if it's in use by a firewall rule.</span></span> <span data-ttu-id="3a25b-154">En este tema se describe cómo un administrador puede configurar reglas para usar la dirección de palabra clave dinámica.</span><span class="sxs-lookup"><span data-stu-id="3a25b-154">This topic outlines how an admin can configure rules to use dynamic keyword address.</span></span>

## <a name="code-examples"></a><span data-ttu-id="3a25b-155">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="3a25b-155">Code examples</span></span>

<span data-ttu-id="3a25b-156">Para probar cada uno de estos ejemplos de código, primero inicie Visual Studio y cree un proyecto basado en la plantilla de proyecto **Aplicación** de consola.</span><span class="sxs-lookup"><span data-stu-id="3a25b-156">To try out each of these code examples, first launch Visual Studio and create a new project based on the **Console App** project template.</span></span> <span data-ttu-id="3a25b-157">Solo puede reemplazar el contenido de `main.cpp` por la lista de código.</span><span class="sxs-lookup"><span data-stu-id="3a25b-157">You can just replace the contents of `main.cpp` with the code listing.</span></span>

<span data-ttu-id="3a25b-158">La mayoría de los ejemplos de código usan las [bibliotecas de implementación de Windows (WIL).](https://github.com/Microsoft/wil)</span><span class="sxs-lookup"><span data-stu-id="3a25b-158">Most of the code examples use the [Windows Implementation Libraries (WIL)](https://github.com/Microsoft/wil).</span></span> <span data-ttu-id="3a25b-159">Una manera cómoda de instalar WIL es ir  a Visual Studio, hacer clic en Project Manage NuGet Packages... (Administrar proyectos paquetes NuGet... Examinar), escribir o pegar \>  \>  **Microsoft.Windows.ImplementationLibrary**  en el cuadro de búsqueda, seleccionar el elemento en los resultados de la búsqueda y, a continuación, hacer clic en Instalar para instalar el paquete para ese proyecto.</span><span class="sxs-lookup"><span data-stu-id="3a25b-159">A convenient way to install WIL is to go to Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.Windows.ImplementationLibrary** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

> [!NOTE]
> <span data-ttu-id="3a25b-160">Los tipos de puntero para las funciones gratuitas de NetFw se publican a través de , pero no se publica una biblioteca de vínculos `NetFw.h` estáticos.</span><span class="sxs-lookup"><span data-stu-id="3a25b-160">Pointer types for the NetFw free functions are published via `NetFw.h`, but a static-link library isn't published.</span></span> <span data-ttu-id="3a25b-161">Use el [patrón LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)GetProcAddress para llamar a / [](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) estas funciones, como se muestra en estos ejemplos de código.</span><span class="sxs-lookup"><span data-stu-id="3a25b-161">Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling these functions, as shown in these code examples.</span></span>

### <a name="add-a-dynamic-keyword-address"></a><span data-ttu-id="3a25b-162">Adición de una dirección de palabra clave dinámica</span><span class="sxs-lookup"><span data-stu-id="3a25b-162">Add a dynamic keyword address</span></span>

<span data-ttu-id="3a25b-163">En este ejemplo se muestra cómo usar la [**función FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="3a25b-163">This example shows how to use the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a><span data-ttu-id="3a25b-164">Eliminación de una dirección de palabra clave dinámica</span><span class="sxs-lookup"><span data-stu-id="3a25b-164">Delete a dynamic keyword address</span></span>

<span data-ttu-id="3a25b-165">En este ejemplo se muestra cómo usar la [**función FWDeleteDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="3a25b-165">This example shows how to use the [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a><span data-ttu-id="3a25b-166">Enumerar y liberar direcciones de palabras clave dinámicas por identificador</span><span class="sxs-lookup"><span data-stu-id="3a25b-166">Enumerate and free dynamic keyword addresses by ID</span></span>

<span data-ttu-id="3a25b-167">En este ejemplo se muestra cómo usar las [**funciones FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) [**y FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)</span><span class="sxs-lookup"><span data-stu-id="3a25b-167">This example shows how to use the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a><span data-ttu-id="3a25b-168">Enumerar y liberar direcciones de palabras clave dinámicas por tipo</span><span class="sxs-lookup"><span data-stu-id="3a25b-168">Enumerate and free dynamic keyword addresses by type</span></span>

<span data-ttu-id="3a25b-169">En este ejemplo se muestra cómo usar las funciones [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) y [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)</span><span class="sxs-lookup"><span data-stu-id="3a25b-169">This example shows how to use the [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a><span data-ttu-id="3a25b-170">Actualización de direcciones de palabras clave dinámicas</span><span class="sxs-lookup"><span data-stu-id="3a25b-170">Update dynamic keyword addresses</span></span>

<span data-ttu-id="3a25b-171">En este ejemplo se muestra cómo usar la [**función FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="3a25b-171">This example shows how to use the [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a><span data-ttu-id="3a25b-172">Suscripción y control de notificaciones de cambio de dirección de palabras clave dinámicas</span><span class="sxs-lookup"><span data-stu-id="3a25b-172">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="3a25b-173">En este ejemplo se muestra cómo usar las funciones [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) y [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) y la devolución FWPM_DYNAMIC_KEYWORD_CALLBACK0 [**de**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) llamada.</span><span class="sxs-lookup"><span data-stu-id="3a25b-173">This example shows how to use the [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) and [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) functions, and the [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) callback.</span></span>

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a><span data-ttu-id="3a25b-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3a25b-174">Related topics</span></span>

* [<span data-ttu-id="3a25b-175">Referencia de palabras clave dinámicas de firewall</span><span class="sxs-lookup"><span data-stu-id="3a25b-175">Firewall dynamic keywords reference</span></span>](firewall-dynamic-keywords-reference.md)
