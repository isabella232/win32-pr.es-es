---
title: Método media. getItemInfoByType
description: El método getItemInfoByType recupera el valor del atributo correspondiente al nombre de atributo, el idioma y el índice especificados.
ms.assetid: 9d3377c2-7ae8-48ce-a42e-9c965f6b79f9
keywords:
- método getItemInfoByType de Windows Media Player
- método getItemInfoByType Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- Media.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc2aff2bee7641075bbac1dd04526ee751ea077a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700234"
---
# <a name="mediagetiteminfobytype-method"></a><span data-ttu-id="40cf4-106">Método media. getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="40cf4-106">Media.getItemInfoByType method</span></span>

<span data-ttu-id="40cf4-107">El método **getItemInfoByType** recupera el valor del atributo correspondiente al nombre de atributo, el idioma y el índice especificados.</span><span class="sxs-lookup"><span data-stu-id="40cf4-107">The **getItemInfoByType** method retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span>

## <a name="syntax"></a><span data-ttu-id="40cf4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40cf4-108">Syntax</span></span>


```JScript
retVal = Media.getItemInfoByType(
  name,
  language,
  index
)
```



## <a name="parameters"></a><span data-ttu-id="40cf4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40cf4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40cf4-110">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="40cf4-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40cf4-111">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="40cf4-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="40cf4-112">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="40cf4-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="40cf4-113">*idioma* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="40cf4-113">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40cf4-114">**Cadena** que representa el idioma.</span><span class="sxs-lookup"><span data-stu-id="40cf4-114">**String** representing the language.</span></span> <span data-ttu-id="40cf4-115">Si el valor se establece en null o en "" (cadena vacía), se usa la cadena de configuración regional actual.</span><span class="sxs-lookup"><span data-stu-id="40cf4-115">If the value is set to null or "" (empty string) the current locale string is used.</span></span> <span data-ttu-id="40cf4-116">De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="40cf4-116">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="40cf4-117">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="40cf4-117">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40cf4-118">**Número** (**largo**) que contiene el índice de base cero del valor que se va a recuperar del atributo.</span><span class="sxs-lookup"><span data-stu-id="40cf4-118">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40cf4-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40cf4-119">Return value</span></span>

<span data-ttu-id="40cf4-120">Este método devuelve un **número**, una **cadena**, un objeto **MetadataPicture** o un objeto **MetadataText** , como se indica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="40cf4-120">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="40cf4-121">Atributo</span><span class="sxs-lookup"><span data-stu-id="40cf4-121">Attribute</span></span>                   | <span data-ttu-id="40cf4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40cf4-122">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="40cf4-123">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="40cf4-123">**SyncState**</span></span>               | <span data-ttu-id="40cf4-124">**Número** (**unsigned Long**)</span><span class="sxs-lookup"><span data-stu-id="40cf4-124">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="40cf4-125">**WM/Letras \_ sincronizadas**</span><span class="sxs-lookup"><span data-stu-id="40cf4-125">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="40cf4-126">Objeto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="40cf4-126">**MetadataText** object</span></span>        |
| <span data-ttu-id="40cf4-127">**WM/imagen**</span><span class="sxs-lookup"><span data-stu-id="40cf4-127">**WM/Picture**</span></span>              | <span data-ttu-id="40cf4-128">Objeto **MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="40cf4-128">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="40cf4-129">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="40cf4-129">**WM/UserWebURL**</span></span>           | <span data-ttu-id="40cf4-130">Objeto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="40cf4-130">**MetadataText** object</span></span>        |
| <span data-ttu-id="40cf4-131">Resto de atributos</span><span class="sxs-lookup"><span data-stu-id="40cf4-131">All other attributes</span></span>        | <span data-ttu-id="40cf4-132">**String**</span><span class="sxs-lookup"><span data-stu-id="40cf4-132">**String**</span></span>                     |



 

<span data-ttu-id="40cf4-133">En el caso de los atributos cuyo valor subyacente es **booleano**, este método devuelve la cadena "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="40cf4-133">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="40cf4-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40cf4-134">Remarks</span></span>

