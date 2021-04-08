---
description: Escriba los registros de las cinco acciones personalizadas de ejemplo creadas en la sección anterior en la tabla CustomAction. Para obtener más información sobre cómo rellenar la tabla CustomAction para este tipo de acción personalizada, vea acción personalizada tipo 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Creación de la tabla CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001723"
---
# <a name="authoring-the-customaction-table"></a><span data-ttu-id="235d9-104">Creación de la tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="235d9-104">Authoring the CustomAction Table</span></span>

<span data-ttu-id="235d9-105">Escriba los registros de las cinco acciones personalizadas de ejemplo creadas en la sección anterior en la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="235d9-105">Enter records for the five sample custom actions created in the previous section to the [CustomAction Table](customaction-table.md).</span></span> <span data-ttu-id="235d9-106">Para obtener más información sobre cómo rellenar la tabla CustomAction para este tipo de acción personalizada, vea [acción personalizada tipo 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="235d9-106">For more information on how to populate the CustomAction table for this type of custom action see [Custom Action Type 1](custom-action-type-1.md).</span></span>

[<span data-ttu-id="235d9-107">Tabla CustomAction</span><span class="sxs-lookup"><span data-stu-id="235d9-107">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="235d9-108">Acción</span><span class="sxs-lookup"><span data-stu-id="235d9-108">Action</span></span>            | <span data-ttu-id="235d9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="235d9-109">Type</span></span>  | <span data-ttu-id="235d9-110">Source</span><span class="sxs-lookup"><span data-stu-id="235d9-110">Source</span></span>      | <span data-ttu-id="235d9-111">Destino</span><span class="sxs-lookup"><span data-stu-id="235d9-111">Target</span></span>                |
|-------------------|-------|-------------|-----------------------|
| <span data-ttu-id="235d9-112">ProcessAccounts</span><span class="sxs-lookup"><span data-stu-id="235d9-112">ProcessAccounts</span></span>   | <span data-ttu-id="235d9-113">1</span><span class="sxs-lookup"><span data-stu-id="235d9-113">1</span></span>     | <span data-ttu-id="235d9-114">Process.dll</span><span class="sxs-lookup"><span data-stu-id="235d9-114">Process.dll</span></span> | <span data-ttu-id="235d9-115">ProcessUserAccounts</span><span class="sxs-lookup"><span data-stu-id="235d9-115">ProcessUserAccounts</span></span>   |
| <span data-ttu-id="235d9-116">UninstallAccounts</span><span class="sxs-lookup"><span data-stu-id="235d9-116">UninstallAccounts</span></span> | <span data-ttu-id="235d9-117">1</span><span class="sxs-lookup"><span data-stu-id="235d9-117">1</span></span>     | <span data-ttu-id="235d9-118">Process.dll</span><span class="sxs-lookup"><span data-stu-id="235d9-118">Process.dll</span></span> | <span data-ttu-id="235d9-119">UninstallUserAccounts</span><span class="sxs-lookup"><span data-stu-id="235d9-119">UninstallUserAccounts</span></span> |
| <span data-ttu-id="235d9-120">CreateAccount</span><span class="sxs-lookup"><span data-stu-id="235d9-120">CreateAccount</span></span>     | <span data-ttu-id="235d9-121">11265</span><span class="sxs-lookup"><span data-stu-id="235d9-121">11265</span></span> | <span data-ttu-id="235d9-122">Create.dll</span><span class="sxs-lookup"><span data-stu-id="235d9-122">Create.dll</span></span>  | <span data-ttu-id="235d9-123">CreateUserAccount</span><span class="sxs-lookup"><span data-stu-id="235d9-123">CreateUserAccount</span></span>     |
| <span data-ttu-id="235d9-124">RemoveAccount</span><span class="sxs-lookup"><span data-stu-id="235d9-124">RemoveAccount</span></span>     | <span data-ttu-id="235d9-125">11265</span><span class="sxs-lookup"><span data-stu-id="235d9-125">11265</span></span> | <span data-ttu-id="235d9-126">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="235d9-126">Remove.dll</span></span>  | <span data-ttu-id="235d9-127">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="235d9-127">RemoveUserAccount</span></span>     |
| <span data-ttu-id="235d9-128">RollbackAccount</span><span class="sxs-lookup"><span data-stu-id="235d9-128">RollbackAccount</span></span>   | <span data-ttu-id="235d9-129">9473</span><span class="sxs-lookup"><span data-stu-id="235d9-129">9473</span></span>  | <span data-ttu-id="235d9-130">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="235d9-130">Remove.dll</span></span>  | <span data-ttu-id="235d9-131">RemoveUserAccount</span><span class="sxs-lookup"><span data-stu-id="235d9-131">RemoveUserAccount</span></span>     |



 

<span data-ttu-id="235d9-132">El código fuente de C++ de las bibliotecas de vínculos dinámicos se proporciona en el SDK de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="235d9-132">The C++ source code for the dynamic-link libraries are provided in the Windows Installer SDK.</span></span> <span data-ttu-id="235d9-133">Use Process. cpp para crear el archivo Process.dll.</span><span class="sxs-lookup"><span data-stu-id="235d9-133">Use Process.cpp to create the file Process.dll.</span></span> <span data-ttu-id="235d9-134">Utilice Create. cpp para crear el archivo Create.dll.</span><span class="sxs-lookup"><span data-stu-id="235d9-134">Use Create.cpp to create the file Create.dll.</span></span> <span data-ttu-id="235d9-135">Utilice Remove. cpp para crear Remove.dll.</span><span class="sxs-lookup"><span data-stu-id="235d9-135">Use Remove.cpp to create Remove.dll.</span></span> <span data-ttu-id="235d9-136">Agregue estos archivos de biblioteca de vínculos dinámicos a la tabla binaria.</span><span class="sxs-lookup"><span data-stu-id="235d9-136">Add these dynamic-link library files to the Binary table.</span></span>

[<span data-ttu-id="235d9-137">Tabla binaria</span><span class="sxs-lookup"><span data-stu-id="235d9-137">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="235d9-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="235d9-138">Name</span></span>        | <span data-ttu-id="235d9-139">Datos</span><span class="sxs-lookup"><span data-stu-id="235d9-139">Data</span></span>            |
|-------------|-----------------|
| <span data-ttu-id="235d9-140">Process.dll</span><span class="sxs-lookup"><span data-stu-id="235d9-140">Process.dll</span></span> | <span data-ttu-id="235d9-141">{*datos binarios*}</span><span class="sxs-lookup"><span data-stu-id="235d9-141">{*binary data*}</span></span> |
| <span data-ttu-id="235d9-142">Create.dll</span><span class="sxs-lookup"><span data-stu-id="235d9-142">Create.dll</span></span>  | <span data-ttu-id="235d9-143">{*datos binarios*}</span><span class="sxs-lookup"><span data-stu-id="235d9-143">{*binary data*}</span></span> |
| <span data-ttu-id="235d9-144">Remove.dll</span><span class="sxs-lookup"><span data-stu-id="235d9-144">Remove.dll</span></span>  | <span data-ttu-id="235d9-145">{*datos binarios*}</span><span class="sxs-lookup"><span data-stu-id="235d9-145">{*binary data*}</span></span> |



 

<span data-ttu-id="235d9-146">Continúe [agregando una tabla CustomUserAccounts personalizada](adding-a-custom-customuseraccounts-table.md).</span><span class="sxs-lookup"><span data-stu-id="235d9-146">Continue to [Adding a Custom CustomUserAccounts Table](adding-a-custom-customuseraccounts-table.md).</span></span>

 

 



