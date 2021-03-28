---
description: Representa una colección de las ventanas abiertas que pertenecen al shell. Los métodos asociados a estos objetos pueden controlar y ejecutar comandos en el Shell y obtener otros objetos relacionados con el shell.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Objeto ShellWindows (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985566"
---
# <a name="shellwindows-object"></a><span data-ttu-id="bf27c-104">Objeto ShellWindows</span><span class="sxs-lookup"><span data-stu-id="bf27c-104">ShellWindows object</span></span>

<span data-ttu-id="bf27c-105">Representa una colección de las ventanas abiertas que pertenecen al shell.</span><span class="sxs-lookup"><span data-stu-id="bf27c-105">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="bf27c-106">Los métodos asociados a estos objetos pueden controlar y ejecutar comandos en el Shell y obtener otros objetos relacionados con el shell.</span><span class="sxs-lookup"><span data-stu-id="bf27c-106">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="bf27c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf27c-107">Members</span></span>

<span data-ttu-id="bf27c-108">El objeto **ShellWindows** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bf27c-108">The **ShellWindows** object has these types of members:</span></span>

-   [<span data-ttu-id="bf27c-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf27c-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="bf27c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf27c-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bf27c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf27c-111">Methods</span></span>

<span data-ttu-id="bf27c-112">El objeto **ShellWindows** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bf27c-112">The **ShellWindows** object has these methods.</span></span>



| <span data-ttu-id="bf27c-113">Método</span><span class="sxs-lookup"><span data-stu-id="bf27c-113">Method</span></span>                                                 | <span data-ttu-id="bf27c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf27c-114">Description</span></span>                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf27c-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="bf27c-115">**\_NewEnum**</span></span>](shellwindows--newenum-method-7ral.md) | <span data-ttu-id="bf27c-116">Crea y devuelve un nuevo objeto **ShellWindows** que es una copia de este objeto **ShellWindows** .</span><span class="sxs-lookup"><span data-stu-id="bf27c-116">Creates and returns a new **ShellWindows** object that is a copy of this **ShellWindows** object.</span></span><br/>        |
| [<span data-ttu-id="bf27c-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="bf27c-117">**Item**</span></span>](shellwindows-item.md)                      | <span data-ttu-id="bf27c-118">Recupera un objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa la ventana del shell.</span><span class="sxs-lookup"><span data-stu-id="bf27c-118">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bf27c-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf27c-119">Properties</span></span>

<span data-ttu-id="bf27c-120">El objeto **ShellWindows** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bf27c-120">The **ShellWindows** object has these properties.</span></span>



| <span data-ttu-id="bf27c-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf27c-121">Property</span></span>                                       | <span data-ttu-id="bf27c-122">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="bf27c-122">Access type</span></span>          | <span data-ttu-id="bf27c-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf27c-123">Description</span></span>                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="bf27c-124">**Count**</span><span class="sxs-lookup"><span data-stu-id="bf27c-124">**Count**</span></span>](shellwindows-count.md)<br/> | <span data-ttu-id="bf27c-125">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf27c-125">Read-only</span></span><br/> | <span data-ttu-id="bf27c-126">Contiene el número de elementos de la colección.</span><span class="sxs-lookup"><span data-stu-id="bf27c-126">Contains the number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bf27c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf27c-127">Requirements</span></span>



| <span data-ttu-id="bf27c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf27c-128">Requirement</span></span> | <span data-ttu-id="bf27c-129">Value</span><span class="sxs-lookup"><span data-stu-id="bf27c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf27c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf27c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bf27c-131">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="bf27c-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bf27c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf27c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bf27c-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf27c-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bf27c-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf27c-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf27c-135"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf27c-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="bf27c-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bf27c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf27c-137"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bf27c-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
