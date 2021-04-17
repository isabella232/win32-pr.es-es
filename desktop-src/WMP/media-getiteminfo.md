---
title: Método media. getItemInfo
description: El método getItemInfo recupera el valor del atributo especificado para el elemento multimedia actual.
ms.assetid: a1ee0d40-b979-424b-bd4e-d1acf6354d8d
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- Media.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7e7348e73e3550ed668f6694ccfe9ed615215b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700236"
---
# <a name="mediagetiteminfo-method"></a><span data-ttu-id="5c59f-106">Método media. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="5c59f-106">Media.getItemInfo method</span></span>

<span data-ttu-id="5c59f-107">El método **getItemInfo** recupera el valor del atributo especificado para el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="5c59f-107">The **getItemInfo** method retrieves the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c59f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c59f-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="5c59f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c59f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c59f-110">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5c59f-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c59f-111">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="5c59f-111">**String** containing the name of the attribute.</span></span> <span data-ttu-id="5c59f-112">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5c59f-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c59f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c59f-113">Return value</span></span>

<span data-ttu-id="5c59f-114">Este método devuelve una **cadena** que representa el valor del atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="5c59f-114">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="5c59f-115">En el caso de los atributos cuyo valor subyacente es **booleano**, devuelve la cadena "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="5c59f-115">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="5c59f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c59f-116">Remarks</span></span>

<span data-ttu-id="5c59f-117">Este método recupera los metadatos de un elemento multimedia o elemento multimedia individual que forma parte de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="5c59f-117">This method retrieves the metadata for an individual digital media item or a media item that is part of a playlist.</span></span>

<span data-ttu-id="5c59f-118">La propiedad **attributeCount** contiene el número de nombres de atributo disponibles para un objeto **multimedia** determinado.</span><span class="sxs-lookup"><span data-stu-id="5c59f-118">The **attributeCount** property contains the number of attribute names available for a given **Media** object.</span></span> <span data-ttu-id="5c59f-119">Los números de índice se pueden usar con el método **getAttributeName** para determinar el nombre de cada atributo disponible.</span><span class="sxs-lookup"><span data-stu-id="5c59f-119">Index numbers can then be used with the **getAttributeName** method to determine the name of each available attribute.</span></span> <span data-ttu-id="5c59f-120">Los nombres de atributo individuales se pueden pasar a **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="5c59f-120">Individual attribute names can be passed to **getItemInfo**.</span></span>

<span data-ttu-id="5c59f-121">Para recuperar los atributos con varios valores y atributos con valores complejos, use el método **getItemInfoByType** .</span><span class="sxs-lookup"><span data-stu-id="5c59f-121">To retrieve attributes with multiple values and attributes with complex values, use the **getItemInfoByType** method.</span></span>

<span data-ttu-id="5c59f-122">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5c59f-122">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5c59f-123">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5c59f-123">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="5c59f-124">Para compartir las bibliotecas de Windows Media a través de UPnP, Windows Media Player crea un servicio de directorio de contenido (CDS) que se expone a través de UPnP.</span><span class="sxs-lookup"><span data-stu-id="5c59f-124">To share the Windows media libraries over UPnP, Windows Media Player creates a content directory service (CDS) that is exposed over UPnP.</span></span> <span data-ttu-id="5c59f-125">Otros dispositivos pueden navegar y examinar las bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="5c59f-125">Other devices can then navigate and browse the libraries.</span></span>

<span data-ttu-id="5c59f-126">En Windows 7, una aplicación puede usar los atributos [**TrackingID**](trackingid-attribute.md) y [**MediaType**](mediatype-attribute.md) de Windows Media Player para construir el identificador de objeto de cada elemento de los CD.</span><span class="sxs-lookup"><span data-stu-id="5c59f-126">In Windows 7, an application can use the Windows Media Player [**TrackingID**](trackingid-attribute.md) and [**MediaType**](mediatype-attribute.md) attributes to construct the object ID of each item in the CDS.</span></span> <span data-ttu-id="5c59f-127">Tenga en cuenta que esta construcción podría cambiar en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c59f-127">Note that this construction might change in future versions of Windows.</span></span> <span data-ttu-id="5c59f-128">La aplicación pasa cada una de estas cadenas de atributo en el parámetro *Name* en una llamada a **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="5c59f-128">The application passes each of these attribute strings in the *name* parameter in a call to **getItemInfo**.</span></span> <span data-ttu-id="5c59f-129">**getItemInfo** devuelve el valor de cada atributo en el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="5c59f-129">**getItemInfo** returns the value for each attribute in the return value.</span></span> <span data-ttu-id="5c59f-130">A continuación, la aplicación usa la siguiente sintaxis para construir cada identificador de objeto:</span><span class="sxs-lookup"><span data-stu-id="5c59f-130">The application then uses the following syntax to construct each object ID:</span></span>

