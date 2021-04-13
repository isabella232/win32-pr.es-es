---
description: La biblioteca de administración de MTS incluida con las interfaces de administración de COM+ proporciona compatibilidad con versiones anteriores de la biblioteca de administración de MTS 2,0.
ms.assetid: 5eb9e68c-4f3b-4d57-bd51-704211d817fe
title: Biblioteca de administración de MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45e4be3cdad6b5b5f4e45c32261a7f94845839ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538806"
---
# <a name="mts-administration-library"></a><span data-ttu-id="2353e-103">Biblioteca de administración de MTS</span><span class="sxs-lookup"><span data-stu-id="2353e-103">MTS Administration Library</span></span>

<span data-ttu-id="2353e-104">La biblioteca de administración de MTS incluida con las interfaces de administración de COM+ proporciona compatibilidad con versiones anteriores de la biblioteca de administración de MTS 2,0.</span><span class="sxs-lookup"><span data-stu-id="2353e-104">The MTS Administration Library shipped with the COM+ Administration interfaces provides backward compatibility with the MTS 2.0 Administration Library.</span></span> <span data-ttu-id="2353e-105">La mayoría del código de administración de MTS 2,0 existente seguirá funcionando con la biblioteca MTSAdmin que se proporciona. sin embargo, algunas funciones han cambiado.</span><span class="sxs-lookup"><span data-stu-id="2353e-105">Most existing MTS 2.0 administration code will still work with the MTSAdmin Library that is provided; however, some functionality has changed.</span></span>

<span data-ttu-id="2353e-106">Para aprovechar las ventajas de la nueva funcionalidad o si está escribiendo código de administración por primera vez, debe usar la biblioteca COMAdmin.</span><span class="sxs-lookup"><span data-stu-id="2353e-106">To take advantage of new functionality or if you are writing administration code for the first time, you should use the COMAdmin Library.</span></span>

<span data-ttu-id="2353e-107">Los siguientes elementos de la biblioteca de administración de MTS actual se han modificado desde la biblioteca de administración de MTS 2,0:</span><span class="sxs-lookup"><span data-stu-id="2353e-107">The following elements in the current MTS Administration Library are changed from the MTS 2.0 Administration Library:</span></span>

-   <span data-ttu-id="2353e-108">La interfaz **IRemoteComponentUtil** ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2353e-108">The **IRemoteComponentUtil** interface is no longer available.</span></span>
-   <span data-ttu-id="2353e-109">La colección **RemoteComponents** ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2353e-109">The **RemoteComponents** collection is no longer available.</span></span>
-   <span data-ttu-id="2353e-110">La propiedad RoleID ya no está disponible, ya que el nombre de rol se usa como clave para este.</span><span class="sxs-lookup"><span data-stu-id="2353e-110">The RoleID property is no longer available, the Role Name is now used as the key for this.</span></span>
-   <span data-ttu-id="2353e-111">El método **ExportPackage** ya no exporta un client.exe.</span><span class="sxs-lookup"><span data-stu-id="2353e-111">The **ExportPackage** method no longer exports a client.exe.</span></span>
-   <span data-ttu-id="2353e-112">La propiedad RemoteComponentInstallPath ya no se expone en la colección [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="2353e-112">The RemoteComponentInstallPath property is no longer exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="2353e-113">La propiedad ApplicationInstallPath ya no se expondrá en la colección [**LocalComputer**](localcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="2353e-113">The ApplicationInstallPath property will no longer be exposed on the [**LocalComputer**](localcomputer.md) collection.</span></span>
-   <span data-ttu-id="2353e-114">El paquete del sistema se llama ahora aplicación del sistema.</span><span class="sxs-lookup"><span data-stu-id="2353e-114">The System package is now named System Application.</span></span>
-   <span data-ttu-id="2353e-115">El paquete de utilidades se llama ahora utilidades COM+.</span><span class="sxs-lookup"><span data-stu-id="2353e-115">The Utilities package is now named COM+ Utilities.</span></span>
-   <span data-ttu-id="2353e-116">La propiedad IsSystem existe en la colección de [**componentes**](components.md) de MTSAdmin, pero devolverá "NotImpl" cuando esté activada y no se guardará si se establece.</span><span class="sxs-lookup"><span data-stu-id="2353e-116">The IsSystem property exists in the [**Components**](components.md) collection in MTSAdmin but will return "NotImpl" when checked and will not be saved if set.</span></span>
-   <span data-ttu-id="2353e-117">La colección de [**componentes**](components.md) ya no admite la propiedad packagename.</span><span class="sxs-lookup"><span data-stu-id="2353e-117">The PackageName property is no longer supported by the [**Components**](components.md) collection.</span></span> <span data-ttu-id="2353e-118">Para averiguar el nombre del paquete, ahora necesitará obtener el PackageID y, a continuación, buscar el paquete coincidente en la colección de paquetes.</span><span class="sxs-lookup"><span data-stu-id="2353e-118">To figure out the package's name, you will now need to get the PackageID and then find the matching package in the Packages collection.</span></span>
-   <span data-ttu-id="2353e-119">Las siguientes propiedades ya no existen en la colección [**InterfacesForComponent**](interfacesforcomponent.md) :</span><span class="sxs-lookup"><span data-stu-id="2353e-119">The following properties no longer exist on the [**InterfacesForComponent**](interfacesforcomponent.md) collection:</span></span>
    -   <span data-ttu-id="2353e-120">**ProxyCLSID**</span><span class="sxs-lookup"><span data-stu-id="2353e-120">**ProxyCLSID**</span></span>
    -   <span data-ttu-id="2353e-121">**ProxyDLL**</span><span class="sxs-lookup"><span data-stu-id="2353e-121">**ProxyDLL**</span></span>
    -   <span data-ttu-id="2353e-122">**ProxyThreadingModel**</span><span class="sxs-lookup"><span data-stu-id="2353e-122">**ProxyThreadingModel**</span></span>
    -   <span data-ttu-id="2353e-123">**TypeLibFile**</span><span class="sxs-lookup"><span data-stu-id="2353e-123">**TypeLibFile**</span></span>
    -   <span data-ttu-id="2353e-124">**TypeLibID**</span><span class="sxs-lookup"><span data-stu-id="2353e-124">**TypeLibID**</span></span>
    -   <span data-ttu-id="2353e-125">**TypeLibLangID**</span><span class="sxs-lookup"><span data-stu-id="2353e-125">**TypeLibLangID**</span></span>
    -   <span data-ttu-id="2353e-126">**TypeLibPlatform**</span><span class="sxs-lookup"><span data-stu-id="2353e-126">**TypeLibPlatform**</span></span>
    -   <span data-ttu-id="2353e-127">**TypeLibVersion**</span><span class="sxs-lookup"><span data-stu-id="2353e-127">**TypeLibVersion**</span></span>

## <a name="related-topics"></a><span data-ttu-id="2353e-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2353e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2353e-129">Conversión automática desde MTS</span><span class="sxs-lookup"><span data-stu-id="2353e-129">Automatic Conversion from MTS</span></span>](automatic-conversion-from-mts.md)
</dt> <dt>

[<span data-ttu-id="2353e-130">Resultados y problemas de la conversión de COM+</span><span class="sxs-lookup"><span data-stu-id="2353e-130">COM+ Conversion Results and Issues</span></span>](com--conversion-results-and-issues.md)
</dt> <dt>

[<span data-ttu-id="2353e-131">Conversión manual desde MTS</span><span class="sxs-lookup"><span data-stu-id="2353e-131">Manual Conversion from MTS</span></span>](manual-conversion-from-mts.md)
</dt> </dl>

 

 



