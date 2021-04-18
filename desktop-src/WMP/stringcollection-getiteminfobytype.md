---
title: StringCollection. getItemInfoByType (método)
description: El método getItemInfoByType recupera el valor correspondiente al índice de la StringCollection, el nombre, el idioma y el índice de atributo especificados.
ms.assetid: 32a25c69-9399-4857-84c1-143c529be58f
keywords:
- método getItemInfoByType de Windows Media Player
- método getItemInfoByType Windows Media Player, StringCollection (clase)
- Clase StringCollection Windows Media Player, método getItemInfoByType
topic_type:
- apiref
api_name:
- StringCollection.getItemInfoByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b3aa8c5bc367095765f24f19f107dd7cb986ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718705"
---
# <a name="stringcollectiongetiteminfobytype-method"></a><span data-ttu-id="1aab7-106">StringCollection. getItemInfoByType (método)</span><span class="sxs-lookup"><span data-stu-id="1aab7-106">StringCollection.getItemInfoByType method</span></span>

<span data-ttu-id="1aab7-107">El método **getItemInfoByType** recupera el valor correspondiente al índice de la **StringCollection** , el nombre, el idioma y el índice de atributo especificados.</span><span class="sxs-lookup"><span data-stu-id="1aab7-107">The **getItemInfoByType** method retrieves the value corresponding to the specified **StringCollection** index, name, language, and attribute index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1aab7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1aab7-108">Syntax</span></span>


```JScript
retVal = StringCollection.getItemInfoByType(
  index,
  name,
  language,
  attributeIndex
)
```



## <a name="parameters"></a><span data-ttu-id="1aab7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1aab7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1aab7-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1aab7-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aab7-111">**Número** (**Long**) que especifica el índice de base cero del elemento **StringCollection** del que se va a obtener el atributo.</span><span class="sxs-lookup"><span data-stu-id="1aab7-111">**Number** (**long**) specifying the zero-based index of the **StringCollection** item from which to get the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="1aab7-112">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1aab7-112">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aab7-113">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="1aab7-113">**String** containing the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="1aab7-114">*idioma* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1aab7-114">*language* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aab7-115">**Cadena** que contiene el idioma.</span><span class="sxs-lookup"><span data-stu-id="1aab7-115">**String** containing the language.</span></span> <span data-ttu-id="1aab7-116">Si el valor se establece en null o en una cadena vacía (""), se usa la cadena de configuración regional actual.</span><span class="sxs-lookup"><span data-stu-id="1aab7-116">If the value is set to null or the empty string ("") the current locale string is used.</span></span> <span data-ttu-id="1aab7-117">De lo contrario, el valor debe ser una cadena de idioma RFC 1766 válida, como "en-US".</span><span class="sxs-lookup"><span data-stu-id="1aab7-117">Otherwise, the value must be a valid RFC 1766 language string such as "en-us".</span></span>

</dd> <dt>

<span data-ttu-id="1aab7-118">*attributeIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1aab7-118">*attributeIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1aab7-119">**Número** (**largo**) que contiene el índice de base cero del valor que se va a recuperar del atributo.</span><span class="sxs-lookup"><span data-stu-id="1aab7-119">**Number** (**long**) containing the zero-based index of the value to retrieve from the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1aab7-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1aab7-120">Return value</span></span>

<span data-ttu-id="1aab7-121">Este método devuelve un **número**, una **cadena**, un objeto **MetadataPicture** o un objeto **MetadataText** , como se indica en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1aab7-121">This method returns a **Number**, **String**, **MetadataPicture** object, or **MetadataText** object as indicated in the following table.</span></span>



