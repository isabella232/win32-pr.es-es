---
description: Cada registro de la tabla IsolatedComponent asocia el componente especificado en la columna de aplicación de componentes \_ (normalmente, un archivo. exe) con el componente especificado en la \_ columna compartida componente (normalmente es una DLL compartida).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Tabla IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686809"
---
# <a name="isolatedcomponent-table"></a><span data-ttu-id="b5c0c-103">Tabla IsolatedComponent</span><span class="sxs-lookup"><span data-stu-id="b5c0c-103">IsolatedComponent Table</span></span>

<span data-ttu-id="b5c0c-104">Cada registro de la tabla IsolatedComponent asocia el componente especificado en la columna de aplicación de componentes \_ (normalmente, un archivo. exe) con el componente especificado en la \_ columna compartida componente (normalmente es una DLL compartida).</span><span class="sxs-lookup"><span data-stu-id="b5c0c-104">Each record of the IsolatedComponent table associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span> <span data-ttu-id="b5c0c-105">La [acción IsolateComponents](isolatecomponents-action.md) instala una copia del componente \_ compartido en una ubicación privada para su uso por parte de la aplicación de componentes \_ .</span><span class="sxs-lookup"><span data-stu-id="b5c0c-105">The [IsolateComponents action](isolatecomponents-action.md) installs a copy of Component\_Shared into a private location for use by Component\_Application.</span></span> <span data-ttu-id="b5c0c-106">Esto aísla la \_ aplicación de componentes de otras copias del componente \_ compartido que se puede instalar en una ubicación compartida del equipo.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-106">This isolates the Component\_Application from other copies of Component\_Shared that may be installed to a shared location on the computer.</span></span> <span data-ttu-id="b5c0c-107">Vea [componentes aislados](isolated-components.md).</span><span class="sxs-lookup"><span data-stu-id="b5c0c-107">See [Isolated Components](isolated-components.md).</span></span>

<span data-ttu-id="b5c0c-108">Para vincular un componente \_ compartido a una aplicación de varios componentes \_ , incluya un registro independiente para cada par en la tabla IsolatedComponents.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-108">To link one Component\_Shared to multiple Component\_Application, include a separate record for each pair in the IsolatedComponents table.</span></span> <span data-ttu-id="b5c0c-109">El instalador copia los archivos del componente \_ compartido en el directorio de cada aplicación de componente \_ que está instalada.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-109">The installer copies the files of Component\_Shared into the directory of each Component\_Application that is installed.</span></span>

<span data-ttu-id="b5c0c-110">La tabla IsolatedComponent tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-110">The IsolatedComponent table has the following columns.</span></span>



| <span data-ttu-id="b5c0c-111">Columna</span><span class="sxs-lookup"><span data-stu-id="b5c0c-111">Column</span></span>                 | <span data-ttu-id="b5c0c-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5c0c-112">Type</span></span>                         | <span data-ttu-id="b5c0c-113">Clave</span><span class="sxs-lookup"><span data-stu-id="b5c0c-113">Key</span></span> | <span data-ttu-id="b5c0c-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="b5c0c-114">Nullable</span></span> |
|------------------------|------------------------------|-----|----------|
| <span data-ttu-id="b5c0c-115">Componente \_ compartido</span><span class="sxs-lookup"><span data-stu-id="b5c0c-115">Component\_Shared</span></span>      | [<span data-ttu-id="b5c0c-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="b5c0c-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="b5c0c-117">Y</span><span class="sxs-lookup"><span data-stu-id="b5c0c-117">Y</span></span>   | <span data-ttu-id="b5c0c-118">N</span><span class="sxs-lookup"><span data-stu-id="b5c0c-118">N</span></span>        |
| <span data-ttu-id="b5c0c-119">Aplicación de componentes \_</span><span class="sxs-lookup"><span data-stu-id="b5c0c-119">Component\_Application</span></span> | [<span data-ttu-id="b5c0c-120">Identificador</span><span class="sxs-lookup"><span data-stu-id="b5c0c-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="b5c0c-121">Y</span><span class="sxs-lookup"><span data-stu-id="b5c0c-121">Y</span></span>   | <span data-ttu-id="b5c0c-122">N</span><span class="sxs-lookup"><span data-stu-id="b5c0c-122">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="b5c0c-123">Columnas</span><span class="sxs-lookup"><span data-stu-id="b5c0c-123">Columns</span></span>

<dl> <dt>

<span data-ttu-id="b5c0c-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Componente \_ compartido</span><span class="sxs-lookup"><span data-stu-id="b5c0c-124"><span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Component\_Shared</span></span>
</dt> <dd>

<span data-ttu-id="b5c0c-125">Clave externa en la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5c0c-125">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="b5c0c-126">Componente que contiene el archivo compartido, normalmente un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-126">The component that contains the shared file, usually a DLL.</span></span> <span data-ttu-id="b5c0c-127">La DLL debe ser el archivo de clave de este componente.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-127">The DLL should be the key file for this component.</span></span> <span data-ttu-id="b5c0c-128">Debe ser un componente diferente del que se muestra en la \_ columna aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-128">This must be a different component than listed in the Component\_Application column.</span></span>

<span data-ttu-id="b5c0c-129">El componente compartido controla el registro de todas las copias aisladas del componente y debe tener la marca **msidbComponentAttributesSharedDllRefCount** establecida en la columna Attributes de la tabla de componentes.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-129">The shared component controls the registration for all the isolated copies of the component and must have the **msidbComponentAttributesSharedDllRefCount** flag set in the Attributes column of the Component table.</span></span> <span data-ttu-id="b5c0c-130">Esto garantiza que el instalador puede administrar la vida del componente compartido.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-130">This ensures that the installer can manage the life of the shared component.</span></span>

</dd> <dt>

<span data-ttu-id="b5c0c-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Aplicación de componentes \_</span><span class="sxs-lookup"><span data-stu-id="b5c0c-131"><span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Component\_Application</span></span>
</dt> <dd>

<span data-ttu-id="b5c0c-132">Clave externa en la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5c0c-132">Foreign key into the [Component table](component-table.md).</span></span> <span data-ttu-id="b5c0c-133">Componente que contiene el. exe que carga el archivo compartido.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-133">The component that contains the .exe which loads the shared file.</span></span> <span data-ttu-id="b5c0c-134">El archivo. exe debe ser el archivo de clave de este componente.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-134">The .exe should be the key file for this component.</span></span> <span data-ttu-id="b5c0c-135">Debe ser un componente diferente del que se muestra en la \_ columna Shared del componente.</span><span class="sxs-lookup"><span data-stu-id="b5c0c-135">This must be a different component than listed in the Component\_Shared column.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="b5c0c-136">Validación</span><span class="sxs-lookup"><span data-stu-id="b5c0c-136">Validation</span></span>

<dl>

[<span data-ttu-id="b5c0c-137">ICE03</span><span class="sxs-lookup"><span data-stu-id="b5c0c-137">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="b5c0c-138">ICE06</span><span class="sxs-lookup"><span data-stu-id="b5c0c-138">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="b5c0c-139">ICE32</span><span class="sxs-lookup"><span data-stu-id="b5c0c-139">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="b5c0c-140">ICE62</span><span class="sxs-lookup"><span data-stu-id="b5c0c-140">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="b5c0c-141">ICE66</span><span class="sxs-lookup"><span data-stu-id="b5c0c-141">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="b5c0c-142">ICE97</span><span class="sxs-lookup"><span data-stu-id="b5c0c-142">ICE97</span></span>](ice97.md)  
</dl>

 

 



