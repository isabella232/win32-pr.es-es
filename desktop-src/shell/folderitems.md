---
description: Representa la colección de elementos de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.
title: Objeto FolderItems (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 6f9a6fa978c64c788cbd224cf3a39454c644a57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808017"
---
# <a name="folderitems-object"></a><span data-ttu-id="36e8e-104">Objeto FolderItems</span><span class="sxs-lookup"><span data-stu-id="36e8e-104">FolderItems object</span></span>

<span data-ttu-id="36e8e-105">Representa la colección de elementos de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="36e8e-105">Represents the collection of items in a Shell folder.</span></span> <span data-ttu-id="36e8e-106">Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.</span><span class="sxs-lookup"><span data-stu-id="36e8e-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="36e8e-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="36e8e-107">Members</span></span>

<span data-ttu-id="36e8e-108">El objeto **FolderItems** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="36e8e-108">The **FolderItems** object has these types of members:</span></span>

-   [<span data-ttu-id="36e8e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="36e8e-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="36e8e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36e8e-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="36e8e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="36e8e-111">Methods</span></span>

<span data-ttu-id="36e8e-112">El objeto **FolderItems** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="36e8e-112">The **FolderItems** object has these methods.</span></span>



| <span data-ttu-id="36e8e-113">Método</span><span class="sxs-lookup"><span data-stu-id="36e8e-113">Method</span></span>                                    | <span data-ttu-id="36e8e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="36e8e-114">Description</span></span>                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36e8e-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="36e8e-115">**\_NewEnum**</span></span>](folderitems--newenum.md) | <span data-ttu-id="36e8e-116">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="36e8e-116">Not implemented.</span></span><br/>                                                                              |
| [<span data-ttu-id="36e8e-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="36e8e-117">**Item**</span></span>](folderitems-item.md)          | <span data-ttu-id="36e8e-118">Recupera el objeto [**carpeta**](folderitem.md) para un elemento especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="36e8e-118">Retrieves the [**FolderItem**](folderitem.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="36e8e-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36e8e-119">Properties</span></span>

<span data-ttu-id="36e8e-120">El objeto **FolderItems** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="36e8e-120">The **FolderItems** object has these properties.</span></span>



| <span data-ttu-id="36e8e-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="36e8e-121">Property</span></span>                                                  | <span data-ttu-id="36e8e-122">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="36e8e-122">Access type</span></span>          | <span data-ttu-id="36e8e-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="36e8e-123">Description</span></span>                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36e8e-124">**Application**</span><span class="sxs-lookup"><span data-stu-id="36e8e-124">**Application**</span></span>](folderitems-application.md)<br/> | <span data-ttu-id="36e8e-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="36e8e-125">Read-only</span></span><br/> | <span data-ttu-id="36e8e-126">Contiene el objeto de [**aplicación**](folderitems-application.md) de la colección de elementos de carpeta.</span><span class="sxs-lookup"><span data-stu-id="36e8e-126">Contains the [**Application**](folderitems-application.md) object of the folder items collection.</span></span><br/> |
| [<span data-ttu-id="36e8e-127">**Count**</span><span class="sxs-lookup"><span data-stu-id="36e8e-127">**Count**</span></span>](folderitems-count.md)<br/>             | <span data-ttu-id="36e8e-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="36e8e-128">Read-only</span></span><br/> | <span data-ttu-id="36e8e-129">Contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="36e8e-129">Contains the number of items in the collection.</span></span><br/>                                                    |
| [<span data-ttu-id="36e8e-130">**Parent**</span><span class="sxs-lookup"><span data-stu-id="36e8e-130">**Parent**</span></span>](folderitems-parent.md)<br/>           | <span data-ttu-id="36e8e-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="36e8e-131">Read-only</span></span><br/> | <span data-ttu-id="36e8e-132">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="36e8e-132">Not implemented.</span></span><br/>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="36e8e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36e8e-133">Requirements</span></span>



| <span data-ttu-id="36e8e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="36e8e-134">Requirement</span></span> | <span data-ttu-id="36e8e-135">Value</span><span class="sxs-lookup"><span data-stu-id="36e8e-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36e8e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36e8e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="36e8e-137">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="36e8e-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="36e8e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36e8e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="36e8e-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="36e8e-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="36e8e-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36e8e-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="36e8e-141"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="36e8e-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="36e8e-142">IDL</span><span class="sxs-lookup"><span data-stu-id="36e8e-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36e8e-143"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36e8e-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="36e8e-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36e8e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36e8e-145"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="36e8e-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




