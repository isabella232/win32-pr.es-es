---
description: Representa la colección de verbos para un elemento de una carpeta de Shell. Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.
title: Objeto FolderItemVerbs (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 31badb4b-b89e-4294-9dd7-bda716e163b2
ms.openlocfilehash: 8206c2113e2fa60abef41e43e4739b6eefd77dd4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840616"
---
# <a name="folderitemverbs-object"></a><span data-ttu-id="94698-104">Objeto FolderItemVerbs</span><span class="sxs-lookup"><span data-stu-id="94698-104">FolderItemVerbs object</span></span>

<span data-ttu-id="94698-105">Representa la colección de verbos para un elemento de una carpeta de Shell.</span><span class="sxs-lookup"><span data-stu-id="94698-105">Represents the collection of verbs for an item in a Shell folder.</span></span> <span data-ttu-id="94698-106">Este objeto contiene propiedades y métodos que permiten recuperar información sobre la colección.</span><span class="sxs-lookup"><span data-stu-id="94698-106">This object contains properties and methods that allow you to retrieve information about the collection.</span></span>

## <a name="members"></a><span data-ttu-id="94698-107">Members</span><span class="sxs-lookup"><span data-stu-id="94698-107">Members</span></span>

<span data-ttu-id="94698-108">El **objeto FolderItemVerbs** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="94698-108">The **FolderItemVerbs** object has these types of members:</span></span>

-   [<span data-ttu-id="94698-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="94698-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="94698-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94698-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="94698-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="94698-111">Methods</span></span>

<span data-ttu-id="94698-112">El **objeto FolderItemVerbs** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="94698-112">The **FolderItemVerbs** object has these methods.</span></span>



| <span data-ttu-id="94698-113">Método</span><span class="sxs-lookup"><span data-stu-id="94698-113">Method</span></span>                                        | <span data-ttu-id="94698-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="94698-114">Description</span></span>                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94698-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="94698-115">**\_NewEnum**</span></span>](folderitemverbs--newenum.md) | <span data-ttu-id="94698-116">Crea y devuelve un **nuevo objeto FolderItemVerbs** que es una copia de este objeto FolderItemVerbs.</span><span class="sxs-lookup"><span data-stu-id="94698-116">Creates and returns a new **FolderItemVerbs** object that is a copy of this FolderItemVerbs object.</span></span><br/>   |
| [<span data-ttu-id="94698-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="94698-117">**Item**</span></span>](folderitemverbs-item.md)          | <span data-ttu-id="94698-118">Recupera el [**objeto FolderItemVerb**](folderitemverb.md) para un elemento especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="94698-118">Retrieves the [**FolderItemVerb**](folderitemverb.md) object for a specified item in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="94698-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="94698-119">Properties</span></span>

<span data-ttu-id="94698-120">El **objeto FolderItemVerbs** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="94698-120">The **FolderItemVerbs** object has these properties.</span></span>



| <span data-ttu-id="94698-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="94698-121">Property</span></span>                                                      | <span data-ttu-id="94698-122">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="94698-122">Access type</span></span>          | <span data-ttu-id="94698-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="94698-123">Description</span></span>                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="94698-124">**Application**</span><span class="sxs-lookup"><span data-stu-id="94698-124">**Application**</span></span>](folderitemverbs-application.md)<br/> | <span data-ttu-id="94698-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="94698-125">Read-only</span></span><br/> | <span data-ttu-id="94698-126">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="94698-126">Not implemented.</span></span><br/>                                |
| [<span data-ttu-id="94698-127">**Contar**</span><span class="sxs-lookup"><span data-stu-id="94698-127">**Count**</span></span>](folderitemverbs-count.md)<br/>             | <span data-ttu-id="94698-128">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="94698-128">Read-only</span></span><br/> | <span data-ttu-id="94698-129">Contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="94698-129">Contains the number of items in the collection.</span></span><br/> |
| [<span data-ttu-id="94698-130">**Parent**</span><span class="sxs-lookup"><span data-stu-id="94698-130">**Parent**</span></span>](folderitemverbs-parent.md)<br/>           | <span data-ttu-id="94698-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="94698-131">Read-only</span></span><br/> | <span data-ttu-id="94698-132">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="94698-132">Not implemented.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="94698-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94698-133">Requirements</span></span>



| <span data-ttu-id="94698-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="94698-134">Requirement</span></span> | <span data-ttu-id="94698-135">Value</span><span class="sxs-lookup"><span data-stu-id="94698-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94698-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94698-136">Minimum supported client</span></span><br/> | <span data-ttu-id="94698-137">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="94698-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="94698-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94698-138">Minimum supported server</span></span><br/> | <span data-ttu-id="94698-139">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="94698-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="94698-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94698-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="94698-141"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="94698-141"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="94698-142">Idl</span><span class="sxs-lookup"><span data-stu-id="94698-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94698-143"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="94698-143"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="94698-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94698-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94698-145"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="94698-145"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




