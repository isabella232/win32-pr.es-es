---
description: Los scripts y las aplicaciones escritas para sistemas operativos de 32 bits deben seguir ejecutándose correctamente.
ms.assetid: b437b9ed-b9e4-4fc5-9b86-0eb77bb41b8e
ms.tgt_platform: multiple
title: Proporcionar datos WMI en una plataforma de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1d6b348c16765014c4eb6988b64976ba3f11a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543686"
---
# <a name="providing-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="86567-103">Proporcionar datos WMI en una plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="86567-103">Providing WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="86567-104">Los scripts y las aplicaciones escritas para sistemas operativos de 32 bits deben seguir ejecutándose correctamente.</span><span class="sxs-lookup"><span data-stu-id="86567-104">Scripts and applications written for 32-bit operating systems should continue to run properly.</span></span> <span data-ttu-id="86567-105">Si tiene un proveedor de 32 bits existente, puede evaluar si tiene que escribir una versión de 64 bits para la operación en paralelo.</span><span class="sxs-lookup"><span data-stu-id="86567-105">If you have an existing 32-bit provider, you can evaluate whether you need to write a 64-bit version for side-by-side operation.</span></span> <span data-ttu-id="86567-106">Por lo general, ambas versiones no son necesarias y la versión de 64 bits puede atender a clientes locales o remotos de 32 y 64 bits.</span><span class="sxs-lookup"><span data-stu-id="86567-106">Generally, both versions are not necessary and the 64-bit version can service both 32-bit and 64-bit local or remote clients.</span></span> <span data-ttu-id="86567-107">Sin embargo, para el modo de compatibilidad de aplicaciones de 32 bits, use el proveedor de WMI de 32 bits existente en un sistema de 64 bits que se ejecute en el modo WOW64 de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="86567-107">However, for 32-bit application compatibility mode, use your existing 32-bit WMI provider on a 64-bit system that runs in the 32-bit WOW64 mode.</span></span>

<span data-ttu-id="86567-108">En raras ocasiones, los proveedores de 32 bits y 64 bits deben ejecutarse en paralelo en sistemas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="86567-108">In rare situations, both the 32-bit and 64-bit providers must run side-by-side on 64-bit systems.</span></span> <span data-ttu-id="86567-109">En este caso, la versión adecuada del proveedor que se carga depende de si el llamador es de 32 bits o de 64 bits y local o remoto.</span><span class="sxs-lookup"><span data-stu-id="86567-109">In this case, the appropriate version of provider that is loaded depends on whether the caller is 32-bit or 64-bit and local or remote.</span></span> <span data-ttu-id="86567-110">Un autor de llamada que usa las marcas de contexto del objeto de conexión, **\_ \_ ProviderArchitecture** y **\_ \_ RequiredArchitecture**, puede solicitar que WMI cargue un proveedor no predeterminado.</span><span class="sxs-lookup"><span data-stu-id="86567-110">A caller using the connection object context flags, **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture**, can request that WMI load a nondefault provider.</span></span> <span data-ttu-id="86567-111">Para obtener más información, consulte [obtener y proporcionar datos en un equipo de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md).</span><span class="sxs-lookup"><span data-stu-id="86567-111">For more information, see [Getting and Providing Data on a 64-bit Computer](getting-and-providing-data-on-a-64-bit-computer.md).</span></span>

<span data-ttu-id="86567-112">En el caso inusual de que deba ejecutar los proveedores de 32 bits y 64 bits en paralelo, debe asegurarse de que los escenarios de instalación y desinstalación se controlan con cuidado.</span><span class="sxs-lookup"><span data-stu-id="86567-112">In the unusual case that you must run both the 32-bit and 64-bit providers side-by-side, then you must ensure that install and uninstall scenarios are handled carefully.</span></span> <span data-ttu-id="86567-113">Esto se debe a que WMI solo tiene un [*repositorio*](gloss-w.md) y las versiones de 32 bits y 64 bits de [**mofcomp.exe**](mofcomp.md) colocan los datos en el mismo repositorio. no hay distinción entre un archivo. mof de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="86567-113">This is because WMI has only one [*repository*](gloss-w.md) and both the 32-bit and 64-bit versions of [**mofcomp.exe**](mofcomp.md) put the data in the same repository; there is no distinction between a 32-bit or a 64-bit .mof file.</span></span> <span data-ttu-id="86567-114">La reinstalación de una versión del proveedor no perjudicará: los archivos. mof se compilarán y las clases almacenadas en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="86567-114">Reinstalling one version of the provider will not hurt: the .mof files will be compiled and the classes stored in the repository.</span></span> <span data-ttu-id="86567-115">Sin embargo, una segunda desinstalación que elimina un espacio de nombres puede interferir con el funcionamiento del otro proveedor.</span><span class="sxs-lookup"><span data-stu-id="86567-115">However, a second uninstall that deletes a namespace can interfere with the operation of the other provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86567-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86567-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86567-117">Obtener y proporcionar datos en un equipo de 64 bits</span><span class="sxs-lookup"><span data-stu-id="86567-117">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> <dt>

[<span data-ttu-id="86567-118">Solicitar datos WMI en una plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="86567-118">Requesting WMI Data on a 64-bit Platform</span></span>](requesting-wmi-data-on-a-64-bit-platform.md)
</dt> <dt>

[<span data-ttu-id="86567-119">Proporcionar datos a WMI</span><span class="sxs-lookup"><span data-stu-id="86567-119">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> </dl>

 

 