| <span data-ttu-id="1aab7-122">Atributo</span><span class="sxs-lookup"><span data-stu-id="1aab7-122">Attribute</span></span>                   | <span data-ttu-id="1aab7-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1aab7-123">Return value</span></span>                   |
|-----------------------------|--------------------------------|
| <span data-ttu-id="1aab7-124">**SyncState**</span><span class="sxs-lookup"><span data-stu-id="1aab7-124">**SyncState**</span></span>               | <span data-ttu-id="1aab7-125">**Número** (**unsigned Long**)</span><span class="sxs-lookup"><span data-stu-id="1aab7-125">**Number** (**unsigned long**)</span></span> |
| <span data-ttu-id="1aab7-126">**WM/Letras \_ sincronizadas**</span><span class="sxs-lookup"><span data-stu-id="1aab7-126">**WM/Lyrics\_Synchronised**</span></span> | <span data-ttu-id="1aab7-127">Objeto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="1aab7-127">**MetadataText** object</span></span>        |
| <span data-ttu-id="1aab7-128">**WM/imagen**</span><span class="sxs-lookup"><span data-stu-id="1aab7-128">**WM/Picture**</span></span>              | <span data-ttu-id="1aab7-129">Objeto **MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="1aab7-129">**MetadataPicture** object</span></span>     |
| <span data-ttu-id="1aab7-130">**WM/UserWebURL**</span><span class="sxs-lookup"><span data-stu-id="1aab7-130">**WM/UserWebURL**</span></span>           | <span data-ttu-id="1aab7-131">Objeto **MetadataText**</span><span class="sxs-lookup"><span data-stu-id="1aab7-131">**MetadataText** object</span></span>        |
| <span data-ttu-id="1aab7-132">Resto de atributos</span><span class="sxs-lookup"><span data-stu-id="1aab7-132">All other attributes</span></span>        | <span data-ttu-id="1aab7-133">String</span><span class="sxs-lookup"><span data-stu-id="1aab7-133">String</span></span>                         |



 

<span data-ttu-id="1aab7-134">En el caso de los atributos cuyo valor subyacente es **booleano**, este método devuelve la cadena "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="1aab7-134">For attributes whose underlying value is **Boolean**, this method returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="1aab7-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1aab7-135">Remarks</span></span>

<span data-ttu-id="1aab7-136">Este método admite atributos con varios valores y atributos con valores complejos.</span><span class="sxs-lookup"><span data-stu-id="1aab7-136">This method supports attributes with multiple values, and attributes with complex values.</span></span> <span data-ttu-id="1aab7-137">El método **getItemInfo** no admite atributos con valores múltiples o complejos.</span><span class="sxs-lookup"><span data-stu-id="1aab7-137">The **getItemInfo** method does not support attributes with multiple or complex values.</span></span>

<span data-ttu-id="1aab7-138">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1aab7-138">To use this method, read access to the library is required.</span></span> <span data-ttu-id="1aab7-139">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1aab7-139">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1aab7-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1aab7-140">Requirements</span></span>



| <span data-ttu-id="1aab7-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1aab7-141">Requirement</span></span> | <span data-ttu-id="1aab7-142">Value</span><span class="sxs-lookup"><span data-stu-id="1aab7-142">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1aab7-143">Versión</span><span class="sxs-lookup"><span data-stu-id="1aab7-143">Version</span></span><br/> | <span data-ttu-id="1aab7-144">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="1aab7-144">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="1aab7-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1aab7-145">DLL</span></span><br/>     | <dl> <span data-ttu-id="1aab7-146"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1aab7-146"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aab7-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="1aab7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aab7-148">**Objeto MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="1aab7-148">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
</dt> <dt>

[<span data-ttu-id="1aab7-149">**Objeto MetadataText**</span><span class="sxs-lookup"><span data-stu-id="1aab7-149">**MetadataText Object**</span></span>](metadatatext-object.md)
</dt> <dt>

[<span data-ttu-id="1aab7-150">**StringCollection. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1aab7-150">**StringCollection.getItemInfo**</span></span>](stringcollection-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1aab7-151">**StringCollection (objeto)**</span><span class="sxs-lookup"><span data-stu-id="1aab7-151">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





