---
description: ICE94 comprueba la tabla de acceso directo, la tabla de características y la tabla MsiAssembly y publica una advertencia si hay accesos directos no anunciados que señalan a un archivo de ensamblado en la caché global de ensamblados.
ms.assetid: 9b1b25b5-b190-47c2-8d43-fa3964e87a6f
title: ICE94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ce52e88a31e246eb4d69defba77b64c2955eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278457"
---
# <a name="ice94"></a><span data-ttu-id="01a4a-103">ICE94</span><span class="sxs-lookup"><span data-stu-id="01a4a-103">ICE94</span></span>

<span data-ttu-id="01a4a-104">ICE94 comprueba la tabla de [acceso directo](shortcut-table.md), la [tabla de características](feature-table.md)y la [tabla MsiAssembly](msiassembly-table.md) y publica una advertencia si hay accesos directos no anunciados que señalan a un archivo de ensamblado en la caché global de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="01a4a-104">ICE94 checks the [Shortcut table](shortcut-table.md), [Feature table](feature-table.md), and [MsiAssembly table](msiassembly-table.md) and posts a warning if there are any unadvertised shortcuts pointing to an assembly file in the global assembly cache.</span></span> <span data-ttu-id="01a4a-105">Si la entrada en el campo de destino de la tabla de acceso directo no es una característica de la tabla de características, el acceso directo no se anuncia.</span><span class="sxs-lookup"><span data-stu-id="01a4a-105">If the entry in the Target field of the Shortcut table is not a feature in the Feature table, the shortcut is unadvertised.</span></span> <span data-ttu-id="01a4a-106">Si la entrada en el \_ campo componente de la tabla de acceso directo también aparece en la tabla MsiAssembly, el acceso directo apunta a un archivo de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="01a4a-106">If the entry in the Component\_ field of the Shortcut table is also listed in the MsiAssembly table, the shortcut points to an assembly file.</span></span> <span data-ttu-id="01a4a-107">Si la entrada del campo de la \_ aplicación de archivo en la tabla MsiAssembly está vacía, el archivo de ensamblado se encuentra en la caché global de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="01a4a-107">If the entry in the File\_Application field in the MsiAssembly table is empty, the assembly file is in the global assembly cache.</span></span>

## <a name="result"></a><span data-ttu-id="01a4a-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="01a4a-108">Result</span></span>

<span data-ttu-id="01a4a-109">ICE94 envía la siguiente advertencia.</span><span class="sxs-lookup"><span data-stu-id="01a4a-109">ICE94 posts the following warning.</span></span>



| <span data-ttu-id="01a4a-110">ADVERTENCIA de ICE94</span><span class="sxs-lookup"><span data-stu-id="01a4a-110">ICE94 warning</span></span>                                                                                | <span data-ttu-id="01a4a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="01a4a-111">Description</span></span>                                                                            |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="01a4a-112">El acceso directo no anunciado ' \[ 2 \] ' apunta a un archivo de ensamblado en la caché global de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="01a4a-112">The non-advertised shortcut '\[2\]' points to an assembly file in the global assembly cache.</span></span> | <span data-ttu-id="01a4a-113">Un acceso directo no anunciado apunta a un archivo de ensamblado en la caché global de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="01a4a-113">An unadvertised shortcut is pointing to an assembly file in the global assembly cache.</span></span> |



 

## <a name="example"></a><span data-ttu-id="01a4a-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01a4a-114">Example</span></span>

<span data-ttu-id="01a4a-115">ICE94 notifica el siguiente error para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="01a4a-115">ICE94 reports the following error for the example:</span></span>

``` syntax
The non-advertised shortcut 'shortcut1' points to an assembly file in the global assembly cache.
```

<span data-ttu-id="01a4a-116">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="01a4a-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="01a4a-117">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="01a4a-117">Shortcut</span></span>  | <span data-ttu-id="01a4a-118">Componente\_</span><span class="sxs-lookup"><span data-stu-id="01a4a-118">Component\_</span></span> | <span data-ttu-id="01a4a-119">Destino</span><span class="sxs-lookup"><span data-stu-id="01a4a-119">Target</span></span>    |
|-----------|-------------|-----------|
| <span data-ttu-id="01a4a-120">shortcut1</span><span class="sxs-lookup"><span data-stu-id="01a4a-120">shortcut1</span></span> | <span data-ttu-id="01a4a-121">c1</span><span class="sxs-lookup"><span data-stu-id="01a4a-121">c1</span></span>          | <span data-ttu-id="01a4a-122">\[archivo1\]</span><span class="sxs-lookup"><span data-stu-id="01a4a-122">\[file1\]</span></span> |
| <span data-ttu-id="01a4a-123">shortcut2</span><span class="sxs-lookup"><span data-stu-id="01a4a-123">shortcut2</span></span> | <span data-ttu-id="01a4a-124">c2</span><span class="sxs-lookup"><span data-stu-id="01a4a-124">c2</span></span>          | <span data-ttu-id="01a4a-125">Feature1</span><span class="sxs-lookup"><span data-stu-id="01a4a-125">feature1</span></span>  |
| <span data-ttu-id="01a4a-126">shortcut3</span><span class="sxs-lookup"><span data-stu-id="01a4a-126">shortcut3</span></span> | <span data-ttu-id="01a4a-127">c3</span><span class="sxs-lookup"><span data-stu-id="01a4a-127">c3</span></span>          | <span data-ttu-id="01a4a-128">\[archivo2\]</span><span class="sxs-lookup"><span data-stu-id="01a4a-128">\[file2\]</span></span> |



 

<span data-ttu-id="01a4a-129">[Tabla de características](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="01a4a-129">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="01a4a-130">Característica</span><span class="sxs-lookup"><span data-stu-id="01a4a-130">Feature</span></span>  |
|----------|
| <span data-ttu-id="01a4a-131">Feature1</span><span class="sxs-lookup"><span data-stu-id="01a4a-131">feature1</span></span> |



 

<span data-ttu-id="01a4a-132">[Tabla MsiAssembly](msiassembly-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="01a4a-132">[MsiAssembly Table](msiassembly-table.md) (partial)</span></span>



| <span data-ttu-id="01a4a-133">Componente\_</span><span class="sxs-lookup"><span data-stu-id="01a4a-133">Component\_</span></span> | <span data-ttu-id="01a4a-134">Aplicación de archivo \_</span><span class="sxs-lookup"><span data-stu-id="01a4a-134">File\_Application</span></span> |
|-------------|-------------------|
| <span data-ttu-id="01a4a-135">c1</span><span class="sxs-lookup"><span data-stu-id="01a4a-135">c1</span></span>          |                   |
| <span data-ttu-id="01a4a-136">c2</span><span class="sxs-lookup"><span data-stu-id="01a4a-136">c2</span></span>          |                   |
| <span data-ttu-id="01a4a-137">c3</span><span class="sxs-lookup"><span data-stu-id="01a4a-137">c3</span></span>          | <span data-ttu-id="01a4a-138">fa1</span><span class="sxs-lookup"><span data-stu-id="01a4a-138">fa1</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="01a4a-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01a4a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01a4a-140">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="01a4a-140">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



