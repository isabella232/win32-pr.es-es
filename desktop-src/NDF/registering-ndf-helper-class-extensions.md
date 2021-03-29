---
title: Registro de extensiones de clase auxiliar NDF
description: Cada extensión de clase auxiliar tiene una serie de claves del registro asociadas. COM requiere algunas claves y NDF requiere algunas claves.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780208"
---
# <a name="registering-ndf-helper-class-extensions"></a><span data-ttu-id="d792e-104">Registro de extensiones de clase auxiliar NDF</span><span class="sxs-lookup"><span data-stu-id="d792e-104">Registering NDF Helper Class Extensions</span></span>

<span data-ttu-id="d792e-105">Cada extensión de clase auxiliar tiene una serie de claves del registro asociadas.</span><span class="sxs-lookup"><span data-stu-id="d792e-105">Each helper class extension has a number of registry keys associated with it.</span></span> <span data-ttu-id="d792e-106">COM requiere algunas claves y NDF requiere algunas claves.</span><span class="sxs-lookup"><span data-stu-id="d792e-106">Some keys are required by COM, and some keys are required by NDF.</span></span>

## <a name="com-registry-keys"></a><span data-ttu-id="d792e-107">Claves del registro COM</span><span class="sxs-lookup"><span data-stu-id="d792e-107">COM Registry Keys</span></span>

<span data-ttu-id="d792e-108">Las extensiones de clase auxiliares deben implementarse como servidores COM.</span><span class="sxs-lookup"><span data-stu-id="d792e-108">Helper class extensions must be implemented as COM servers.</span></span> <span data-ttu-id="d792e-109">Se debe completar el registro COM para cada extensión de clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="d792e-109">COM registration must be completed for each helper class extension.</span></span> <span data-ttu-id="d792e-110">Se debe registrar el CLSID del objeto, la interfaz [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) y la interfaz [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) .</span><span class="sxs-lookup"><span data-stu-id="d792e-110">The object's CLSID, the [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) interface, and the [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) interface must be registered.</span></span> <span data-ttu-id="d792e-111">El registro crea un número de claves del registro relacionadas con COM para la extensión de clase auxiliar NDF.</span><span class="sxs-lookup"><span data-stu-id="d792e-111">Registration creates a number of COM-related registry keys for the NDF helper class extension.</span></span>

## <a name="ndf-registry-keys"></a><span data-ttu-id="d792e-112">Claves del registro NDF</span><span class="sxs-lookup"><span data-stu-id="d792e-112">NDF Registry Keys</span></span>

<span data-ttu-id="d792e-113">Las extensiones de clase auxiliares deben registrarse antes de interactuar con el marco de diagnóstico de red y con otras clases auxiliares relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d792e-113">Helper class extensions must be registered before interacting with the Network Diagnostics Framework and with other related helper classes.</span></span> <span data-ttu-id="d792e-114">Esto se logra rellenando el registro.</span><span class="sxs-lookup"><span data-stu-id="d792e-114">This is accomplished by populating the registry.</span></span>

<span data-ttu-id="d792e-115">En el procedimiento siguiente se muestra cómo agregar extensiones de clase auxiliar al registro.</span><span class="sxs-lookup"><span data-stu-id="d792e-115">The following procedure shows how to add helper class extensions to the registry.</span></span>

1.  <span data-ttu-id="d792e-116">Publique los nombres de las clases auxiliares implementadas por el archivo DLL y sus dependencias mediante la creación de una clave para la DLL en</span><span class="sxs-lookup"><span data-stu-id="d792e-116">Publish the names of helper classes implemented by the DLL and their dependencies by creating a key for the DLL under</span></span>

    <span data-ttu-id="d792e-117">**HKLM \\ System \\ CurrentControlSet \\ control \\ NetDiagFx** \\ *NombreProveedor* \\ **HostDLLs** \\ *clase de aplicación auxiliar* \\ **HelperClasses** \\ *nombre de clase auxiliar*</span><span class="sxs-lookup"><span data-stu-id="d792e-117">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*</span></span>

    <span data-ttu-id="d792e-118">Reemplace *NombreProveedor*, el *archivo dll de la clase auxiliar* y *el nombre de clase auxiliar* por valores definidos por el usuario, tal y como se describe a continuación.</span><span class="sxs-lookup"><span data-stu-id="d792e-118">Replace *VendorName*, *Helper Class DLL*, and *Helper Class Name* with user-defined values as described below.</span></span>

    | <span data-ttu-id="d792e-119">Value</span><span class="sxs-lookup"><span data-stu-id="d792e-119">Value</span></span>               | <span data-ttu-id="d792e-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="d792e-120">Type</span></span>    | <span data-ttu-id="d792e-121">Significado</span><span class="sxs-lookup"><span data-stu-id="d792e-121">Meaning</span></span>                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | <span data-ttu-id="d792e-122">*VendorName*</span><span class="sxs-lookup"><span data-stu-id="d792e-122">*VendorName*</span></span>        | <span data-ttu-id="d792e-123">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d792e-123">REG\_SZ</span></span> | <span data-ttu-id="d792e-124">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="d792e-124">The name of the vendor.</span></span>                                                      |
    | <span data-ttu-id="d792e-125">*DLL de clase auxiliar*</span><span class="sxs-lookup"><span data-stu-id="d792e-125">*Helper Class DLL*</span></span>  | <span data-ttu-id="d792e-126">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d792e-126">REG\_SZ</span></span> | <span data-ttu-id="d792e-127">Nombre del archivo DLL, sin extensión.</span><span class="sxs-lookup"><span data-stu-id="d792e-127">Name of the DLL, without extension.</span></span>                                          |
    | <span data-ttu-id="d792e-128">*Nombre de clase auxiliar*</span><span class="sxs-lookup"><span data-stu-id="d792e-128">*Helper Class Name*</span></span> | <span data-ttu-id="d792e-129">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d792e-129">REG\_SZ</span></span> | <span data-ttu-id="d792e-130">Nombre de la clase auxiliar de la que depende la clase auxiliar actual.</span><span class="sxs-lookup"><span data-stu-id="d792e-130">The name of the helper class on which the current helper class is dependent.</span></span> |

    

     