<span data-ttu-id="5c59f-131">*TrackingID*. 0. *MediaTypeID*</span><span class="sxs-lookup"><span data-stu-id="5c59f-131">*TrackingID*.0.*MediaTypeID*</span></span>

<span data-ttu-id="5c59f-132">Esta sintaxis tiene el significado siguiente:</span><span class="sxs-lookup"><span data-stu-id="5c59f-132">This syntax has the following meaning:</span></span>

-   <span data-ttu-id="5c59f-133">*TrackingID* es la cadena que se almacena en el atributo Windows Media Player [**TrackingID**](trackingid-attribute.md) del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="5c59f-133">*TrackingID* is the string that is stored in the Windows Media Player [**TrackingID**](trackingid-attribute.md) attribute of the media item.</span></span>
-   <span data-ttu-id="5c59f-134">*MediaTypeID* depende del valor del atributo [**mediatype**](mediatype-attribute.md) , tal como se muestra en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="5c59f-134">*MediaTypeID* depends on the value of the [**MediaType**](mediatype-attribute.md) attribute, as shown in the following table:</span></span>

    | <span data-ttu-id="5c59f-135">MediaType (atributo)</span><span class="sxs-lookup"><span data-stu-id="5c59f-135">MediaType attribute</span></span>                      | <span data-ttu-id="5c59f-136">MediaTypeID</span><span class="sxs-lookup"><span data-stu-id="5c59f-136">MediaTypeID</span></span> |
    |------------------------------------------|-------------|
    | [<span data-ttu-id="5c59f-137">Elementos de audio</span><span class="sxs-lookup"><span data-stu-id="5c59f-137">Audio Items</span></span>](audio-item-attributes.md) | <span data-ttu-id="5c59f-138">4</span><span class="sxs-lookup"><span data-stu-id="5c59f-138">4</span></span>           |
    | [<span data-ttu-id="5c59f-139">Elementos de fotografía</span><span class="sxs-lookup"><span data-stu-id="5c59f-139">Photo Items</span></span>](photo-item-attributes.md) | <span data-ttu-id="5c59f-140">B</span><span class="sxs-lookup"><span data-stu-id="5c59f-140">B</span></span>           |
    | [<span data-ttu-id="5c59f-141">Elementos de vídeo</span><span class="sxs-lookup"><span data-stu-id="5c59f-141">Video Items</span></span>](video-item-attributes.md) | <span data-ttu-id="5c59f-142">8</span><span class="sxs-lookup"><span data-stu-id="5c59f-142">8</span></span>           |

    

     

<span data-ttu-id="5c59f-143">**Windows Media Player 10 Mobile:** Los atributos de un elemento multimedia solo están disponibles durante la reproducción, a menos que se recuperen del elemento a través de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="5c59f-143">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c59f-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c59f-144">Requirements</span></span>



| <span data-ttu-id="5c59f-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c59f-145">Requirement</span></span> | <span data-ttu-id="5c59f-146">Value</span><span class="sxs-lookup"><span data-stu-id="5c59f-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5c59f-147">Versión</span><span class="sxs-lookup"><span data-stu-id="5c59f-147">Version</span></span><br/> | <span data-ttu-id="5c59f-148">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5c59f-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5c59f-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c59f-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="5c59f-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c59f-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c59f-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c59f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c59f-152">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="5c59f-152">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="5c59f-153">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="5c59f-153">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="5c59f-154">**Media. getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="5c59f-154">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="5c59f-155">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="5c59f-155">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="5c59f-156">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="5c59f-156">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="5c59f-157">**Leer valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="5c59f-157">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="5c59f-158">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5c59f-158">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5c59f-159">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5c59f-159">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





