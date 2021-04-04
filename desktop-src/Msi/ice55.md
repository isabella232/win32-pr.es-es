---
description: ICE55 valida que todos los objetos LockPermission existen y tienen valores de permiso válidos.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278158"
---
# <a name="ice55"></a><span data-ttu-id="cbead-103">ICE55</span><span class="sxs-lookup"><span data-stu-id="cbead-103">ICE55</span></span>

<span data-ttu-id="cbead-104">ICE55 valida que todos los objetos LockPermission existen y tienen valores de permiso válidos.</span><span class="sxs-lookup"><span data-stu-id="cbead-104">ICE55 validates that all LockPermission objects exist and have valid permission values.</span></span>

## <a name="result"></a><span data-ttu-id="cbead-105">Resultado</span><span class="sxs-lookup"><span data-stu-id="cbead-105">Result</span></span>

<span data-ttu-id="cbead-106">ICE55 registra un error si no existe un LockObject enumerado en la [tabla LockPermissions](lockpermissions-table.md) o si no se especifica ningún nivel de privilegios en la columna Permission.</span><span class="sxs-lookup"><span data-stu-id="cbead-106">ICE55 post an error if a LockObject listed in the [LockPermissions table](lockpermissions-table.md) does not exist or if no privilege level is specified in the Permission column.</span></span>

## <a name="example"></a><span data-ttu-id="cbead-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cbead-107">Example</span></span>

<span data-ttu-id="cbead-108">ICE55 notificaría los siguientes errores para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="cbead-108">ICE55 would report the following errors for the example.</span></span>

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

<span data-ttu-id="cbead-109">[Tabla LockPermissions](lockpermissions-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="cbead-109">[LockPermissions Table](lockpermissions-table.md) (partial)</span></span>



| <span data-ttu-id="cbead-110">LockObject</span><span class="sxs-lookup"><span data-stu-id="cbead-110">LockObject</span></span> | <span data-ttu-id="cbead-111">Tabla</span><span class="sxs-lookup"><span data-stu-id="cbead-111">Table</span></span> | <span data-ttu-id="cbead-112">Domain</span><span class="sxs-lookup"><span data-stu-id="cbead-112">Domain</span></span> | <span data-ttu-id="cbead-113">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="cbead-113">User</span></span>  | <span data-ttu-id="cbead-114">Permiso</span><span class="sxs-lookup"><span data-stu-id="cbead-114">Permission</span></span> |
|------------|-------|--------|-------|------------|
| <span data-ttu-id="cbead-115">Archivo1</span><span class="sxs-lookup"><span data-stu-id="cbead-115">File1</span></span>      | <span data-ttu-id="cbead-116">Archivo</span><span class="sxs-lookup"><span data-stu-id="cbead-116">File</span></span>  |        | <span data-ttu-id="cbead-117">guest</span><span class="sxs-lookup"><span data-stu-id="cbead-117">guest</span></span> |            |
| <span data-ttu-id="cbead-118">File3</span><span class="sxs-lookup"><span data-stu-id="cbead-118">File3</span></span>      | <span data-ttu-id="cbead-119">Archivo</span><span class="sxs-lookup"><span data-stu-id="cbead-119">File</span></span>  |        | <span data-ttu-id="cbead-120">guest</span><span class="sxs-lookup"><span data-stu-id="cbead-120">guest</span></span> | <span data-ttu-id="cbead-121">1</span><span class="sxs-lookup"><span data-stu-id="cbead-121">1</span></span>          |



 

<span data-ttu-id="cbead-122">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="cbead-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="cbead-123">Archivo</span><span class="sxs-lookup"><span data-stu-id="cbead-123">File</span></span>  | <span data-ttu-id="cbead-124">Versión</span><span class="sxs-lookup"><span data-stu-id="cbead-124">Version</span></span> | <span data-ttu-id="cbead-125">Idioma</span><span class="sxs-lookup"><span data-stu-id="cbead-125">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="cbead-126">Archivo1</span><span class="sxs-lookup"><span data-stu-id="cbead-126">File1</span></span> | <span data-ttu-id="cbead-127">Archivo2</span><span class="sxs-lookup"><span data-stu-id="cbead-127">File2</span></span>   |          |
| <span data-ttu-id="cbead-128">Archivo2</span><span class="sxs-lookup"><span data-stu-id="cbead-128">File2</span></span> | <span data-ttu-id="cbead-129">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="cbead-129">1.0.0.0</span></span> | <span data-ttu-id="cbead-130">3082</span><span class="sxs-lookup"><span data-stu-id="cbead-130">1033</span></span>     |



 

<span data-ttu-id="cbead-131">El objeto archivo1 tiene un valor null en la columna Permission.</span><span class="sxs-lookup"><span data-stu-id="cbead-131">The object File1 has a null in the Permission column.</span></span> <span data-ttu-id="cbead-132">Cada fila debe tener un valor en la columna permisos.</span><span class="sxs-lookup"><span data-stu-id="cbead-132">Each row must have a value in the Permissions column.</span></span> <span data-ttu-id="cbead-133">Para corregir este error, especifique un valor numérico en esta columna.</span><span class="sxs-lookup"><span data-stu-id="cbead-133">To fix this error specify a numeric value in this column.</span></span> <span data-ttu-id="cbead-134">Si no se necesitan privilegios para este objeto, debe quitar la fila.</span><span class="sxs-lookup"><span data-stu-id="cbead-134">If no privileges are needed for this object then you should remove the row.</span></span>

<span data-ttu-id="cbead-135">El objeto Archivo3 descrito en la tabla LockPermissions no aparece en la tabla de archivos.</span><span class="sxs-lookup"><span data-stu-id="cbead-135">The object File3 described in the LockPermissions table is not listed in the File table.</span></span> <span data-ttu-id="cbead-136">Para corregir este error, consulte un objeto válido.</span><span class="sxs-lookup"><span data-stu-id="cbead-136">To fix this error refer to a valid object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbead-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cbead-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbead-138">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="cbead-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



