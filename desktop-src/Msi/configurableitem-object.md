---
description: El objeto ConfigurableItem representa una sola fila de la tabla ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Objeto ConfigurableItem (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653924"
---
# <a name="configurableitem-object"></a><span data-ttu-id="c4e5f-103">Objeto ConfigurableItem</span><span class="sxs-lookup"><span data-stu-id="c4e5f-103">ConfigurableItem object</span></span>

<span data-ttu-id="c4e5f-104">El **objeto ConfigurableItem** representa una sola fila de la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4e5f-104">The **ConfigurableItem object** represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="c4e5f-105">Se trata de un único "atributo" configurable desde el módulo.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-105">This is a single configurable "attribute" from the module.</span></span> <span data-ttu-id="c4e5f-106">La interfaz consta de propiedades de solo lectura, una para cada columna de la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-106">The interface consists read-only properties, one for each column in the ModuleConfiguration table.</span></span> <span data-ttu-id="c4e5f-107">La definición de la interfaz es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-107">The Interface definition is as follows.</span></span>

## <a name="members"></a><span data-ttu-id="c4e5f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c4e5f-108">Members</span></span>

<span data-ttu-id="c4e5f-109">El objeto **ConfigurableItem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c4e5f-109">The **ConfigurableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="c4e5f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4e5f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4e5f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4e5f-111">Properties</span></span>

<span data-ttu-id="c4e5f-112">El objeto **ConfigurableItem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-112">The **ConfigurableItem** object has these properties.</span></span>



| <span data-ttu-id="c4e5f-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c4e5f-113">Property</span></span>                                                         | <span data-ttu-id="c4e5f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4e5f-114">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4e5f-115">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-115">**Attributes**</span></span>](configurableitem-attributes.md)<br/>     | <span data-ttu-id="c4e5f-116">Devuelve el valor del campo Attributes del registro de este objeto en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-116">Returns the value in the Attributes field of this object's record in the ModuleConfiguration table.</span></span><br/>                            |
| [<span data-ttu-id="c4e5f-117">**Context**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-117">**Context**</span></span>](configurableitem-context.md)<br/>           | <span data-ttu-id="c4e5f-118">Devuelve el valor en el campo de contexto del registro de este objeto en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-118">Returns the value in the Context field of this object's record in the ModuleConfiguration table.</span></span><br/>                               |
| [<span data-ttu-id="c4e5f-119">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-119">**DefaultValue**</span></span>](configurableitem-defaultvalue.md)<br/> | <span data-ttu-id="c4e5f-120">Devuelve el valor del campo DefaultValue del registro de este objeto en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-120">Returns the value in the DefaultValue field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="c4e5f-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-121">**Description**</span></span>](configurableitem-description.md)<br/>   | <span data-ttu-id="c4e5f-122">Devuelve el valor en el campo de Descripción del registro de este objeto en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-122">Returns the value in the Description field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="c4e5f-123">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-123">**DisplayName**</span></span>](configurableitem-displayname.md)<br/>   | <span data-ttu-id="c4e5f-124">Devuelve el valor en el campo DisplayName del registro de este objeto en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-124">Returns the value in the DisplayName field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="c4e5f-125">**Aplique**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-125">**Format**</span></span>](configurableitem-format.md)<br/>             | <span data-ttu-id="c4e5f-126">Devuelve el valor en el campo de formato del registro de este objeto en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-126">Returns the value in the Format field of this object's record in the ModuleConfiguration table.</span></span><br/>                                |
| [<span data-ttu-id="c4e5f-127">**HelpKeyword**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-127">**HelpKeyword**</span></span>](configurableitem-helpkeyword.md)<br/>   | <span data-ttu-id="c4e5f-128">Devuelve el valor del campo HelpKeyword del registro de este objeto en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-128">Returns the value in the HelpKeyword field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="c4e5f-129">**HelpLocation**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-129">**HelpLocation**</span></span>](configurableitem-helplocation.md)<br/> | <span data-ttu-id="c4e5f-130">Devuelve el valor en el campo HelpLocation del registro de este objeto en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-130">Returns the value in the HelpLocation field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="c4e5f-131">**Name**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-131">**Name**</span></span>](configurableitem-name.md)<br/>                 | <span data-ttu-id="c4e5f-132">Devuelve el valor del campo Nombre del registro de este objeto en la [tabla ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="c4e5f-132">Returns the value in the Name field of this object's record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span><br/> |
| [<span data-ttu-id="c4e5f-133">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-133">**Type**</span></span>](configurableitem-type.md)<br/>                 | <span data-ttu-id="c4e5f-134">Devuelve el valor en el campo de tipo del registro de este objeto en la tabla ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c4e5f-134">Returns the value in the Type field of this object's record in the ModuleConfiguration table.</span></span><br/>                                  |



 

## <a name="c"></a><span data-ttu-id="c4e5f-135">C++</span><span class="sxs-lookup"><span data-stu-id="c4e5f-135">C++</span></span>

<span data-ttu-id="c4e5f-136">interfaz **IMsmConfigurableItem: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-136">interface **IMsmConfigurableItem : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="c4e5f-137">IDENTIFICADOR de interfaz</span><span class="sxs-lookup"><span data-stu-id="c4e5f-137">Interface ID</span></span>



| <span data-ttu-id="c4e5f-138">Constante</span><span class="sxs-lookup"><span data-stu-id="c4e5f-138">Constant</span></span>                      | <span data-ttu-id="c4e5f-139">Value</span><span class="sxs-lookup"><span data-stu-id="c4e5f-139">Value</span></span>                                  |
|-------------------------------|----------------------------------------|
| <span data-ttu-id="c4e5f-140">**\_IMSMCONFIGURABLEITEM IID**</span><span class="sxs-lookup"><span data-stu-id="c4e5f-140">**IID\_IMsmConfigurableItem**</span></span> | <span data-ttu-id="c4e5f-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span><span class="sxs-lookup"><span data-stu-id="c4e5f-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c4e5f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4e5f-142">Requirements</span></span>



| <span data-ttu-id="c4e5f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4e5f-143">Requirement</span></span> | <span data-ttu-id="c4e5f-144">Value</span><span class="sxs-lookup"><span data-stu-id="c4e5f-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e5f-145">Versión</span><span class="sxs-lookup"><span data-stu-id="c4e5f-145">Version</span></span><br/> | <span data-ttu-id="c4e5f-146">Mergemod.dll 2,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="c4e5f-146">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="c4e5f-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4e5f-147">Header</span></span><br/>  | <dl> <span data-ttu-id="c4e5f-148"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4e5f-148"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4e5f-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4e5f-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="c4e5f-150"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4e5f-150"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




