---
title: Elemento Image (marco de cinta de Windows)
description: Representa una imagen.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Cinta de opciones de Windows (elemento)
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d33f6710da2261a359aa7fd0a3b493871155cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104148977"
---
# <a name="image-element"></a><span data-ttu-id="0d238-104">Elemento Image</span><span class="sxs-lookup"><span data-stu-id="0d238-104">Image element</span></span>

<span data-ttu-id="0d238-105">Representa una imagen.</span><span class="sxs-lookup"><span data-stu-id="0d238-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="0d238-106">Uso</span><span class="sxs-lookup"><span data-stu-id="0d238-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="0d238-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="0d238-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0d238-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="0d238-108">Attribute</span></span></th>
<th><span data-ttu-id="0d238-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d238-109">Type</span></span></th>
<th><span data-ttu-id="0d238-110">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="0d238-110">Required</span></span></th>
<th><span data-ttu-id="0d238-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d238-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d238-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="0d238-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="0d238-113">XS: positiveInteger Union XS: String</span><span class="sxs-lookup"><span data-stu-id="0d238-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="0d238-114">No</span><span class="sxs-lookup"><span data-stu-id="0d238-114">No</span></span><br/></td>
<td><span data-ttu-id="0d238-115">IDENTIFICADOR de recurso único.</span><span class="sxs-lookup"><span data-stu-id="0d238-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="0d238-116">
<dt><span></span><span></span><strong></strong> (La Unión de XS: positiveInteger y XS: String)</span><span class="sxs-lookup"><span data-stu-id="0d238-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0d238-117">Un valor entero entre 2 y 59999, inclusive, o 0X2 y 0xea5f en formato hexadecimal, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="0d238-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="0d238-118">La longitud máxima es de 10 caracteres, incluidos los ceros a la izquierda opcionales.</span><span class="sxs-lookup"><span data-stu-id="0d238-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d238-119"><strong>MinDPI</strong></span><span class="sxs-lookup"><span data-stu-id="0d238-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="0d238-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="0d238-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="0d238-121">No</span><span class="sxs-lookup"><span data-stu-id="0d238-121">No</span></span><br/></td>
<td><span data-ttu-id="0d238-122"><dt><span></span><span></span><strong></strong> (XS: positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="0d238-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="0d238-123">Cualquier secuencia de dígitos con un valor mínimo de 96.</span><span class="sxs-lookup"><span data-stu-id="0d238-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="0d238-124">Si se omite MinDPI, el valor predeterminado es 96.</span><span class="sxs-lookup"><span data-stu-id="0d238-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d238-125"><strong>Origen</strong></span><span class="sxs-lookup"><span data-stu-id="0d238-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="0d238-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="0d238-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="0d238-127">No</span><span class="sxs-lookup"><span data-stu-id="0d238-127">No</span></span><br/></td>
<td><span data-ttu-id="0d238-128"><dt><span></span><span></span><strong></strong> (XS: anyURI)</span><span class="sxs-lookup"><span data-stu-id="0d238-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="0d238-129">Cualquier secuencia de caracteres que representa un identificador URI.</span><span class="sxs-lookup"><span data-stu-id="0d238-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="0d238-130">El valor del URI es una ruta de acceso absoluta o relativa (en el archivo de marcado de la cinta de opciones) a un recurso de imagen de tipo BMP.</span><span class="sxs-lookup"><span data-stu-id="0d238-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d238-131"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="0d238-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="0d238-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="0d238-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="0d238-133">No</span><span class="sxs-lookup"><span data-stu-id="0d238-133">No</span></span><br/></td>
<td><span data-ttu-id="0d238-134">Símbolo de recurso de la imagen.</span><span class="sxs-lookup"><span data-stu-id="0d238-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="0d238-135">
<dt><span></span><span></span><strong></strong> (XS: String)</span><span class="sxs-lookup"><span data-stu-id="0d238-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0d238-136">Cadena formada por una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado hasta un máximo de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="0d238-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0d238-137">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0d238-137">Child elements</span></span>



| <span data-ttu-id="0d238-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="0d238-138">Element</span></span>                                                               | <span data-ttu-id="0d238-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d238-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="0d238-140">**Imagen. origen**</span><span class="sxs-lookup"><span data-stu-id="0d238-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="0d238-141">Puede aparecer como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="0d238-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0d238-142">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="0d238-142">Parent elements</span></span>



| <span data-ttu-id="0d238-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="0d238-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d238-144">**Comando. LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="0d238-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="0d238-145">**Comando. LargeImages**</span><span class="sxs-lookup"><span data-stu-id="0d238-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="0d238-146">**Comando. SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="0d238-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="0d238-147">**Comando. SmallImages**</span><span class="sxs-lookup"><span data-stu-id="0d238-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="0d238-148">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d238-148">Remarks</span></span>

<span data-ttu-id="0d238-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="0d238-149">Optional.</span></span>

<span data-ttu-id="0d238-150">Puede producirse una o varias veces para cada elemento [**Command. SmallImages**](windowsribbon-element-command-smallimages.md), [**Command. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. LargeImages**](windowsribbon-element-command-largeimages.md)o [**Command. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) .</span><span class="sxs-lookup"><span data-stu-id="0d238-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="0d238-151">Cuando una colección de recursos de imagen diseñada para admitir la configuración específica de puntos por pulgada (PPP) se proporciona al marco de la cinta de opciones a través de un conjunto de elementos de **imagen** , el marco de trabajo usa la **imagen** con un valor de atributo *MinDPI* que coincide con la configuración de PPP de la pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="0d238-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="0d238-152">Si no se declara ningún elemento de **imagen** con un valor de *MinDPI* que coincida con la configuración de PPP de pantalla actual, el marco de trabajo selecciona la **imagen** que tiene el valor de *MinDPI* más cercano menor que la configuración de PPP de pantalla actual y escala el recurso de imagen hacia arriba.</span><span class="sxs-lookup"><span data-stu-id="0d238-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="0d238-153">De lo contrario, si no se declara ningún elemento de **imagen** con un valor de atributo *MinDPI* inferior al valor de PPP de pantalla actual, el marco de trabajo selecciona el valor de *MinDPI* más cercano mayor que la configuración de PPP de pantalla actual y escala el recurso de imagen hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="0d238-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="0d238-154">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0d238-154">Examples</span></span>

<span data-ttu-id="0d238-155">En el ejemplo de código siguiente se muestra el marcado necesario para declarar, a través de un conjunto de elementos de **imagen** , una colección de recursos de imagen que están diseñados para admitir cuatro configuraciones de PPP de pantalla específicas.</span><span class="sxs-lookup"><span data-stu-id="0d238-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a><span data-ttu-id="0d238-156">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="0d238-156">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="0d238-157">Sistema mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d238-157">Minimum supported system</span></span><br/> | <span data-ttu-id="0d238-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0d238-158">Windows 7</span></span> |
| <span data-ttu-id="0d238-159">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0d238-159">Can be empty</span></span>                        | <span data-ttu-id="0d238-160">No</span><span class="sxs-lookup"><span data-stu-id="0d238-160">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="0d238-161">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0d238-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d238-162">Especificar recursos de imagen de cinta</span><span class="sxs-lookup"><span data-stu-id="0d238-162">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





