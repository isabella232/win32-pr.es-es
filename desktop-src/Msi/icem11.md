---
description: ICEM11 comprueba que un módulo de combinación configurable muestra la tabla ModuleConfiguration y la tabla ModuleSubstitution en la tabla ModuleIgnoreTable del módulo.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277746"
---
# <a name="icem11"></a><span data-ttu-id="29cb6-103">ICEM11</span><span class="sxs-lookup"><span data-stu-id="29cb6-103">ICEM11</span></span>

<span data-ttu-id="29cb6-104">ICEM11 comprueba que un módulo de combinación configurable muestra la tabla [ModuleConfiguration](moduleconfiguration-table.md) y la [tabla ModuleSubstitution](modulesubstitution-table.md) en la [tabla ModuleIgnoreTable](moduleignoretable-table.md) del módulo.</span><span class="sxs-lookup"><span data-stu-id="29cb6-104">ICEM11 verifies that a Configurable Merge Module lists the [ModuleConfiguration table](moduleconfiguration-table.md) and [ModuleSubstitution table](modulesubstitution-table.md) in the [ModuleIgnoreTable table](moduleignoretable-table.md) of the module.</span></span> <span data-ttu-id="29cb6-105">Esto garantiza que las herramientas de combinación que no reconocen los módulos de combinación configurables (menos de la versión 2,0) no copian estas tablas en la base de datos de destino.</span><span class="sxs-lookup"><span data-stu-id="29cb6-105">This ensures that merge tools that do not recognize configurable merge modules(less than version 2.0) do not copy these tables into the target database.</span></span>

<span data-ttu-id="29cb6-106">Este ICEM está disponible en el archivo Mergemod. Cub proporcionado en el SDK de Windows Installer 2,0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="29cb6-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="29cb6-107">Para obtener más información, consulte [componentes de Windows SDK para desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="29cb6-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="29cb6-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="29cb6-108">Result</span></span>

<span data-ttu-id="29cb6-109">ICEM11 publica un error si el módulo contiene una tabla ModuleConfiguration o ModuleSubstitution que no aparece en la tabla ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="29cb6-109">ICEM11 posts an error if the module contains a ModuleConfiguration or ModuleSubstitution table not listed in the ModuleIgnoreTable table.</span></span>

## <a name="example"></a><span data-ttu-id="29cb6-110">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="29cb6-110">Example</span></span>

<span data-ttu-id="29cb6-111">ICEM11 expone los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.</span><span class="sxs-lookup"><span data-stu-id="29cb6-111">ICEM11 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

<span data-ttu-id="29cb6-112">[ModuleConfiguration](moduleconfiguration-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="29cb6-112">[ModuleConfiguration](moduleconfiguration-table.md) (partial)</span></span>



| <span data-ttu-id="29cb6-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="29cb6-113">Name</span></span>     | <span data-ttu-id="29cb6-114">Formato</span><span class="sxs-lookup"><span data-stu-id="29cb6-114">Format</span></span> | <span data-ttu-id="29cb6-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="29cb6-115">Type</span></span>   | <span data-ttu-id="29cb6-116">ContextData</span><span class="sxs-lookup"><span data-stu-id="29cb6-116">ContextData</span></span> | <span data-ttu-id="29cb6-117">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="29cb6-117">DefaultValue</span></span> |
|----------|--------|--------|-------------|--------------|
| <span data-ttu-id="29cb6-118">IconKey1</span><span class="sxs-lookup"><span data-stu-id="29cb6-118">IconKey1</span></span> | <span data-ttu-id="29cb6-119">1</span><span class="sxs-lookup"><span data-stu-id="29cb6-119">1</span></span>      | <span data-ttu-id="29cb6-120">Binary</span><span class="sxs-lookup"><span data-stu-id="29cb6-120">Binary</span></span> | <span data-ttu-id="29cb6-121">Icono</span><span class="sxs-lookup"><span data-stu-id="29cb6-121">Icon</span></span>        | <span data-ttu-id="29cb6-122">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="29cb6-122">DefaultIcon</span></span>  |



 

[<span data-ttu-id="29cb6-123">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="29cb6-123">ModuleSubstitution</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="29cb6-124">Tabla</span><span class="sxs-lookup"><span data-stu-id="29cb6-124">Table</span></span>   | <span data-ttu-id="29cb6-125">Row</span><span class="sxs-lookup"><span data-stu-id="29cb6-125">Row</span></span>              | <span data-ttu-id="29cb6-126">Columna</span><span class="sxs-lookup"><span data-stu-id="29cb6-126">Column</span></span> | <span data-ttu-id="29cb6-127">Valor</span><span class="sxs-lookup"><span data-stu-id="29cb6-127">Value</span></span>        |
|---------|------------------|--------|--------------|
| <span data-ttu-id="29cb6-128">Control</span><span class="sxs-lookup"><span data-stu-id="29cb6-128">Control</span></span> | <span data-ttu-id="29cb6-129">Dialog1; Control1</span><span class="sxs-lookup"><span data-stu-id="29cb6-129">Dialog1;Control1</span></span> | <span data-ttu-id="29cb6-130">Texto</span><span class="sxs-lookup"><span data-stu-id="29cb6-130">Text</span></span>   | <span data-ttu-id="29cb6-131">\[IconKey1\]</span><span class="sxs-lookup"><span data-stu-id="29cb6-131">\[IconKey1\]</span></span> |



 

[<span data-ttu-id="29cb6-132">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="29cb6-132">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)



| <span data-ttu-id="29cb6-133">Tabla</span><span class="sxs-lookup"><span data-stu-id="29cb6-133">Table</span></span>               |
|---------------------|
| <span data-ttu-id="29cb6-134">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="29cb6-134">ModuleConfiguration</span></span> |



 

<span data-ttu-id="29cb6-135">Para corregir este error, incluya las tablas ModuleSubstitution y ModuleConfiguration en la tabla ModuleIgnoreTable.</span><span class="sxs-lookup"><span data-stu-id="29cb6-135">To fix this error include both the ModuleSubstitution and ModuleConfiguration tables in the ModuleIgnoreTable table.</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="29cb6-136">Tabla utilizada durante la ejecución</span><span class="sxs-lookup"><span data-stu-id="29cb6-136">Table Used During Execution</span></span>

[<span data-ttu-id="29cb6-137">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="29cb6-137">ModuleSubstitution</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="29cb6-138">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="29cb6-138">ModuleConfiguration</span></span>](moduleconfiguration-table.md)

[<span data-ttu-id="29cb6-139">ModuleIgnoreTable</span><span class="sxs-lookup"><span data-stu-id="29cb6-139">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)

## <a name="related-topics"></a><span data-ttu-id="29cb6-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29cb6-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29cb6-141">Referencia de módulo de combinación ICE</span><span class="sxs-lookup"><span data-stu-id="29cb6-141">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



