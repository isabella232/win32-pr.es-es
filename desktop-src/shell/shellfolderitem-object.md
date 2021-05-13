---
description: Extiende el objeto FolderItem. Además de las propiedades y los métodos admitidos por FolderItem, ShellFolderItem tiene dos métodos adicionales.
title: Objeto ShellFolderItem (Shldisp.h)
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
ms.openlocfilehash: a9e6d6b3f954f0c8ee4b13fb651a9ea04274deb6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840776"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="8164e-104">Objeto ShellFolderItem</span><span class="sxs-lookup"><span data-stu-id="8164e-104">ShellFolderItem object</span></span>

<span data-ttu-id="8164e-105">Extiende el [**objeto FolderItem.**](folderitem.md)</span><span class="sxs-lookup"><span data-stu-id="8164e-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="8164e-106">Además de las propiedades y los métodos admitidos **por FolderItem,** **ShellFolderItem** tiene dos métodos adicionales.</span><span class="sxs-lookup"><span data-stu-id="8164e-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="8164e-107">Members</span><span class="sxs-lookup"><span data-stu-id="8164e-107">Members</span></span>

<span data-ttu-id="8164e-108">El **objeto ShellFolderItem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8164e-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="8164e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8164e-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8164e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8164e-110">Methods</span></span>

<span data-ttu-id="8164e-111">El **objeto ShellFolderItem** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8164e-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="8164e-112">Método</span><span class="sxs-lookup"><span data-stu-id="8164e-112">Method</span></span>                                                       | <span data-ttu-id="8164e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8164e-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8164e-114">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="8164e-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="8164e-115">Obtiene el valor de una propiedad del conjunto de propiedades de un elemento.</span><span class="sxs-lookup"><span data-stu-id="8164e-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="8164e-116">La propiedad se puede especificar por nombre o por el identificador de formato (FMTID) y el identificador de propiedad (PID) del conjunto de propiedades.</span><span class="sxs-lookup"><span data-stu-id="8164e-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="8164e-117">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="8164e-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="8164e-118">Ejecuta un verbo en un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="8164e-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="8164e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8164e-119">Requirements</span></span>



| <span data-ttu-id="8164e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8164e-120">Requirement</span></span> | <span data-ttu-id="8164e-121">Value</span><span class="sxs-lookup"><span data-stu-id="8164e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8164e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8164e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8164e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8164e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8164e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8164e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8164e-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8164e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8164e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8164e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8164e-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="8164e-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8164e-128">Idl</span><span class="sxs-lookup"><span data-stu-id="8164e-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8164e-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="8164e-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8164e-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8164e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8164e-131"><dt>Shell32.dll (versión 5.0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8164e-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




