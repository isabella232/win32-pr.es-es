---
description: La tabla CreateFolder contiene referencias a las carpetas que se deben crear explícitamente para un componente determinado.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: CreateFolder (tabla)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277983"
---
# <a name="createfolder-table"></a><span data-ttu-id="f6808-103">CreateFolder (tabla)</span><span class="sxs-lookup"><span data-stu-id="f6808-103">CreateFolder Table</span></span>

<span data-ttu-id="f6808-104">La tabla CreateFolder contiene referencias a las carpetas que se deben crear explícitamente para un componente determinado.</span><span class="sxs-lookup"><span data-stu-id="f6808-104">The CreateFolder table contains references to folders that need to be created explicitly for a particular component.</span></span>

<span data-ttu-id="f6808-105">La tabla CreateFolder tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="f6808-105">The CreateFolder table has the following columns.</span></span>



| <span data-ttu-id="f6808-106">Columna</span><span class="sxs-lookup"><span data-stu-id="f6808-106">Column</span></span>      | <span data-ttu-id="f6808-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6808-107">Type</span></span>                         | <span data-ttu-id="f6808-108">Clave</span><span class="sxs-lookup"><span data-stu-id="f6808-108">Key</span></span> | <span data-ttu-id="f6808-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="f6808-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="f6808-110">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="f6808-110">Directory\_</span></span> | [<span data-ttu-id="f6808-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="f6808-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="f6808-112">Y</span><span class="sxs-lookup"><span data-stu-id="f6808-112">Y</span></span>   | <span data-ttu-id="f6808-113">N</span><span class="sxs-lookup"><span data-stu-id="f6808-113">N</span></span>        |
| <span data-ttu-id="f6808-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="f6808-114">Component\_</span></span> | [<span data-ttu-id="f6808-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="f6808-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="f6808-116">Y</span><span class="sxs-lookup"><span data-stu-id="f6808-116">Y</span></span>   | <span data-ttu-id="f6808-117">N</span><span class="sxs-lookup"><span data-stu-id="f6808-117">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f6808-118">Columnas</span><span class="sxs-lookup"><span data-stu-id="f6808-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f6808-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_</span><span class="sxs-lookup"><span data-stu-id="f6808-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="f6808-120">Clave externa en la primera columna de la [tabla de directorio](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6808-120">External key into the first column of the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6808-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="f6808-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="f6808-122">Clave externa en la primera columna de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6808-122">External key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6808-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6808-123">Remarks</span></span>

<span data-ttu-id="f6808-124">Las carpetas de esta tabla se crean cuando se instala el componente.</span><span class="sxs-lookup"><span data-stu-id="f6808-124">The folders in this table are created when the component is installed.</span></span> <span data-ttu-id="f6808-125">Se realiza un intento de quitar estas carpetas solo cuando el componente se desinstala o se mueve a ejecutar desde el origen.</span><span class="sxs-lookup"><span data-stu-id="f6808-125">An attempt is made to remove these folders only when the component is uninstalled or moved to run-from-source.</span></span> <span data-ttu-id="f6808-126">No se desencadena ninguna eliminación automática si las carpetas están vacías.</span><span class="sxs-lookup"><span data-stu-id="f6808-126">No automatic removal is triggered if the folders become empty.</span></span> <span data-ttu-id="f6808-127">Por el contrario, las carpetas creadas por el instalador pero que no aparecen en esta tabla se quitan cuando están vacías.</span><span class="sxs-lookup"><span data-stu-id="f6808-127">In contrast, folders created by the installer but not listed in this table are removed when they become empty.</span></span>

<span data-ttu-id="f6808-128">Dado que las carpetas creadas por el instalador se eliminan cuando están vacías, debe crear una entrada en la tabla CreateFolder para instalar un componente que se compone de una carpeta vacía.</span><span class="sxs-lookup"><span data-stu-id="f6808-128">Because folders created by the installer are deleted when they become empty, you must author an entry into the CreateFolder table to install a component that consists of an empty folder.</span></span>

<span data-ttu-id="f6808-129">Se hace referencia a esta tabla cuando se llama a la acción [CreateFolders](createfolders-action.md) o a la acción [RemoveFolders](removefolders-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f6808-129">This table is referred to when the [CreateFolders](createfolders-action.md) action or the [RemoveFolders](removefolders-action.md) action is called.</span></span>

<span data-ttu-id="f6808-130">Para obtener información sobre cómo proteger una carpeta, vea la [tabla MsiLockPermissionsEx](msilockpermissionsex-table.md) y la [tabla LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6808-130">For information on how to secure a folder see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f6808-131">Validación</span><span class="sxs-lookup"><span data-stu-id="f6808-131">Validation</span></span>

<dl>

[<span data-ttu-id="f6808-132">ICE03</span><span class="sxs-lookup"><span data-stu-id="f6808-132">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f6808-133">ICE06</span><span class="sxs-lookup"><span data-stu-id="f6808-133">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f6808-134">ICE18</span><span class="sxs-lookup"><span data-stu-id="f6808-134">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="f6808-135">ICE32</span><span class="sxs-lookup"><span data-stu-id="f6808-135">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f6808-136">ICE55</span><span class="sxs-lookup"><span data-stu-id="f6808-136">ICE55</span></span>](ice55.md)  
</dl>

 

 



