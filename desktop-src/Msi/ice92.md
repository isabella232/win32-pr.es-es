---
description: ICE92 comprueba que un componente sin un GUID de identificador de componente no se especifica también como un componente permanente.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910706"
---
# <a name="ice92"></a><span data-ttu-id="4b0f8-103">ICE92</span><span class="sxs-lookup"><span data-stu-id="4b0f8-103">ICE92</span></span>

<span data-ttu-id="4b0f8-104">ICE92 comprueba que un componente sin un GUID de identificador de componente no se especifica también como un componente permanente.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-104">ICE92 verifies that a component without a Component Id GUID is not also specified as a permanent component.</span></span> <span data-ttu-id="4b0f8-105">Esta acción personalizada de ICE comprueba la [tabla](component-table.md) de componentes en busca de componentes sin un [GUID](guid.md) especificado en el campo ComponentID y comprueba que la marca **msidbComponentAttributesPermanent** no se ha establecido en el campo atributos.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-105">This ICE custom action checks the [Component Table](component-table.md) for components without a [GUID](guid.md) specified in the ComponentId field and verifies that the **msidbComponentAttributesPermanent** flag has not been set in the Attributes field.</span></span> <span data-ttu-id="4b0f8-106">ICE92 también comprueba que ningún componente tiene los atributos **msidbComponentAttributesPermanent** y **msidbComponentAttributesUninstallOnSupersedence** .</span><span class="sxs-lookup"><span data-stu-id="4b0f8-106">ICE92 also verifies that no component has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes.</span></span>

<span data-ttu-id="4b0f8-107">Si la columna ComponentId es null, el instalador no registra el componente y el instalador no puede quitarlo ni repararlo.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-107">If the ComponentId column is null, the installer does not register the component and the component cannot be removed or repaired by the installer.</span></span>

## <a name="result"></a><span data-ttu-id="4b0f8-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="4b0f8-108">Result</span></span>

<span data-ttu-id="4b0f8-109">ICE92 expone el siguiente error.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-109">ICE92 posts the following error.</span></span>



| <span data-ttu-id="4b0f8-110">Error ICE92</span><span class="sxs-lookup"><span data-stu-id="4b0f8-110">ICE92 error</span></span>                                                          | <span data-ttu-id="4b0f8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b0f8-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b0f8-112">El componente ' \[ 1 \] ' no tiene ningún ComponentID y está marcado como permanente.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-112">The Component '\[1\]' has no ComponentId and is marked as permanent.</span></span> | <span data-ttu-id="4b0f8-113">La entrada de este componente en la tabla componente tiene el valor null en la columna ComponentId y tiene **msidbComponentAttributesPermanent** en la columna Attributes.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-113">The entry for this component in the Component table has null in the ComponentId column and has **msidbComponentAttributesPermanent** in the Attributes column.</span></span> |



 

<span data-ttu-id="4b0f8-114">ICE92 envía la siguiente advertencia.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-114">ICE92 posts the following warning.</span></span>



| <span data-ttu-id="4b0f8-115">ADVERTENCIA de ICE92</span><span class="sxs-lookup"><span data-stu-id="4b0f8-115">ICE92 warning</span></span>                                                                                                                                                           | <span data-ttu-id="4b0f8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b0f8-116">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b0f8-117">El componente ' \[ 1 \] ' está marcado como Permanent y Uninstall-on-subestado.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-117">The Component '\[1\]' is marked as permanent and uninstall-on-supersedence.</span></span> <span data-ttu-id="4b0f8-118">Se omitirá el atributo Uninstall-on-sustitución porque el componente es permanente.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-118">The uninstall-on-supersedence attribute will be ignored because the component is permanent.</span></span> | <span data-ttu-id="4b0f8-119">La entrada de este componente en la [tabla de componentes](component-table.md) tiene los atributos **msidbComponentAttributesPermanent** y **msidbComponentAttributesUninstallOnSupersedence** especificados.</span><span class="sxs-lookup"><span data-stu-id="4b0f8-119">The entry for this component in the [Component table](component-table.md) has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes specified.</span></span> |



 

## <a name="example"></a><span data-ttu-id="4b0f8-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4b0f8-120">Example</span></span>

<span data-ttu-id="4b0f8-121">ICE92 notifica el siguiente error para el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4b0f8-121">ICE92 reports the following error for the example:</span></span>

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

<span data-ttu-id="4b0f8-122">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="4b0f8-122">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="4b0f8-123">Componente</span><span class="sxs-lookup"><span data-stu-id="4b0f8-123">Component</span></span>  | <span data-ttu-id="4b0f8-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="4b0f8-124">ComponentId</span></span> | <span data-ttu-id="4b0f8-125">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="4b0f8-125">Directory\_</span></span> | <span data-ttu-id="4b0f8-126">Atributos</span><span class="sxs-lookup"><span data-stu-id="4b0f8-126">Attributes</span></span> | <span data-ttu-id="4b0f8-127">Rutas</span><span class="sxs-lookup"><span data-stu-id="4b0f8-127">KeyPath</span></span> |
|------------|-------------|-------------|------------|---------|
| <span data-ttu-id="4b0f8-128">Component1</span><span class="sxs-lookup"><span data-stu-id="4b0f8-128">Component1</span></span> |             | <span data-ttu-id="4b0f8-129">Directorioa</span><span class="sxs-lookup"><span data-stu-id="4b0f8-129">DirectoryA</span></span>  | <span data-ttu-id="4b0f8-130">16</span><span class="sxs-lookup"><span data-stu-id="4b0f8-130">16</span></span>         | <span data-ttu-id="4b0f8-131">Archivoa</span><span class="sxs-lookup"><span data-stu-id="4b0f8-131">FileA</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="4b0f8-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b0f8-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b0f8-133">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="4b0f8-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



