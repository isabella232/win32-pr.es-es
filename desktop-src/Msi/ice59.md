---
description: ICE59 comprueba que los accesos directos anunciados pertenecen a los componentes que se instalan con la característica de destino del acceso directo.
ms.assetid: 9cd19137-792d-4fde-92d2-7d96942448d6
title: ICE59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5631b723a158bb371fff3211654a70d694b6cb5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652589"
---
# <a name="ice59"></a><span data-ttu-id="7bbb7-103">ICE59</span><span class="sxs-lookup"><span data-stu-id="7bbb7-103">ICE59</span></span>

<span data-ttu-id="7bbb7-104">ICE59 comprueba que los accesos directos anunciados pertenecen a los componentes que se instalan con la característica de destino del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="7bbb7-104">ICE59 checks that advertised shortcuts belong to components that are installed by the target feature of the shortcut.</span></span>

<span data-ttu-id="7bbb7-105">Los errores informados por ICE59 generalmente conducen al comportamiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="7bbb7-105">Errors reported by ICE59 generally lead to the following behavior:</span></span>

1.  <span data-ttu-id="7bbb7-106">El acceso directo anunciado iniciará el Windows Installer para instalar la característica que se muestra en la columna destino.</span><span class="sxs-lookup"><span data-stu-id="7bbb7-106">The advertised shortcut will launch the Windows Installer to install the feature listed in the Target column.</span></span>
2.  <span data-ttu-id="7bbb7-107">Pero como la [tabla FeatureComponents](featurecomponents-table.md) no asigna la característica de destino al componente que contiene el acceso directo, el keyfile del componente (que se activa mediante el acceso directo) no está instalado.</span><span class="sxs-lookup"><span data-stu-id="7bbb7-107">But because the [FeatureComponents table](featurecomponents-table.md) does not map the target feature to the component containing the shortcut, the keyfile of the component (which is activated by the shortcut) is not installed.</span></span>
3.  <span data-ttu-id="7bbb7-108">Por lo tanto, el acceso directo se rompe y no hará nada.</span><span class="sxs-lookup"><span data-stu-id="7bbb7-108">Therefore the shortcut is broken and will not do anything.</span></span>

## <a name="result"></a><span data-ttu-id="7bbb7-109">Resultado</span><span class="sxs-lookup"><span data-stu-id="7bbb7-109">Result</span></span>

<span data-ttu-id="7bbb7-110">ICE59 publica un error si un acceso directo anunciado no pertenece a los componentes que se instalan con la característica de destino del acceso directo.</span><span class="sxs-lookup"><span data-stu-id="7bbb7-110">ICE59 posts an error if an advertised shortcut does not belong to the components that are installed by the target feature of the shortcut.</span></span>

## <a name="example"></a><span data-ttu-id="7bbb7-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7bbb7-111">Example</span></span>

<span data-ttu-id="7bbb7-112">ICE59 notifica el siguiente error para el ejemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="7bbb7-112">ICE59 reports the following error for the example shown:</span></span>

``` syntax
The shortcut ShortcutB activates component ComponentB and advertises feature FeatureA, but there is no mapping between FeatureA and ComponentB in the FeatureComponents table.
```

<span data-ttu-id="7bbb7-113">En este caso, ShortcutB anuncia Featurea y, cuando se activa, inicia el archivo de clave de ComponentB.</span><span class="sxs-lookup"><span data-stu-id="7bbb7-113">In this case, ShortcutB advertises FeatureA, and when activated, starts the key file of ComponentB.</span></span> <span data-ttu-id="7bbb7-114">Además, ComponentB nunca se instala con Featurea, por lo que, incluso después de que se complete la fase de instalación a petición, el destino del acceso directo no existe.</span><span class="sxs-lookup"><span data-stu-id="7bbb7-114">Yet ComponentB is never installed by FeatureA, so even after the installation-on-demand phase completes, the target of the shortcut does not exist.</span></span>

<span data-ttu-id="7bbb7-115">Para corregir este error, agregue una fila a la [tabla FeatureComponents](featurecomponents-table.md) que asocia featurea y ComponentB.</span><span class="sxs-lookup"><span data-stu-id="7bbb7-115">To fix this error, add a row to the [FeatureComponents table](featurecomponents-table.md) that associates FeatureA and ComponentB.</span></span>

