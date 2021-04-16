---
title: Media. attributeCount
description: La propiedad attributeCount recupera el número de atributos que se pueden consultar o establecer para el elemento multimedia.
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- Media Player Windows Media. attributeCount
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709099"
---
# <a name="mediaattributecount"></a><span data-ttu-id="e5a63-104">Media. attributeCount</span><span class="sxs-lookup"><span data-stu-id="e5a63-104">Media.attributeCount</span></span>

<span data-ttu-id="e5a63-105">La propiedad **attributeCount** recupera el número de atributos que se pueden consultar o establecer para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="e5a63-105">The **attributeCount** property retrieves the number of attributes that can be queried and/or set for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5a63-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e5a63-106">Syntax</span></span>

<span data-ttu-id="e5a63-107">*reproductor*. *currentMedia*. **attributeCount**</span><span class="sxs-lookup"><span data-stu-id="e5a63-107">*player*.*currentMedia*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="e5a63-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="e5a63-108">Possible Values</span></span>

<span data-ttu-id="e5a63-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="e5a63-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="e5a63-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5a63-110">Remarks</span></span>

<span data-ttu-id="e5a63-111">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e5a63-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="e5a63-112">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e5a63-112">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="e5a63-113">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e5a63-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="e5a63-114">**Windows Media Player 10 Mobile:** Los atributos de un elemento multimedia solo están disponibles durante la reproducción, a menos que se recuperen del elemento a través de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="e5a63-114">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="e5a63-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e5a63-115">Examples</span></span>

<span data-ttu-id="e5a63-116">En el siguiente ejemplo de JScript se utiliza el *medio*. **attributeCount** para determinar el número de atributos disponibles en el elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="e5a63-116">The following JScript example uses *Media*.**attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="e5a63-117">El código utiliza ese valor para imprimir una lista de nombres de atributo y valores en un área de texto HTML, denominada mi texto.</span><span class="sxs-lookup"><span data-stu-id="e5a63-117">The code uses that value to print a list of attribute names and values in an HTML text area, named myText.</span></span> <span data-ttu-id="e5a63-118">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="e5a63-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="e5a63-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5a63-119">Requirements</span></span>



| <span data-ttu-id="e5a63-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5a63-120">Requirement</span></span> | <span data-ttu-id="e5a63-121">Value</span><span class="sxs-lookup"><span data-stu-id="e5a63-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e5a63-122">Versión</span><span class="sxs-lookup"><span data-stu-id="e5a63-122">Version</span></span><br/> | <span data-ttu-id="e5a63-123">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e5a63-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e5a63-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e5a63-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="e5a63-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5a63-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5a63-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5a63-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5a63-127">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="e5a63-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e5a63-128">**Media. getAttributeName**</span><span class="sxs-lookup"><span data-stu-id="e5a63-128">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="e5a63-129">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="e5a63-129">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="e5a63-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e5a63-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e5a63-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e5a63-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





