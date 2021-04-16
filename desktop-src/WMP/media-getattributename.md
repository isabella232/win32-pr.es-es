---
title: Método media. getAttributeName
description: El método getAttributeName recupera el nombre del atributo correspondiente al índice especificado.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- método getAttributeName de Windows Media Player
- método getAttributeName Windows Media Player, clase multimedia
- Clase multimedia Windows Media Player, método getAttributeName
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699442"
---
# <a name="mediagetattributename-method"></a><span data-ttu-id="a845e-106">Método media. getAttributeName</span><span class="sxs-lookup"><span data-stu-id="a845e-106">Media.getAttributeName method</span></span>

<span data-ttu-id="a845e-107">El método **getAttributeName** recupera el nombre del atributo correspondiente al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="a845e-107">The **getAttributeName** method retrieves the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a845e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a845e-108">Syntax</span></span>


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="a845e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a845e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a845e-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a845e-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a845e-111">**Número** (**largo**) que contiene el índice del atributo.</span><span class="sxs-lookup"><span data-stu-id="a845e-111">**Number** (**long**) containing the index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a845e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a845e-112">Return value</span></span>

<span data-ttu-id="a845e-113">Este método devuelve una **cadena** que especifica el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="a845e-113">This method returns a **String** specifying the name of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="a845e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a845e-114">Remarks</span></span>

<span data-ttu-id="a845e-115">El nombre de atributo devuelto se puede usar junto con **getItemInfo** para recuperar el valor de un atributo con nombre específico.</span><span class="sxs-lookup"><span data-stu-id="a845e-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="a845e-116">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a845e-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="a845e-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a845e-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="a845e-118">Para obtener información acerca de los atributos que admite Windows Media Player, vea la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a845e-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="a845e-119">**Windows Media Player 10 Mobile:** Los atributos de un elemento multimedia solo están disponibles durante la reproducción, a menos que se recuperen del elemento a través de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="a845e-119">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="a845e-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a845e-120">Examples</span></span>

<span data-ttu-id="a845e-121">En el siguiente ejemplo de JScript se utiliza el *medio*. **getAttributeName** para rellenar un área de texto HTML denominada mi texto con el índice y el nombre de cada atributo del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="a845e-121">The following JScript example uses *Media*.**getAttributeName** to fill an HTML text area named myText with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="a845e-122">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="a845e-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="a845e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a845e-123">Requirements</span></span>



| <span data-ttu-id="a845e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a845e-124">Requirement</span></span> | <span data-ttu-id="a845e-125">Value</span><span class="sxs-lookup"><span data-stu-id="a845e-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a845e-126">Versión</span><span class="sxs-lookup"><span data-stu-id="a845e-126">Version</span></span><br/> | <span data-ttu-id="a845e-127">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="a845e-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a845e-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a845e-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="a845e-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a845e-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a845e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a845e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a845e-131">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="a845e-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="a845e-132">**Media. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="a845e-132">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="a845e-133">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="a845e-133">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="a845e-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a845e-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="a845e-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="a845e-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