<span data-ttu-id="40cf4-135">Este método recupera los metadatos de un elemento multimedia o elemento multimedia individual que forma parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="40cf4-135">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="40cf4-136">Este método admite atributos con varios valores y atributos con valores complejos.</span><span class="sxs-lookup"><span data-stu-id="40cf4-136">This method supports attributes with multiple values and attributes with complex values.</span></span> <span data-ttu-id="40cf4-137">El método **getItemInfo** no admite atributos con varios valores y atributos con valores complejos.</span><span class="sxs-lookup"><span data-stu-id="40cf4-137">The **getItemInfo** method does not support attributes with multiple values and attributes with complex values.</span></span>

<span data-ttu-id="40cf4-138">La propiedad **attributeCount** contiene el número de nombres de atributo disponibles para un objeto **multimedia** determinado.</span><span class="sxs-lookup"><span data-stu-id="40cf4-138">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="40cf4-139">Los números de índice se pueden usar con el método **getAttributeName** para determinar el nombre de cada atributo disponible.</span><span class="sxs-lookup"><span data-stu-id="40cf4-139">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="40cf4-140">Los nombres de atributo individuales se pueden pasar al parámetro *Name* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="40cf4-140">Individual attribute names can be passed to the *name* parameter of **getItemInfoByType**.</span></span>

<span data-ttu-id="40cf4-141">El método **getAttributeCountByType** devuelve el número de atributos que corresponden a un nombre de atributo determinado para un objeto **multimedia** determinado.</span><span class="sxs-lookup"><span data-stu-id="40cf4-141">The **getAttributeCountByType** method returns the number of attributes that correspond to a particular attribute name for a given **Media** object.</span></span> <span data-ttu-id="40cf4-142">Los números de índice se pueden pasar al parámetro de *Índice* de **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="40cf4-142">Index numbers can then be passed to the *index* parameter of **getItemInfoByType**.</span></span> <span data-ttu-id="40cf4-143">Esto resulta útil cuando un elemento multimedia digital se ha clasificado en varios géneros, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="40cf4-143">This is useful when a digital media item has been categorized under multiple genres, for example.</span></span>

<span data-ttu-id="40cf4-144">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="40cf4-144">To use this method, read access to the library is required.</span></span> <span data-ttu-id="40cf4-145">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="40cf4-145">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="40cf4-146">Este método puede producir errores.</span><span class="sxs-lookup"><span data-stu-id="40cf4-146">This method can cause errors.</span></span> <span data-ttu-id="40cf4-147">Debe incluir el código de control de errores al llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="40cf4-147">You should include error-handling code when you call this method.</span></span> <span data-ttu-id="40cf4-148">Por ejemplo, en JScript puede implementar el control de errores mediante el uso de la **instrucción try... detectar... Finally** (estructura).</span><span class="sxs-lookup"><span data-stu-id="40cf4-148">For example, in JScript you can implement error handling by using the **try...catch...finally** structure.</span></span>

<span data-ttu-id="40cf4-149">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="40cf4-149">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="40cf4-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40cf4-150">Requirements</span></span>



| <span data-ttu-id="40cf4-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="40cf4-151">Requirement</span></span> | <span data-ttu-id="40cf4-152">Value</span><span class="sxs-lookup"><span data-stu-id="40cf4-152">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="40cf4-153">Versión</span><span class="sxs-lookup"><span data-stu-id="40cf4-153">Version</span></span><br/> | <span data-ttu-id="40cf4-154">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="40cf4-154">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="40cf4-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="40cf4-155">DLL</span></span><br/>     | <dl> <span data-ttu-id="40cf4-156"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40cf4-156"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40cf4-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="40cf4-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40cf4-158">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="40cf4-158">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="40cf4-159">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="40cf4-159">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="40cf4-160">**Media. getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="40cf4-160">**Media.getAttributeCountByType**</span></span>](media-getattributecountbytype.md)
</dt> <dt>

[<span data-ttu-id="40cf4-161">**Media. getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="40cf4-161">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="40cf4-162">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="40cf4-162">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="40cf4-163">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="40cf4-163">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="40cf4-164">**Objeto MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="40cf4-164">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="40cf4-165">**Objeto MetadataText**</span><span class="sxs-lookup"><span data-stu-id="40cf4-165">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="40cf4-166">**Leer valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="40cf4-166">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="40cf4-167">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="40cf4-167">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="40cf4-168">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="40cf4-168">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





