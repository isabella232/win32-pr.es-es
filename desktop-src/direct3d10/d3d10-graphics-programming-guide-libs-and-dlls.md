---
description: Para que una aplicación se ejecute correctamente, el equipo host debe tener instalados los archivos dll adecuados. El sistema operativo o el paquete redistribuible de las aplicaciones pueden proporcionar estos archivos dll.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Vinculación de bibliotecas estáticas y dinámicas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696106"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a><span data-ttu-id="e922d-104">Vinculación de bibliotecas estáticas y dinámicas (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e922d-104">Linking Static and Dynamic Libraries (Direct3D 10)</span></span>

<span data-ttu-id="e922d-105">Para que una aplicación se ejecute correctamente, el equipo host debe tener instalados los archivos dll adecuados.</span><span class="sxs-lookup"><span data-stu-id="e922d-105">For an application to run properly, the host computer must have the appropriate DLLs installed.</span></span> <span data-ttu-id="e922d-106">El sistema operativo o el paquete redistribuible de las aplicaciones pueden proporcionar estos archivos dll.</span><span class="sxs-lookup"><span data-stu-id="e922d-106">These DLLs may be provided by either the operating system, or the applications' redistributable package.</span></span>

## <a name="libraries-load-appropriate-dlls"></a><span data-ttu-id="e922d-107">Las bibliotecas cargan los archivos dll adecuados</span><span class="sxs-lookup"><span data-stu-id="e922d-107">Libraries Load Appropriate DLLs</span></span>

<span data-ttu-id="e922d-108">Las bibliotecas incluidas con el SDK de DirectX cargarán automáticamente los archivos dll adecuados en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="e922d-108">The libraries included with the DirectX SDK will automatically load the proper DLLs at runtime.</span></span> <span data-ttu-id="e922d-109">La excepción a esta regla es d3dx10. lib/d3dx10d. lib, que cargará el d3dx10.dll que se distribuyó con esa versión del SDK.</span><span class="sxs-lookup"><span data-stu-id="e922d-109">The exception to this rule is d3dx10.lib/d3dx10d.lib, which will load the d3dx10.dll that was shipped with that version of the SDK.</span></span> <span data-ttu-id="e922d-110">Por ejemplo, si el SDK descargado incluye d3dx10 \_33.dll y d3dx10 \_34.dll, la biblioteca (d3dx10. lib) que se suministra con ese SDK cargará d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="e922d-110">For example, if the downloaded SDK includes d3dx10\_33.dll and d3dx10\_34.dll, then the library (d3dx10.lib) that shipped with that SDK will load d3dx10\_34.dll.</span></span> <span data-ttu-id="e922d-111">Si se instala posteriormente un SDK posterior que contiene d3dx10 \_ 35. lib, d3dx10. lib del SDK anterior seguirá cargando d3dx10 \_34.dll.</span><span class="sxs-lookup"><span data-stu-id="e922d-111">If a subsequent SDK is installed later containing d3dx10\_35.lib, the d3dx10.lib from the previous SDK will still load d3dx10\_34.dll.</span></span> <span data-ttu-id="e922d-112">El d3dx10. lib del SDK más reciente cargará d3dx10 \_35.dll.</span><span class="sxs-lookup"><span data-stu-id="e922d-112">The d3dx10.lib from the newer SDK will load d3dx10\_35.dll.</span></span>

## <a name="redistributing-binaries"></a><span data-ttu-id="e922d-113">Redistribuir archivos binarios</span><span class="sxs-lookup"><span data-stu-id="e922d-113">Redistributing Binaries</span></span>

