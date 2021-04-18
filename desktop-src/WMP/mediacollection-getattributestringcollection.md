---
title: MediaCollection. getAttributeStringCollection, método
description: El método getAttributeStringCollection recupera un objeto StringCollection que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- método getAttributeStringCollection de Windows Media Player
- método getAttributeStringCollection de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getAttributeStringCollection
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690638"
---
# <a name="mediacollectiongetattributestringcollection-method"></a><span data-ttu-id="f5196-106">MediaCollection. getAttributeStringCollection, método</span><span class="sxs-lookup"><span data-stu-id="f5196-106">MediaCollection.getAttributeStringCollection method</span></span>

<span data-ttu-id="f5196-107">El método **getAttributeStringCollection** recupera un objeto **StringCollection** que representa el conjunto de todos los valores de un atributo especificado dentro de un tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="f5196-107">The **getAttributeStringCollection** method retrieves a **StringCollection** object representing the set of all values for a specified attribute within a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5196-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5196-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="f5196-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5196-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5196-110">*atributo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f5196-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5196-111">**Cadena** que especifica el atributo.</span><span class="sxs-lookup"><span data-stu-id="f5196-111">**String** specifying the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="f5196-112">*mediaType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f5196-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5196-113">**Cadena** que representa el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="f5196-113">**String** representing the media type.</span></span> <span data-ttu-id="f5196-114">Contiene uno de los siguientes valores: "audio", "vídeo", "lista de reproducción" u "otro".</span><span class="sxs-lookup"><span data-stu-id="f5196-114">Contains one of the following values: "Audio", "Video", "Playlist", or "Other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5196-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5196-115">Return value</span></span>

<span data-ttu-id="f5196-116">Este método devuelve un objeto **StringCollection** .</span><span class="sxs-lookup"><span data-stu-id="f5196-116">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5196-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5196-117">Remarks</span></span>

<span data-ttu-id="f5196-118">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f5196-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="f5196-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="f5196-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="f5196-120">Para obtener información sobre los atributos que admite Windows Media Player, consulte la sección [referencia de atributos](attribute-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="f5196-120">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md) section.</span></span>

## <a name="examples"></a><span data-ttu-id="f5196-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f5196-121">Examples</span></span>

<span data-ttu-id="f5196-122">En el siguiente ejemplo de JScript se usa *MediaCollection*. **getAttributeStringCollection** para mostrar una lista de valores que corresponden a un atributo determinado para los elementos de audio de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="f5196-122">The following JScript example uses *MediaCollection*.**getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="f5196-123">Un elemento SELECT de HTML, creado con ID = "Attribute", permite al usuario seleccionar un atributo, como artista, género o álbum.</span><span class="sxs-lookup"><span data-stu-id="f5196-123">An HTML SELECT element, created with ID = "Attribute", allows the user to select an attribute, such as Artist, Genre, or Album.</span></span> <span data-ttu-id="f5196-124">Un elemento TEXTAREA HTML, creado con ID = "AttributeVals", muestra el resultado.</span><span class="sxs-lookup"><span data-stu-id="f5196-124">An HTML TEXTAREA element, created with ID = "AttributeVals", displays the result.</span></span> <span data-ttu-id="f5196-125">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f5196-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="f5196-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5196-126">Requirements</span></span>



| <span data-ttu-id="f5196-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5196-127">Requirement</span></span> | <span data-ttu-id="f5196-128">Value</span><span class="sxs-lookup"><span data-stu-id="f5196-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f5196-129">Versión</span><span class="sxs-lookup"><span data-stu-id="f5196-129">Version</span></span><br/> | <span data-ttu-id="f5196-130">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="f5196-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f5196-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5196-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="f5196-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5196-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5196-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5196-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5196-134">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="f5196-134">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="f5196-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f5196-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f5196-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="f5196-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="f5196-137">**StringCollection (objeto)**</span><span class="sxs-lookup"><span data-stu-id="f5196-137">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





