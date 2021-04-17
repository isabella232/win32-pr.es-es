---
description: Este ejemplo permite al consumidor del módulo configurar de forma independiente un control de edición, el atributo checksum y el atributo Compressed.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Ejemplo de componente configurable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666675"
---
# <a name="configurable-component-example"></a><span data-ttu-id="37027-103">Ejemplo de componente configurable</span><span class="sxs-lookup"><span data-stu-id="37027-103">Configurable Component Example</span></span>

<span data-ttu-id="37027-104">En este ejemplo, las tablas ModuleConfiguration y ModuleSubstitution siguientes permiten al consumidor del módulo configurar de forma independiente el atributo de contraseña para un control de edición, el atributo de suma de comprobación para un archivo y el atributo comprimido para el mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="37027-104">In this example, the following ModuleConfiguration and ModuleSubstitution tables allows the module consumer to independently configure the Password attribute for an edit control, the checksum attribute for a file, and the compressed attribute for the same file.</span></span>

[<span data-ttu-id="37027-105">Tabla ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="37027-105">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="37027-106">Tabla</span><span class="sxs-lookup"><span data-stu-id="37027-106">Table</span></span>   | <span data-ttu-id="37027-107">Row</span><span class="sxs-lookup"><span data-stu-id="37027-107">Row</span></span>           | <span data-ttu-id="37027-108">Columna</span><span class="sxs-lookup"><span data-stu-id="37027-108">Column</span></span>     | <span data-ttu-id="37027-109">Valor</span><span class="sxs-lookup"><span data-stu-id="37027-109">Value</span></span>                        |
|---------|---------------|------------|------------------------------|
| <span data-ttu-id="37027-110">Control</span><span class="sxs-lookup"><span data-stu-id="37027-110">Control</span></span> | <span data-ttu-id="37027-111">Dialog1; Edit1</span><span class="sxs-lookup"><span data-stu-id="37027-111">Dialog1;Edit1</span></span> | <span data-ttu-id="37027-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="37027-112">Attributes</span></span> | <span data-ttu-id="37027-113">\[= Contraseña\]</span><span class="sxs-lookup"><span data-stu-id="37027-113">\[=Password\]</span></span>                |
| <span data-ttu-id="37027-114">Archivo</span><span class="sxs-lookup"><span data-stu-id="37027-114">File</span></span>    | <span data-ttu-id="37027-115">Archivo1</span><span class="sxs-lookup"><span data-stu-id="37027-115">File1</span></span>         | <span data-ttu-id="37027-116">Atributos</span><span class="sxs-lookup"><span data-stu-id="37027-116">Attributes</span></span> | <span data-ttu-id="37027-117">\[= Checksum \] \[ = comprimido\]</span><span class="sxs-lookup"><span data-stu-id="37027-117">\[=Checksum\]\[=Compressed\]</span></span> |



 

[<span data-ttu-id="37027-118">Tabla ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="37027-118">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md)



| <span data-ttu-id="37027-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="37027-119">Name</span></span>       | <span data-ttu-id="37027-120">Formato</span><span class="sxs-lookup"><span data-stu-id="37027-120">Format</span></span>   | <span data-ttu-id="37027-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="37027-121">Type</span></span> | <span data-ttu-id="37027-122">ContextData</span><span class="sxs-lookup"><span data-stu-id="37027-122">ContextData</span></span>                              | <span data-ttu-id="37027-123">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="37027-123">DefaultValue</span></span> | <span data-ttu-id="37027-124">Atributos</span><span class="sxs-lookup"><span data-stu-id="37027-124">Attributes</span></span> | <span data-ttu-id="37027-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="37027-125">DisplayName</span></span> | <span data-ttu-id="37027-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="37027-126">Description</span></span> |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| <span data-ttu-id="37027-127">Contraseña</span><span class="sxs-lookup"><span data-stu-id="37027-127">Password</span></span>   | <span data-ttu-id="37027-128">Bits</span><span class="sxs-lookup"><span data-stu-id="37027-128">Bitfield</span></span> |      | <span data-ttu-id="37027-129">2097152; True = 2097152; False = 0</span><span class="sxs-lookup"><span data-stu-id="37027-129">2097152;True=2097152;False=0</span></span>             | <span data-ttu-id="37027-130">0</span><span class="sxs-lookup"><span data-stu-id="37027-130">0</span></span>            | <span data-ttu-id="37027-131">0</span><span class="sxs-lookup"><span data-stu-id="37027-131">0</span></span>          |             |             |
| <span data-ttu-id="37027-132">Suma de comprobación</span><span class="sxs-lookup"><span data-stu-id="37027-132">Checksum</span></span>   | <span data-ttu-id="37027-133">Bits</span><span class="sxs-lookup"><span data-stu-id="37027-133">Bitfield</span></span> |      | <span data-ttu-id="37027-134">1024; Suma de comprobación = 1024; Sin suma de comprobación = 0</span><span class="sxs-lookup"><span data-stu-id="37027-134">1024;Checksum=1024;No Checksum=0</span></span>         | <span data-ttu-id="37027-135">0</span><span class="sxs-lookup"><span data-stu-id="37027-135">0</span></span>            | <span data-ttu-id="37027-136">0</span><span class="sxs-lookup"><span data-stu-id="37027-136">0</span></span>          |             |             |
| <span data-ttu-id="37027-137">Compressed</span><span class="sxs-lookup"><span data-stu-id="37027-137">Compressed</span></span> | <span data-ttu-id="37027-138">Bits</span><span class="sxs-lookup"><span data-stu-id="37027-138">Bitfield</span></span> |      | <span data-ttu-id="37027-139">24576; Compressed = 16384; Sin comprimir = 8192</span><span class="sxs-lookup"><span data-stu-id="37027-139">24576;Compressed=16384;Uncompressed=8192</span></span> | <span data-ttu-id="37027-140">8192</span><span class="sxs-lookup"><span data-stu-id="37027-140">8192</span></span>         | <span data-ttu-id="37027-141">0</span><span class="sxs-lookup"><span data-stu-id="37027-141">0</span></span>          |             |             |



 

 

 



