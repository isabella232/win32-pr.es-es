---
description: Windows Vista presenta nuevos escenarios de almacenamiento y un nuevo espacio de nombres de Perfil de usuario.
title: Carpetas conocidas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7527b7242c68f0d6c78cd0fae427626c182302f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985782"
---
# <a name="known-folders"></a><span data-ttu-id="f2fd7-103">Carpetas conocidas</span><span class="sxs-lookup"><span data-stu-id="f2fd7-103">Known Folders</span></span>

<span data-ttu-id="f2fd7-104">Windows Vista presenta nuevos escenarios de almacenamiento y un nuevo espacio de nombres de Perfil de usuario.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-104">Windows Vista introduces new storage scenarios and a new user profile namespace.</span></span> <span data-ttu-id="f2fd7-105">Para abordar estos nuevos factores, se ha reemplazado el sistema anterior que hace referencia a las carpetas estándar mediante un valor [**CSIDL**](csidl.md) .</span><span class="sxs-lookup"><span data-stu-id="f2fd7-105">To address these new factors, the older system of referring to standard folders by a [**CSIDL**](csidl.md) value has been replaced.</span></span> <span data-ttu-id="f2fd7-106">A partir de Windows Vista, se hace referencia a esas carpetas mediante un nuevo conjunto de valores GUID denominados identificadores de carpeta conocidos.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-106">As of Windows Vista, those folders are referenced by a new set of GUID values called Known Folder IDs.</span></span>

<span data-ttu-id="f2fd7-107">El sistema de carpetas conocido proporciona estas ventajas:</span><span class="sxs-lookup"><span data-stu-id="f2fd7-107">The Known Folder system provides these advantages:</span></span>

