---
description: ICE67 comprueba que el destino de un acceso directo no anunciado pertenece al mismo componente que el propio acceso directo o que los atributos del componente de destino garantizan que no cambie las ubicaciones de instalación.
ms.assetid: 3fc462e7-4c11-4167-a157-6c1e0791901d
title: ICE67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca140a2d7eace9b693e82763f6bf5824346b51e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002698"
---
# <a name="ice67"></a><span data-ttu-id="5412e-103">ICE67</span><span class="sxs-lookup"><span data-stu-id="5412e-103">ICE67</span></span>

<span data-ttu-id="5412e-104">ICE67 comprueba que el destino de un acceso directo no anunciado pertenece al mismo componente que el propio acceso directo o que los atributos del componente de destino garantizan que no cambie las ubicaciones de instalación.</span><span class="sxs-lookup"><span data-stu-id="5412e-104">ICE67 checks that the target of a non-advertised shortcut belongs to the same component as the shortcut itself, or that the attributes of the target component ensure that it does not change installation locations.</span></span>

<span data-ttu-id="5412e-105">Un error al corregir una advertencia o un error informados por ICE67 puede hacer que el acceso directo no sea válido si el componente de destino cambia de estado y el componente de origen no lo hace.</span><span class="sxs-lookup"><span data-stu-id="5412e-105">Failure to fix a warning or error reported by ICE67 can cause the shortcut to be invalid if the target component changes state and the source component does not.</span></span> <span data-ttu-id="5412e-106">Por ejemplo, cuando el componente del archivo de destino se establece en ejecutar desde el origen, una reinstalación que cambia el componente a resultados locales en el componente que contiene el acceso directo no se vuelve a instalar.</span><span class="sxs-lookup"><span data-stu-id="5412e-106">For example, when the target file's component is set to run from source, a reinstallation that changes the component to local results in the component containing the shortcut not being reinstalled.</span></span> <span data-ttu-id="5412e-107">Por lo tanto, el acceso directo apunta a una ubicación no válida.</span><span class="sxs-lookup"><span data-stu-id="5412e-107">Thus the shortcut points to an invalid location.</span></span>

<span data-ttu-id="5412e-108">Tenga en cuenta que en algunos casos, el uso de un componente diferente para el acceso directo es inevitable.</span><span class="sxs-lookup"><span data-stu-id="5412e-108">Note that in some cases, using a different component for the shortcut is unavoidable.</span></span> <span data-ttu-id="5412e-109">Por ejemplo, si se crea el acceso directo en el perfil de usuario y el archivo se instala en un directorio que no es de perfil, es posible que no pueda usar el mismo componente para ambos fragmentos de datos.</span><span class="sxs-lookup"><span data-stu-id="5412e-109">For example, if the shortcut is created in the user profile and the file is installed to a non-profile directory, you may not be able to use the same component for both pieces of data.</span></span> <span data-ttu-id="5412e-110">(Esto provoca errores en escenarios de varios usuarios, como los descritos en [ICE57](ice57.md)).</span><span class="sxs-lookup"><span data-stu-id="5412e-110">(This results in failures in multi-user scenarios – such as those described in [ICE57](ice57.md)).</span></span> <span data-ttu-id="5412e-111">En este caso, es posible que pueda usar accesos directos anunciados para lograr el comportamiento que desea, o simplemente puede asegurarse de que el componente de destino no puede cambiar de ejecutar desde el origen a local.</span><span class="sxs-lookup"><span data-stu-id="5412e-111">In this case, you may be able to use advertised shortcuts to achieve the behavior you want, or you can simply ensure that the target component cannot change from run-from-source to local.</span></span>

## <a name="result"></a><span data-ttu-id="5412e-112">Resultado</span><span class="sxs-lookup"><span data-stu-id="5412e-112">Result</span></span>

<span data-ttu-id="5412e-113">ICE67 devuelve un error o una advertencia si el destino de un acceso directo no anunciado no pertenece al mismo componente que el propio método abreviado, o si los atributos del componente de destino no se aseguran de que las ubicaciones de instalación no cambien.</span><span class="sxs-lookup"><span data-stu-id="5412e-113">ICE67 returns an error or a warning if the target of a non-advertised shortcut does not belong to the same component as the shortcut itself, or if the attributes of the target component do not ensure that the installation locations will not change.</span></span>