2.  <span data-ttu-id="d792e-131">En cada clave de *nombre de clase auxiliar* , publique la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="d792e-131">Under each *Helper Class Name* key, publish the following information.</span></span>

    

    | <span data-ttu-id="d792e-132">Value</span><span class="sxs-lookup"><span data-stu-id="d792e-132">Value</span></span>         | <span data-ttu-id="d792e-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="d792e-133">Type</span></span>       | <span data-ttu-id="d792e-134">Significado</span><span class="sxs-lookup"><span data-stu-id="d792e-134">Meaning</span></span>                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="d792e-135">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="d792e-135">**CLSID**</span></span>     | <span data-ttu-id="d792e-136">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d792e-136">REG\_SZ</span></span>    | <span data-ttu-id="d792e-137">Cadena que contiene el identificador de clase COM de la clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="d792e-137">A string that contains the COM class ID of the helper class.</span></span>                                                                                                            |
    | <span data-ttu-id="d792e-138">**Versión**</span><span class="sxs-lookup"><span data-stu-id="d792e-138">**Version**</span></span>   | <span data-ttu-id="d792e-139">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d792e-139">REG\_SZ</span></span>    | <span data-ttu-id="d792e-140">Una cadena que contiene las versiones principal y secundaria de la clase auxiliar en el formato <major> <minor> .</span><span class="sxs-lookup"><span data-stu-id="d792e-140">A string the contains the major and minor versions of the helper class in the format <major><minor>.</span></span>                                                        |
    | <span data-ttu-id="d792e-141">**Publicado**</span><span class="sxs-lookup"><span data-stu-id="d792e-141">**Published**</span></span> | <span data-ttu-id="d792e-142">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="d792e-142">REG\_DWORD</span></span> | <span data-ttu-id="d792e-143">Un valor de 1 significa que se espera que esta clase auxiliar se invoque directamente desde el cliente de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="d792e-143">A value of 1 means that this helper class is expected to be directly invoked from the Diagnostics client.</span></span> <span data-ttu-id="d792e-144">0 significa que solo se puede llamar desde otra clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="d792e-144">0 means that it can be called only from another helper class.</span></span> |
    | <span data-ttu-id="d792e-145">**Parent**</span><span class="sxs-lookup"><span data-stu-id="d792e-145">**Parent**</span></span>    | <span data-ttu-id="d792e-146">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d792e-146">REG\_SZ</span></span>    | <span data-ttu-id="d792e-147">Cadena que nombra la clase auxiliar extensible de Microsoft que se va a extender.</span><span class="sxs-lookup"><span data-stu-id="d792e-147">A string that names the Microsoft extensible helper class that is being extended.</span></span>                                                                                       |

    

     

3.  <span data-ttu-id="d792e-148">Para cada clase auxiliar, publique la lista de atributos coincidentes mediante la creación de una clave en</span><span class="sxs-lookup"><span data-stu-id="d792e-148">For each helper class, publish the list of matching attributes by creating a key under</span></span>

    <span data-ttu-id="d792e-149">**HKLM \\ System \\ CurrentControlSet \\ control \\ NetDiagFx** \\ *NombreProveedor* \\ **HostDLLs** \\ *clase auxiliar* \\ **HelperClasses** \\ *nombre de clase auxiliar* \\ **MatchAttributes**</span><span class="sxs-lookup"><span data-stu-id="d792e-149">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*\\**MatchAttributes**</span></span>

    <span data-ttu-id="d792e-150">La clave debe contener uno o más valores (uno por atributo) del tipo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d792e-150">They key must contain one or more values (one per attribute) of the following type.</span></span>

    | <span data-ttu-id="d792e-151">Value</span><span class="sxs-lookup"><span data-stu-id="d792e-151">Value</span></span>             | <span data-ttu-id="d792e-152">Tipo</span><span class="sxs-lookup"><span data-stu-id="d792e-152">Type</span></span>                             | <span data-ttu-id="d792e-153">Significado</span><span class="sxs-lookup"><span data-stu-id="d792e-153">Meaning</span></span>                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="d792e-154">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="d792e-154">**AttributeName**</span></span> | <span data-ttu-id="d792e-155">REG. reg. \_ \| \_ DWORD \| reg \_ binario</span><span class="sxs-lookup"><span data-stu-id="d792e-155">REG\_SZ\|REG\_DWORD\|REG\_BINARY</span></span> | <span data-ttu-id="d792e-156">Valor que completa el par de nombre y valor para un atributo determinado.</span><span class="sxs-lookup"><span data-stu-id="d792e-156">A value that completes the name and value pair for a particular attribute.</span></span> |

    

     

 

 




