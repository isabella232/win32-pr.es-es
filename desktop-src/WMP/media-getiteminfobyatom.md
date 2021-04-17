---
title: Método media. getItemInfoByAtom
description: El método getItemInfoByAtom recupera el valor del atributo con el número de índice especificado.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- método getItemInfoByAtom de Windows Media Player
- método getItemInfoByAtom Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getItemInfoByAtom
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700235"
---
# <a name="mediagetiteminfobyatom-method"></a><span data-ttu-id="193ec-106">Método media. getItemInfoByAtom</span><span class="sxs-lookup"><span data-stu-id="193ec-106">Media.getItemInfoByAtom method</span></span>

<span data-ttu-id="193ec-107">El método **getItemInfoByAtom** recupera el valor del atributo con el número de índice especificado.</span><span class="sxs-lookup"><span data-stu-id="193ec-107">The **getItemInfoByAtom** method retrieves the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="193ec-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="193ec-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="193ec-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="193ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="193ec-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="193ec-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="193ec-111">**Número** (**largo**) que especifica el índice en el que un atributo determinado reside en el conjunto de atributos disponibles.</span><span class="sxs-lookup"><span data-stu-id="193ec-111">**Number** (**long**) specifying the index at which a given attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="193ec-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="193ec-112">Return value</span></span>

<span data-ttu-id="193ec-113">Este método devuelve una **cadena** que representa el valor del atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="193ec-113">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="193ec-114">En el caso de los atributos cuyo valor subyacente es **booleano**, devuelve la cadena "true" o "false".</span><span class="sxs-lookup"><span data-stu-id="193ec-114">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="193ec-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="193ec-115">Remarks</span></span>

<span data-ttu-id="193ec-116">Este método se puede utilizar para recuperar los metadatos de un elemento multimedia digital específico mediante un número de índice de atributo.</span><span class="sxs-lookup"><span data-stu-id="193ec-116">This method can be used to retrieve metadata for a specific digital media item by using an attribute index number.</span></span> <span data-ttu-id="193ec-117">La propiedad **attributeCount** se puede utilizar para determinar el número de atributos disponibles para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="193ec-117">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="193ec-118">El método **getMediaAtom** del objeto **MediaCollection** también se puede usar para recuperar el índice de un atributo determinado.</span><span class="sxs-lookup"><span data-stu-id="193ec-118">The **getMediaAtom** method of the **MediaCollection** object can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="193ec-119">Esta técnica suele ser más eficaz que los métodos **getItemInfo** o **getItemInfoByType** al trabajar con listas de reproducción grandes.</span><span class="sxs-lookup"><span data-stu-id="193ec-119">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="193ec-120">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="193ec-120">To use this method, read access to the library is required.</span></span> <span data-ttu-id="193ec-121">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="193ec-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="193ec-122">Para obtener información acerca de los atributos que admite Windows Media Player, vea la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="193ec-122">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="193ec-123">**Windows Media Player 10 Mobile:** Los atributos de un elemento multimedia solo están disponibles durante la reproducción, a menos que se recuperen del elemento a través de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="193ec-123">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="193ec-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="193ec-124">Requirements</span></span>



| <span data-ttu-id="193ec-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="193ec-125">Requirement</span></span> | <span data-ttu-id="193ec-126">Value</span><span class="sxs-lookup"><span data-stu-id="193ec-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="193ec-127">Versión</span><span class="sxs-lookup"><span data-stu-id="193ec-127">Version</span></span><br/> | <span data-ttu-id="193ec-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="193ec-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="193ec-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="193ec-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="193ec-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="193ec-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="193ec-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="193ec-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="193ec-132">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="193ec-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="193ec-133">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="193ec-133">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="193ec-134">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="193ec-134">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="193ec-135">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="193ec-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="193ec-136">**Media. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="193ec-136">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="193ec-137">**MediaCollection.getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="193ec-137">**MediaCollection.getMediaAtom**</span></span>](mediacollection-getmediaatom.md)
</dt> <dt>

[<span data-ttu-id="193ec-138">**Leer valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="193ec-138">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="193ec-139">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="193ec-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="193ec-140">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="193ec-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





