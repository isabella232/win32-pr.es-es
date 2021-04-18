---
description: Extiende el objeto carpeta. Además de las propiedades y los métodos admitidos por carpeta, ShellFolderItem tiene dos métodos adicionales.
title: Objeto ShellFolderItem (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: 84e230e295a956f3f83833a577b47be1e46873a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985878"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="4b752-104">Objeto ShellFolderItem</span><span class="sxs-lookup"><span data-stu-id="4b752-104">ShellFolderItem object</span></span>

<span data-ttu-id="4b752-105">Extiende el objeto [**carpeta**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="4b752-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="4b752-106">Además de las propiedades y los métodos admitidos por **carpeta**, **ShellFolderItem** tiene dos métodos adicionales.</span><span class="sxs-lookup"><span data-stu-id="4b752-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="4b752-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4b752-107">Members</span></span>

<span data-ttu-id="4b752-108">El objeto **ShellFolderItem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4b752-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="4b752-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="4b752-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4b752-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4b752-110">Methods</span></span>

<span data-ttu-id="4b752-111">El objeto **ShellFolderItem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4b752-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="4b752-112">Método</span><span class="sxs-lookup"><span data-stu-id="4b752-112">Method</span></span>                                                       | <span data-ttu-id="4b752-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b752-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4b752-114">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="4b752-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="4b752-115">Obtiene el valor de una propiedad del conjunto de propiedades de un elemento.</span><span class="sxs-lookup"><span data-stu-id="4b752-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="4b752-116">La propiedad se puede especificar por nombre o por el identificador de formato del conjunto de propiedades (FMTID) y el identificador de propiedad (PID).</span><span class="sxs-lookup"><span data-stu-id="4b752-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="4b752-117">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="4b752-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="4b752-118">Ejecuta un verbo en un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="4b752-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="4b752-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b752-119">Requirements</span></span>



| <span data-ttu-id="4b752-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b752-120">Requirement</span></span> | <span data-ttu-id="4b752-121">Value</span><span class="sxs-lookup"><span data-stu-id="4b752-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b752-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b752-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4b752-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4b752-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4b752-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4b752-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4b752-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4b752-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4b752-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4b752-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b752-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b752-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4b752-128">IDL</span><span class="sxs-lookup"><span data-stu-id="4b752-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b752-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b752-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4b752-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4b752-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b752-131"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="4b752-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




