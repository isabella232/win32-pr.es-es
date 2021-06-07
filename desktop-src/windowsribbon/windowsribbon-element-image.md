---
title: Elemento Image (Marco de la cinta de opciones de Windows)
description: Representa una imagen.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Cinta de opciones de Windows del elemento Image
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe0b9afb51697d50de9cb80886cf829b90c81262
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442896"
---
# <a name="image-element"></a><span data-ttu-id="61816-104">Elemento Image</span><span class="sxs-lookup"><span data-stu-id="61816-104">Image element</span></span>

<span data-ttu-id="61816-105">Representa una imagen.</span><span class="sxs-lookup"><span data-stu-id="61816-105">Represents an image.</span></span>

## <a name="usage"></a><span data-ttu-id="61816-106">Uso</span><span class="sxs-lookup"><span data-stu-id="61816-106">Usage</span></span>

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
```

## <a name="attributes"></a><span data-ttu-id="61816-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="61816-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61816-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="61816-108">Attribute</span></span></th>
<th><span data-ttu-id="61816-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="61816-109">Type</span></span></th>
<th><span data-ttu-id="61816-110">Requerido</span><span class="sxs-lookup"><span data-stu-id="61816-110">Required</span></span></th>
<th><span data-ttu-id="61816-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="61816-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61816-112"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="61816-112"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="61816-113">xs:positiveInteger union xs:string</span><span class="sxs-lookup"><span data-stu-id="61816-113">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="61816-114">No</span><span class="sxs-lookup"><span data-stu-id="61816-114">No</span></span><br/></td>
<td><span data-ttu-id="61816-115">Identificador de recurso único.</span><span class="sxs-lookup"><span data-stu-id="61816-115">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="61816-116">
<dt><span></span><span></span><strong></strong> (La unión de xs:positiveInteger y xs:string)</span><span class="sxs-lookup"><span data-stu-id="61816-116">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="61816-117">Valor entero comprendido entre 2 y 59999, ambos incluidos, 0x2 y 0xea5f en formato hexadecimal, inclusivo.</span><span class="sxs-lookup"><span data-stu-id="61816-117">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="61816-118">La longitud máxima es de 10 caracteres, incluidos los ceros iniciales opcionales.</span><span class="sxs-lookup"><span data-stu-id="61816-118">The maximum length is 10 characters including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61816-119"><strong>MinDPI</strong></span><span class="sxs-lookup"><span data-stu-id="61816-119"><strong>MinDPI</strong></span></span><br/></td>
<td><span data-ttu-id="61816-120">xs:positiveInteger</span><span class="sxs-lookup"><span data-stu-id="61816-120">xs:positiveInteger</span></span><br/></td>
<td><span data-ttu-id="61816-121">No</span><span class="sxs-lookup"><span data-stu-id="61816-121">No</span></span><br/></td>
<td><span data-ttu-id="61816-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span><span class="sxs-lookup"><span data-stu-id="61816-122"><dt><span></span><span></span><strong></strong> (xs:positiveInteger)</span></span><br/> </dt> <dd> <span data-ttu-id="61816-123">Cualquier secuencia de dígitos con un valor mínimo de 96.</span><span class="sxs-lookup"><span data-stu-id="61816-123">Any sequence of digits with a minimum value of 96.</span></span> <br/> <span data-ttu-id="61816-124">Si se omite MinDPI, el valor predeterminado es 96.</span><span class="sxs-lookup"><span data-stu-id="61816-124">If MinDPI is omitted, the default value is 96.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61816-125"><strong>Origen</strong></span><span class="sxs-lookup"><span data-stu-id="61816-125"><strong>Source</strong></span></span><br/></td>
<td><span data-ttu-id="61816-126">xs:anyURI</span><span class="sxs-lookup"><span data-stu-id="61816-126">xs:anyURI</span></span><br/></td>
<td><span data-ttu-id="61816-127">No</span><span class="sxs-lookup"><span data-stu-id="61816-127">No</span></span><br/></td>
<td><span data-ttu-id="61816-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span><span class="sxs-lookup"><span data-stu-id="61816-128"><dt><span></span><span></span><strong></strong> (xs:anyURI)</span></span><br/> </dt> <dd> <span data-ttu-id="61816-129">Cualquier secuencia de caracteres que represente un URI.</span><span class="sxs-lookup"><span data-stu-id="61816-129">Any sequence of characters that represents a URI.</span></span> <span data-ttu-id="61816-130">El valor uri es una ruta de acceso absoluta o relativa (al archivo de marcado de la cinta de opciones) a un recurso de imagen de tipo BMP.</span><span class="sxs-lookup"><span data-stu-id="61816-130">The URI value is an absolute or relative (to the Ribbon markup file) path to an image resource of type BMP.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61816-131"><strong>Símbolo</strong></span><span class="sxs-lookup"><span data-stu-id="61816-131"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="61816-132">xs:string</span><span class="sxs-lookup"><span data-stu-id="61816-132">xs:string</span></span><br/></td>
<td><span data-ttu-id="61816-133">No</span><span class="sxs-lookup"><span data-stu-id="61816-133">No</span></span><br/></td>
<td><span data-ttu-id="61816-134">Símbolo de recurso para la imagen.</span><span class="sxs-lookup"><span data-stu-id="61816-134">The resource symbol for the image.</span></span><br/> <br/><span data-ttu-id="61816-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span><span class="sxs-lookup"><span data-stu-id="61816-135">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="61816-136">Cadena formada por una letra o un carácter de subrayado seguido de cualquier secuencia de letras, dígitos o caracteres de subrayado hasta un máximo de 100 caracteres.</span><span class="sxs-lookup"><span data-stu-id="61816-136">A string composed of a letter or underscore followed by any sequence of letters, digits, or underscores up to a maximum of 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="61816-137">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="61816-137">Child elements</span></span>



| <span data-ttu-id="61816-138">Elemento</span><span class="sxs-lookup"><span data-stu-id="61816-138">Element</span></span>                                                               | <span data-ttu-id="61816-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="61816-139">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="61816-140">**Image.Source**</span><span class="sxs-lookup"><span data-stu-id="61816-140">**Image.Source**</span></span>](windowsribbon-element-image-source.md)<br/> | <span data-ttu-id="61816-141">Puede producirse como máximo una vez</span><span class="sxs-lookup"><span data-stu-id="61816-141">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="61816-142">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="61816-142">Parent elements</span></span>



| <span data-ttu-id="61816-143">Elemento</span><span class="sxs-lookup"><span data-stu-id="61816-143">Element</span></span>                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61816-144">**Command.LargeHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="61816-144">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [<span data-ttu-id="61816-145">**Command.LargeImages**</span><span class="sxs-lookup"><span data-stu-id="61816-145">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         |
| [<span data-ttu-id="61816-146">**Command.SmallHighContrastImages**</span><span class="sxs-lookup"><span data-stu-id="61816-146">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [<span data-ttu-id="61816-147">**Command.SmallImages**</span><span class="sxs-lookup"><span data-stu-id="61816-147">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a><span data-ttu-id="61816-148">Comentarios</span><span class="sxs-lookup"><span data-stu-id="61816-148">Remarks</span></span>

<span data-ttu-id="61816-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="61816-149">Optional.</span></span>

<span data-ttu-id="61816-150">Puede producirse una o varias veces para cada [**elemento Command.SmallImages,**](windowsribbon-element-command-smallimages.md) [**Command.SmallHighContrastImages,**](windowsribbon-element-command-smallhighcontrastimages.md) [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)o [**Command.LargeHighContrastImages.**](windowsribbon-element-command-largehighcontrastimages.md)</span><span class="sxs-lookup"><span data-stu-id="61816-150">May occur one or more times for each [**Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md), or [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) element.</span></span>

<span data-ttu-id="61816-151">Cuando se proporciona una colección de recursos de imagen diseñados para admitir valores específicos de puntos de pantalla por  pulgada (ppp) al marco de la cinta de opciones a través de un conjunto de elementos **Image,** el marco usa la imagen con un valor de atributo *MinDPI* que coincide con la configuración de ppp de la pantalla actual.</span><span class="sxs-lookup"><span data-stu-id="61816-151">When a collection of image resources that are designed to support specific screen dots per inch (dpi) settings is supplied to the Ribbon framework through a set of **Image** elements, the framework uses the **Image** with a *MinDPI* attribute value that matches the current screen dpi setting.</span></span>

<span data-ttu-id="61816-152">Si no se declara ningún elemento **Image** con un valor *MinDPI* que  coincida con la configuración de ppp de la pantalla actual, el marco elige la imagen que tiene el valor *MinDPI* más próximo menos que el valor de ppp de la pantalla actual y escala verticalmente el recurso de imagen.</span><span class="sxs-lookup"><span data-stu-id="61816-152">If no **Image** element is declared with a *MinDPI* value that matches the current screen dpi setting, the framework picks the **Image** that has the nearest *MinDPI* value less than the current screen dpi setting and scales the image resource up.</span></span> <span data-ttu-id="61816-153">De lo contrario, si no se declara ningún elemento **Image** con un valor de atributo *MinDPI* menor que el valor de ppp de pantalla actual, el marco elige el valor *MinDPI* más próximo mayor que el valor de ppp de pantalla actual y escala el recurso de imagen hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="61816-153">Otherwise, if no **Image** element is declared with a *MinDPI* attribute value less than the current screen dpi setting, the framework picks the nearest *MinDPI* value greater than the current screen dpi setting and scales the image resource down.</span></span>

## <a name="examples"></a><span data-ttu-id="61816-154">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="61816-154">Examples</span></span>

<span data-ttu-id="61816-155">En el ejemplo de código siguiente se muestra el marcado necesario para declarar, a través de un conjunto de elementos **Image,** una colección de recursos de imagen diseñados para admitir cuatro configuraciones de ppp de pantalla específicas.</span><span class="sxs-lookup"><span data-stu-id="61816-155">The following code example shows the markup required to declare, through a set of **Image** elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="61816-156">Información de elemento</span><span class="sxs-lookup"><span data-stu-id="61816-156">Element information</span></span>

* <span data-ttu-id="61816-157">**Sistema mínimo admitido:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="61816-157">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="61816-158">**Puede estar vacío:** No</span><span class="sxs-lookup"><span data-stu-id="61816-158">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="61816-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="61816-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61816-160">Especificar recursos de imagen de cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="61816-160">Specifying Ribbon Image Resources</span></span>](windowsribbon-imageformats.md)
</dt> </dl>

 

 