<span data-ttu-id="7bbb7-116">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="7bbb7-116">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="7bbb7-117">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="7bbb7-117">Shortcut</span></span>  | <span data-ttu-id="7bbb7-118">Destino</span><span class="sxs-lookup"><span data-stu-id="7bbb7-118">Target</span></span>   | <span data-ttu-id="7bbb7-119">Componente\_</span><span class="sxs-lookup"><span data-stu-id="7bbb7-119">Component\_</span></span> |
|-----------|----------|-------------|
| <span data-ttu-id="7bbb7-120">ShortcutB</span><span class="sxs-lookup"><span data-stu-id="7bbb7-120">ShortcutB</span></span> | <span data-ttu-id="7bbb7-121">FeatureA</span><span class="sxs-lookup"><span data-stu-id="7bbb7-121">FeatureA</span></span> | <span data-ttu-id="7bbb7-122">ComponentB</span><span class="sxs-lookup"><span data-stu-id="7bbb7-122">ComponentB</span></span>  |



 

[<span data-ttu-id="7bbb7-123">Tabla FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="7bbb7-123">FeatureComponents Table</span></span>](featurecomponents-table.md)



| <span data-ttu-id="7bbb7-124">Característica\_</span><span class="sxs-lookup"><span data-stu-id="7bbb7-124">Feature\_</span></span> | <span data-ttu-id="7bbb7-125">Componente\_</span><span class="sxs-lookup"><span data-stu-id="7bbb7-125">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="7bbb7-126">FeatureA</span><span class="sxs-lookup"><span data-stu-id="7bbb7-126">FeatureA</span></span>  | <span data-ttu-id="7bbb7-127">Componentea</span><span class="sxs-lookup"><span data-stu-id="7bbb7-127">ComponentA</span></span>  |



 

<span data-ttu-id="7bbb7-128">[Tabla de características](feature-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="7bbb7-128">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="7bbb7-129">Característica</span><span class="sxs-lookup"><span data-stu-id="7bbb7-129">Feature</span></span>  | <span data-ttu-id="7bbb7-130">Nivel</span><span class="sxs-lookup"><span data-stu-id="7bbb7-130">Level</span></span> |
|----------|-------|
| <span data-ttu-id="7bbb7-131">FeatureA</span><span class="sxs-lookup"><span data-stu-id="7bbb7-131">FeatureA</span></span> | <span data-ttu-id="7bbb7-132">10</span><span class="sxs-lookup"><span data-stu-id="7bbb7-132">10</span></span>    |



 

<span data-ttu-id="7bbb7-133">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="7bbb7-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="7bbb7-134">Componente</span><span class="sxs-lookup"><span data-stu-id="7bbb7-134">Component</span></span>  | <span data-ttu-id="7bbb7-135">Rutas</span><span class="sxs-lookup"><span data-stu-id="7bbb7-135">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="7bbb7-136">Componentea</span><span class="sxs-lookup"><span data-stu-id="7bbb7-136">ComponentA</span></span> | <span data-ttu-id="7bbb7-137">Archivoa</span><span class="sxs-lookup"><span data-stu-id="7bbb7-137">FileA</span></span>   |
| <span data-ttu-id="7bbb7-138">ComponentB</span><span class="sxs-lookup"><span data-stu-id="7bbb7-138">ComponentB</span></span> | <span data-ttu-id="7bbb7-139">FileB</span><span class="sxs-lookup"><span data-stu-id="7bbb7-139">FileB</span></span>   |



 

<span data-ttu-id="7bbb7-140">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="7bbb7-140">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="7bbb7-141">Archivo</span><span class="sxs-lookup"><span data-stu-id="7bbb7-141">File</span></span>  | <span data-ttu-id="7bbb7-142">Componente\_</span><span class="sxs-lookup"><span data-stu-id="7bbb7-142">Component\_</span></span> | <span data-ttu-id="7bbb7-143">Secuencia</span><span class="sxs-lookup"><span data-stu-id="7bbb7-143">Sequence</span></span> |
|-------|-------------|----------|
| <span data-ttu-id="7bbb7-144">Archivoa</span><span class="sxs-lookup"><span data-stu-id="7bbb7-144">FileA</span></span> | <span data-ttu-id="7bbb7-145">Componentea</span><span class="sxs-lookup"><span data-stu-id="7bbb7-145">ComponentA</span></span>  | <span data-ttu-id="7bbb7-146">1</span><span class="sxs-lookup"><span data-stu-id="7bbb7-146">1</span></span>        |
| <span data-ttu-id="7bbb7-147">FileB</span><span class="sxs-lookup"><span data-stu-id="7bbb7-147">FileB</span></span> | <span data-ttu-id="7bbb7-148">ComponentB</span><span class="sxs-lookup"><span data-stu-id="7bbb7-148">ComponentB</span></span>  | <span data-ttu-id="7bbb7-149">2</span><span class="sxs-lookup"><span data-stu-id="7bbb7-149">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="7bbb7-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bbb7-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bbb7-151">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="7bbb7-151">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