-   <span data-ttu-id="f2fd7-108">Los fabricantes de software independientes (ISV) pueden extender el conjunto de identificadores de carpeta conocidos con los suyos propios.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-108">Independent software vendors (ISVs) can extend the set of Known Folder IDs with their own.</span></span> <span data-ttu-id="f2fd7-109">Pueden definir carpetas, asignarles identificadores y registrarlos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-109">They can define folders, give them IDs, and register them with the system.</span></span> <span data-ttu-id="f2fd7-110">No se pudieron extender los valores de CSIDL.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-110">CSIDL values could not be extended.</span></span>
-   <span data-ttu-id="f2fd7-111">Todas las carpetas conocidas de un sistema se pueden enumerar.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-111">All Known Folders on a system can be enumerated.</span></span> <span data-ttu-id="f2fd7-112">Ninguna API proporcionó esta funcionalidad para los valores CSIDL.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-112">No API provided this functionality for CSIDL values.</span></span> <span data-ttu-id="f2fd7-113">Vea [**IKnownFolderManager:: GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-113">See [**IKnownFolderManager::GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) for more information.</span></span>
-   <span data-ttu-id="f2fd7-114">Una carpeta conocida agregada por un ISV puede Agregar propiedades personalizadas que le permitan explicar su finalidad y el uso previsto.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-114">A known folder added by an ISV can add custom properties that allow it to explain its purpose and intended use.</span></span>
-   <span data-ttu-id="f2fd7-115">Muchas carpetas conocidas se pueden redirigir a nuevas ubicaciones, incluidas las ubicaciones de red.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-115">Many known folders can be redirected to new locations, including network locations.</span></span> <span data-ttu-id="f2fd7-116">En el sistema CSIDL, solo se podría redirigir la carpeta **Mis documentos** .</span><span class="sxs-lookup"><span data-stu-id="f2fd7-116">Under the CSIDL system, only the **My Documents** folder could be redirected.</span></span>
-   <span data-ttu-id="f2fd7-117">Las carpetas conocidas pueden tener controladores personalizados para su uso durante la creación o la eliminación.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-117">Known folders can have custom handlers for use during creation or deletion.</span></span>

<span data-ttu-id="f2fd7-118">Todavía se admite el sistema CSIDL y las API que hacen uso de los valores de CSIDL por compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-118">The CSIDL system and APIs that make use of CSIDL values are still supported for compatibility.</span></span> <span data-ttu-id="f2fd7-119">Sin embargo, no se recomienda usarlas en ningún desarrollo nuevo.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-119">However, it is not recommended to use them in any new development.</span></span>


<span data-ttu-id="f2fd7-120">En los temas siguientes se describen los detalles del sistema de carpetas conocidas.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-120">The following topics discuss the specifics of the Known Folders system.</span></span>

-   [<span data-ttu-id="f2fd7-121">Trabajar con carpetas conocidas en aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f2fd7-121">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
-   [<span data-ttu-id="f2fd7-122">Cómo extender carpetas conocidas con carpetas personalizadas</span><span class="sxs-lookup"><span data-stu-id="f2fd7-122">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
-   [<span data-ttu-id="f2fd7-123">**KNOWNFOLDERID**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-123">**KNOWNFOLDERID**</span></span>](knownfolderid.md)

<span data-ttu-id="f2fd7-124">Las siguientes páginas de referencia explican las funciones de carpetas conocidas de Win32, que se pueden usar para recuperar la ubicación de carpetas conocidas o redirigirlas a una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-124">The following reference pages explain the Win32 Known Folders functions, which can be used to retrieve the location of Known Folders or redirect them to a new location.</span></span> <span data-ttu-id="f2fd7-125">Estas funciones reemplazan a las funciones anteriores de Win32.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-125">These functions replace older Win32 functions.</span></span> <span data-ttu-id="f2fd7-126">Las nuevas funciones se proporcionan para proporcionar un comportamiento equivalente a las funciones anteriores, pero cada nueva función también se duplica mediante una API del modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="f2fd7-126">The new functions are provided to give equivalent behavior to the old functions, but each new function is also duplicated by a Component Object Model (COM) API.</span></span>



| <span data-ttu-id="f2fd7-127">Nueva función</span><span class="sxs-lookup"><span data-stu-id="f2fd7-127">New Function</span></span>                                             | <span data-ttu-id="f2fd7-128">Reemplazo</span><span class="sxs-lookup"><span data-stu-id="f2fd7-128">Replaces</span></span>                                           | <span data-ttu-id="f2fd7-129">Equivalente de COM</span><span class="sxs-lookup"><span data-stu-id="f2fd7-129">COM Equivalent</span></span>                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="f2fd7-130">**SHGetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-130">**SHGetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [<span data-ttu-id="f2fd7-131">**SHGetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-131">**SHGetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [<span data-ttu-id="f2fd7-132">**IKnownFolder::GetPath**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-132">**IKnownFolder::GetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [<span data-ttu-id="f2fd7-133">**SHGetKnownFolderIDList**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-133">**SHGetKnownFolderIDList**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [<span data-ttu-id="f2fd7-134">**SHGetFolderLocation**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-134">**SHGetFolderLocation**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [<span data-ttu-id="f2fd7-135">**IKnownFolder::GetIDList**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-135">**IKnownFolder::GetIDList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [<span data-ttu-id="f2fd7-136">**SHSetKnownFolderPath**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-136">**SHSetKnownFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [<span data-ttu-id="f2fd7-137">**SHSetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-137">**SHSetFolderPath**</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [<span data-ttu-id="f2fd7-138">**IKnownFolder::SetPath**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-138">**IKnownFolder::SetPath**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

<span data-ttu-id="f2fd7-139">Las siguientes páginas de referencia explican las API de carpetas conocidas de COM, que proporcionan toda la funcionalidad de las API de Win32 enumeradas anteriormente, además de agregar la capacidad de enumerar todas las carpetas conocidas, tener acceso a las propiedades de las carpetas conocidas y ampliar el conjunto estándar de carpetas conocidas.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-139">The following reference pages explain the COM Known Folders APIs, which provide all of the functionality of the Win32 APIs listed above, plus add the ability to enumerate all Known Folders, access Known Folder properties, and extend the standard set of Known Folders.</span></span>

-   [<span data-ttu-id="f2fd7-140">**IKnownFolder**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-140">**IKnownFolder**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [<span data-ttu-id="f2fd7-141">**IKnownFolderManager**</span><span class="sxs-lookup"><span data-stu-id="f2fd7-141">**IKnownFolderManager**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

<span data-ttu-id="f2fd7-142">En el kit de desarrollo de software (SDK) de Windows se incluye un ejemplo de C++ que muestra las API de carpeta conocidas.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-142">A C++ sample that demonstrates the Known Folder APIs is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f2fd7-143">Una vez que haya instalado el Windows SDK en el equipo, el ejemplo se puede encontrar en% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ AppPlatform \\ KnownFolders.</span><span class="sxs-lookup"><span data-stu-id="f2fd7-143">Once you have installed the Windows SDK on your computer, the sample can be found under %ProgramFiles%\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppPlatform\\KnownFolders.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2fd7-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2fd7-144">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f2fd7-145">[Ejemplo de carpetas conocidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2fd7-145">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
