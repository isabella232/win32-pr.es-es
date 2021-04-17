---
description: Es el elemento raíz de un archivo de script XML del generador de código de WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: elemento wsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715702"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="ae08a-103">elemento wsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="ae08a-103">wsdCodeGen element</span></span>

<span data-ttu-id="ae08a-104">Es el elemento raíz de un archivo de script XML del generador de código de WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ae08a-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="ae08a-105">Uso</span><span class="sxs-lookup"><span data-stu-id="ae08a-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="ae08a-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae08a-106">Attributes</span></span>



| <span data-ttu-id="ae08a-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="ae08a-107">Attribute</span></span>                        | <span data-ttu-id="ae08a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae08a-108">Type</span></span>                             | <span data-ttu-id="ae08a-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="ae08a-109">Required</span></span>       | <span data-ttu-id="ae08a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae08a-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae08a-111">**ConfigFileVersion**</span><span class="sxs-lookup"><span data-stu-id="ae08a-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="ae08a-112">Cualquier cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="ae08a-112">Any character string.</span></span><br/> | <span data-ttu-id="ae08a-113">Sí</span><span class="sxs-lookup"><span data-stu-id="ae08a-113">Yes</span></span><br/> | <span data-ttu-id="ae08a-114">Versión del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="ae08a-114">The version of the configuration file.</span></span> <span data-ttu-id="ae08a-115">El único valor válido es "1,0".</span><span class="sxs-lookup"><span data-stu-id="ae08a-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="ae08a-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae08a-116">Child elements</span></span>



| <span data-ttu-id="ae08a-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="ae08a-117">Element</span></span>                                                         | <span data-ttu-id="ae08a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="ae08a-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae08a-119">**autoestática**</span><span class="sxs-lookup"><span data-stu-id="ae08a-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="ae08a-120">Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos.</span><span class="sxs-lookup"><span data-stu-id="ae08a-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="ae08a-121">Esta opción está habilitada de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ae08a-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="ae08a-122">**archivo**</span><span class="sxs-lookup"><span data-stu-id="ae08a-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="ae08a-123">Dirige el generador de código para generar un archivo.</span><span class="sxs-lookup"><span data-stu-id="ae08a-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="ae08a-124">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="ae08a-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="ae08a-125">Los metadatos de hospedaje para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="ae08a-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="ae08a-126">Este elemento se usa solo para implementaciones de dispositivos (hosts).</span><span class="sxs-lookup"><span data-stu-id="ae08a-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="ae08a-127">**layerNumber**</span><span class="sxs-lookup"><span data-stu-id="ae08a-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="ae08a-128">Número de la capa de código que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="ae08a-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="ae08a-129">Los números de capa se utilizan en tablas en tiempo de ejecución para distinguir un nivel de código para otro.</span><span class="sxs-lookup"><span data-stu-id="ae08a-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="ae08a-130">WSDAPI utiliza código generado que tiene un número de capa de 0.</span><span class="sxs-lookup"><span data-stu-id="ae08a-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="ae08a-131">**layerPrefix**</span><span class="sxs-lookup"><span data-stu-id="ae08a-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="ae08a-132">Prefijo que se va a usar en el código generado para garantizar la unicidad de los símbolos generados.</span><span class="sxs-lookup"><span data-stu-id="ae08a-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="ae08a-133">WSDAPI usa el prefijo "WSD".</span><span class="sxs-lookup"><span data-stu-id="ae08a-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="ae08a-134">**macro**</span><span class="sxs-lookup"><span data-stu-id="ae08a-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="ae08a-135">Define el texto o el CDATA que va a reutilizar el elemento [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="ae08a-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="ae08a-136">**System.IO**</span><span class="sxs-lookup"><span data-stu-id="ae08a-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="ae08a-137">Describe un espacio de nombres que se usará para la generación de código.</span><span class="sxs-lookup"><span data-stu-id="ae08a-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="ae08a-138">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="ae08a-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="ae08a-139">Describe el host y los metadatos hospedados para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae08a-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="ae08a-140">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="ae08a-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="ae08a-141">Los metadatos del fabricante y del modelo para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="ae08a-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="ae08a-142">Este elemento se usa solo para implementaciones de dispositivos (hosts).</span><span class="sxs-lookup"><span data-stu-id="ae08a-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="ae08a-143">**mencionados**</span><span class="sxs-lookup"><span data-stu-id="ae08a-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="ae08a-144">Especifica un archivo WSDL que se va a procesar para la información del contrato.</span><span class="sxs-lookup"><span data-stu-id="ae08a-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="ae08a-145">**BTM**</span><span class="sxs-lookup"><span data-stu-id="ae08a-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="ae08a-146">Especifica un archivo XSD para procesar la información de contrato.</span><span class="sxs-lookup"><span data-stu-id="ae08a-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="ae08a-147">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae08a-147">Child element sequence</span></span>

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a><span data-ttu-id="ae08a-148">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ae08a-148">Parent elements</span></span>

<span data-ttu-id="ae08a-149">No hay elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ae08a-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae08a-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae08a-150">Remarks</span></span>

<span data-ttu-id="ae08a-151">En general, los elementos de [**archivo**](file.md) deben aparecer en último lugar porque generan código que utiliza los datos especificados por los demás elementos.</span><span class="sxs-lookup"><span data-stu-id="ae08a-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="ae08a-152">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="ae08a-152">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="ae08a-153">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae08a-153">Minimum supported system</span></span><br/> | <span data-ttu-id="ae08a-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae08a-154">Windows Vista</span></span> |
| <span data-ttu-id="ae08a-155">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ae08a-155">Can be empty</span></span>                        | <span data-ttu-id="ae08a-156">Sí</span><span class="sxs-lookup"><span data-stu-id="ae08a-156">Yes</span></span>           |



 

 