<span data-ttu-id="e922d-114">Solo se pueden redistribuir d3dx10.dll (y las versiones posteriores del mismo archivo).</span><span class="sxs-lookup"><span data-stu-id="e922d-114">Only d3dx10.dll (and subsequent versions of the same file) can be redistributed.</span></span> <span data-ttu-id="e922d-115">Para redistribuir este archivo, debe utilizar la función **DirectXSetup** .</span><span class="sxs-lookup"><span data-stu-id="e922d-115">To redistribute this file, you must use the **DirectXSetup** function.</span></span> <span data-ttu-id="e922d-116">Para más información sobre el uso de esta función y la agrupación de un paquete redistribuible, consulte [instalación de DirectX con DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="e922d-116">For details on using this function and putting together a redistributable package, see [Installing DirectX with DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx).</span></span> <span data-ttu-id="e922d-117">El resto de los binarios necesarios se incluyen en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e922d-117">All other necessary binaries are included in Windows Vista.</span></span> <span data-ttu-id="e922d-118">Los únicos binarios que se pueden redistribuir son los que se encuentran en el siguiente directorio.</span><span class="sxs-lookup"><span data-stu-id="e922d-118">The only binaries that can be redistributed are those located in the following directory.</span></span>


```
(SDK root)\Redist
```



<span data-ttu-id="e922d-119">En la tabla siguiente se describen los archivos binarios que los desarrolladores deben tener en cuenta.</span><span class="sxs-lookup"><span data-stu-id="e922d-119">The following table describes the binaries developers should be aware of.</span></span>



| <span data-ttu-id="e922d-120">Archivos binarios de Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="e922d-120">Direct3D 10 Binaries</span></span>   | <span data-ttu-id="e922d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e922d-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e922d-122">d3dx10.dll/d3dx10d.dll</span><span class="sxs-lookup"><span data-stu-id="e922d-122">d3dx10.dll/d3dx10d.dll</span></span> | <span data-ttu-id="e922d-123">Componentes D3DX10 comerciales y de depuración; los componentes comerciales se pueden redistribuir en el archivo CAB de Redist.</span><span class="sxs-lookup"><span data-stu-id="e922d-123">Retail and debug D3DX10 components; the retail components can be redistributed in the REDIST CAB.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="e922d-124">d3d10ref.dll</span><span class="sxs-lookup"><span data-stu-id="e922d-124">d3d10ref.dll</span></span>           | <span data-ttu-id="e922d-125">Rasterizador de referencia.</span><span class="sxs-lookup"><span data-stu-id="e922d-125">Reference Rasterizer.</span></span> <span data-ttu-id="e922d-126">Proporciona la implementación de software de la canalización de gráficos.</span><span class="sxs-lookup"><span data-stu-id="e922d-126">Provides software implementation of the graphics pipeline.</span></span> <span data-ttu-id="e922d-127">Solo se incluye como parte del SDK de DirectX Windows SDK o heredado y no se puede redistribuir.</span><span class="sxs-lookup"><span data-stu-id="e922d-127">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> <span data-ttu-id="e922d-128">El rasterizador de referencia está pensado únicamente para la depuración.</span><span class="sxs-lookup"><span data-stu-id="e922d-128">The Reference Rasterizer is intended for debugging only.</span></span> <span data-ttu-id="e922d-129">No es necesaria la vinculación explícita; Si se intenta crear un dispositivo de referencia (consulte [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)), se cargará este archivo dll si está presente.</span><span class="sxs-lookup"><span data-stu-id="e922d-129">Explicit linking is not necessary; attempting to create a reference device (see [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) will load this dll if it is present.</span></span>                                                                                                    |
| <span data-ttu-id="e922d-130">d3d10sdklayers.dll</span><span class="sxs-lookup"><span data-stu-id="e922d-130">d3d10sdklayers.dll</span></span>     | <span data-ttu-id="e922d-131">Una serie de utilidades de SDK que actúan como una capa entre las llamadas API y la ejecución en tiempo de ejecución, incluida la [capa de depuración](d3d10-graphics-programming-guide-api-features-layers.md) y la capa de cambio a referencia.</span><span class="sxs-lookup"><span data-stu-id="e922d-131">A series of SDK utilities that act as a layer between API calls and runtime execution, including the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) and the switch-to-reference layer.</span></span> <span data-ttu-id="e922d-132">No es necesaria la vinculación explícita; Si un dispositivo se crea con la marca de capa adecuada, este archivo DLL se carga automáticamente.</span><span class="sxs-lookup"><span data-stu-id="e922d-132">Explicit linking is not necessary; if a device is created with the appropriate layer flag, this DLL is loaded automatically.</span></span> <span data-ttu-id="e922d-133">Este componente está pensado únicamente para fines de desarrollo y depuración.</span><span class="sxs-lookup"><span data-stu-id="e922d-133">This component is meant for development and debugging purposes only.</span></span> <span data-ttu-id="e922d-134">Solo se incluye como parte del SDK de DirectX Windows SDK o heredado y no se puede redistribuir.</span><span class="sxs-lookup"><span data-stu-id="e922d-134">Only included as part of the Windows SDK or legacy DirectX SDK and cannot be redistributed.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e922d-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e922d-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e922d-136">Guía de programación para Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="e922d-136">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="e922d-137">Gráficos de Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="e922d-137">Direct3D 10 Graphics</span></span>](d3d10-graphics.md)
</dt> </dl>

 

 