## <a name="example"></a><span data-ttu-id="5412e-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5412e-114">Example</span></span>

<span data-ttu-id="5412e-115">ICE67 notifica los siguientes errores y advertencias para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="5412e-115">ICE67 reports the following warning and errors for the example shown.</span></span>

``` syntax
The shortcut 'Shortcut1' is a non-advertised shortcut with a file target. The shortcut and target are installed by different components, and the target component can run locally or from source.
```

<span data-ttu-id="5412e-116">Shortcut1 instala Component2, pero Component1 instala su archivo de destino, archivo1.</span><span class="sxs-lookup"><span data-stu-id="5412e-116">Shortcut1 is installed by Component2, but its target file, File1, is installed by component1.</span></span> <span data-ttu-id="5412e-117">El componente de destino está marcado como opcional (lo que significa que puede ser local o ejecutar desde el origen).</span><span class="sxs-lookup"><span data-stu-id="5412e-117">The target component is marked optional (meaning that it can be local or run-from-source).</span></span> <span data-ttu-id="5412e-118">Una posible situación que podría provocar un problema es que Component1 cambie de ejecutar desde el origen a local.</span><span class="sxs-lookup"><span data-stu-id="5412e-118">One possible situation that would cause a problem is if Component1 changes from run-from-source to local.</span></span> <span data-ttu-id="5412e-119">Esto haría que Shortcut1 apuntara a una ubicación no válida.</span><span class="sxs-lookup"><span data-stu-id="5412e-119">This would cause Shortcut1 to point to an invalid location.</span></span>

<span data-ttu-id="5412e-120">Para corregir esta advertencia, instale el acceso directo como parte de Component1 o marque Component1 como LocalOnly o SourceOnly.</span><span class="sxs-lookup"><span data-stu-id="5412e-120">To fix this warning, Install the shortcut as part of Component1, or mark Component1 as LocalOnly or SourceOnly.</span></span>

<span data-ttu-id="5412e-121">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="5412e-121">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="5412e-122">Archivo</span><span class="sxs-lookup"><span data-stu-id="5412e-122">File</span></span>  | <span data-ttu-id="5412e-123">Componente\_</span><span class="sxs-lookup"><span data-stu-id="5412e-123">Component\_</span></span> |
|-------|-------------|
| <span data-ttu-id="5412e-124">Archivo1</span><span class="sxs-lookup"><span data-stu-id="5412e-124">File1</span></span> | <span data-ttu-id="5412e-125">Component1</span><span class="sxs-lookup"><span data-stu-id="5412e-125">Component1</span></span>  |



 

<span data-ttu-id="5412e-126">[Tabla de acceso directo](shortcut-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="5412e-126">[Shortcut Table](shortcut-table.md) (partial)</span></span>



| <span data-ttu-id="5412e-127">Acceso directo</span><span class="sxs-lookup"><span data-stu-id="5412e-127">Shortcut</span></span>  | <span data-ttu-id="5412e-128">Componente\_</span><span class="sxs-lookup"><span data-stu-id="5412e-128">Component\_</span></span> | <span data-ttu-id="5412e-129">Destino</span><span class="sxs-lookup"><span data-stu-id="5412e-129">Target</span></span>      |
|-----------|-------------|-------------|
| <span data-ttu-id="5412e-130">Shortcut1</span><span class="sxs-lookup"><span data-stu-id="5412e-130">Shortcut1</span></span> | <span data-ttu-id="5412e-131">Component2</span><span class="sxs-lookup"><span data-stu-id="5412e-131">Component2</span></span>  | <span data-ttu-id="5412e-132">\[\#Archivo1\]</span><span class="sxs-lookup"><span data-stu-id="5412e-132">\[\#File1\]</span></span> |



 

<span data-ttu-id="5412e-133">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="5412e-133">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="5412e-134">Componente</span><span class="sxs-lookup"><span data-stu-id="5412e-134">Component</span></span>  | <span data-ttu-id="5412e-135">Atributos</span><span class="sxs-lookup"><span data-stu-id="5412e-135">Attributes</span></span> |
|------------|------------|
| <span data-ttu-id="5412e-136">Component1</span><span class="sxs-lookup"><span data-stu-id="5412e-136">Component1</span></span> | <span data-ttu-id="5412e-137">2</span><span class="sxs-lookup"><span data-stu-id="5412e-137">2</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="5412e-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5412e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5412e-139">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="5412e-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



