---
description: Es el elemento raíz de un archivo de script XML del generador de código WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: wsdCodeGen, elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9861617854e0e75575f2993717f5b2a86515fb0f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994682"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="edccf-103">wsdCodeGen, elemento</span><span class="sxs-lookup"><span data-stu-id="edccf-103">wsdCodeGen element</span></span>

<span data-ttu-id="edccf-104">Es el elemento raíz de un archivo de script XML del generador de código WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="edccf-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="edccf-105">Uso</span><span class="sxs-lookup"><span data-stu-id="edccf-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="edccf-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="edccf-106">Attributes</span></span>



| <span data-ttu-id="edccf-107">Atributo</span><span class="sxs-lookup"><span data-stu-id="edccf-107">Attribute</span></span>                        | <span data-ttu-id="edccf-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="edccf-108">Type</span></span>                             | <span data-ttu-id="edccf-109">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="edccf-109">Required</span></span>       | <span data-ttu-id="edccf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="edccf-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="edccf-111">**ConfigFileVersion**</span><span class="sxs-lookup"><span data-stu-id="edccf-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="edccf-112">Cualquier cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="edccf-112">Any character string.</span></span><br/> | <span data-ttu-id="edccf-113">Sí</span><span class="sxs-lookup"><span data-stu-id="edccf-113">Yes</span></span><br/> | <span data-ttu-id="edccf-114">Versión del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="edccf-114">The version of the configuration file.</span></span> <span data-ttu-id="edccf-115">El único valor válido es "1.0".</span><span class="sxs-lookup"><span data-stu-id="edccf-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="edccf-116">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="edccf-116">Child elements</span></span>



| <span data-ttu-id="edccf-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="edccf-117">Element</span></span>                                                         | <span data-ttu-id="edccf-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="edccf-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="edccf-119">**autoStatic**</span><span class="sxs-lookup"><span data-stu-id="edccf-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="edccf-120">Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos.</span><span class="sxs-lookup"><span data-stu-id="edccf-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="edccf-121">Esta opción está habilitada de manera predeterminada.</span><span class="sxs-lookup"><span data-stu-id="edccf-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="edccf-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="edccf-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="edccf-123">Dirige al generador de código para generar un archivo.</span><span class="sxs-lookup"><span data-stu-id="edccf-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="edccf-124">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="edccf-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="edccf-125">Metadatos de hospedaje para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="edccf-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="edccf-126">Este elemento solo se usa para implementaciones de dispositivos (hosts).</span><span class="sxs-lookup"><span data-stu-id="edccf-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="edccf-127">**layerNumber**</span><span class="sxs-lookup"><span data-stu-id="edccf-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="edccf-128">Número de la capa de código que se va a generar.</span><span class="sxs-lookup"><span data-stu-id="edccf-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="edccf-129">Los números de capa se usan en tablas en tiempo de ejecución para distinguir una capa de código para otra.</span><span class="sxs-lookup"><span data-stu-id="edccf-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="edccf-130">El propio WSDAPI usa código generado que tiene un número de capa de 0.</span><span class="sxs-lookup"><span data-stu-id="edccf-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="edccf-131">**layerPrefix**</span><span class="sxs-lookup"><span data-stu-id="edccf-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="edccf-132">Prefijo que se usará en el código generado para garantizar la unidad de los símbolos generados.</span><span class="sxs-lookup"><span data-stu-id="edccf-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="edccf-133">WSDAPI usa el prefijo "WSD".</span><span class="sxs-lookup"><span data-stu-id="edccf-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="edccf-134">**Macro**</span><span class="sxs-lookup"><span data-stu-id="edccf-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="edccf-135">Define el texto o CDATA que el elemento [**include**](include.md) va a reutilizar.</span><span class="sxs-lookup"><span data-stu-id="edccf-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="edccf-136">**Nombres**</span><span class="sxs-lookup"><span data-stu-id="edccf-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="edccf-137">Describe un espacio de nombres que se usará para la generación de código.</span><span class="sxs-lookup"><span data-stu-id="edccf-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="edccf-138">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="edccf-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="edccf-139">Describe el host y los metadatos hospedados para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="edccf-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="edccf-140">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="edccf-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="edccf-141">Metadatos del fabricante y del modelo para el dispositivo que se va a implementar.</span><span class="sxs-lookup"><span data-stu-id="edccf-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="edccf-142">Este elemento solo se usa para implementaciones de dispositivos (hosts).</span><span class="sxs-lookup"><span data-stu-id="edccf-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="edccf-143">**Wsdl**</span><span class="sxs-lookup"><span data-stu-id="edccf-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="edccf-144">Especifica un archivo WSDL para procesar la información del contrato.</span><span class="sxs-lookup"><span data-stu-id="edccf-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="edccf-145">**Xsd**</span><span class="sxs-lookup"><span data-stu-id="edccf-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="edccf-146">Especifica un archivo XSD para procesar la información del contrato.</span><span class="sxs-lookup"><span data-stu-id="edccf-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="edccf-147">Secuencia de elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="edccf-147">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="edccf-148">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="edccf-148">Parent elements</span></span>

<span data-ttu-id="edccf-149">No hay elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="edccf-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="edccf-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="edccf-150">Remarks</span></span>

<span data-ttu-id="edccf-151">En general, [**los elementos de**](file.md) archivo deben producirse en último lugar porque generan código que usa los datos especificados por los demás elementos.</span><span class="sxs-lookup"><span data-stu-id="edccf-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="edccf-152">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="edccf-152">Element information</span></span>



| <span data-ttu-id="edccf-153">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="edccf-153">Label</span></span> | <span data-ttu-id="edccf-154">Value</span><span class="sxs-lookup"><span data-stu-id="edccf-154">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="edccf-155">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="edccf-155">Minimum supported system</span></span><br/> | <span data-ttu-id="edccf-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="edccf-156">Windows Vista</span></span> |
| <span data-ttu-id="edccf-157">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="edccf-157">Can be empty</span></span>                        | <span data-ttu-id="edccf-158">Sí</span><span class="sxs-lookup"><span data-stu-id="edccf-158">Yes</span></span>           |



 

 




