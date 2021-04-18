---
title: MediaCollection. setDeleted, método
description: El método setDeleted mueve el elemento multimedia especificado a la carpeta elementos eliminados. | MediaCollection. setDeleted, método
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- método setDeleted de Windows Media Player
- método setDeleted de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método setDeleted
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690292"
---
# <a name="mediacollectionsetdeleted-method"></a><span data-ttu-id="26727-107">MediaCollection. setDeleted, método</span><span class="sxs-lookup"><span data-stu-id="26727-107">MediaCollection.setDeleted method</span></span>

<span data-ttu-id="26727-108">El método **setDeleted** mueve el elemento multimedia especificado a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="26727-108">The **setDeleted** method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="26727-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26727-109">Syntax</span></span>


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a><span data-ttu-id="26727-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26727-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26727-111">*elemento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="26727-111">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26727-112">Objeto **multimedia** que se está moviendo.</span><span class="sxs-lookup"><span data-stu-id="26727-112">**Media** object being moved.</span></span>

</dd> <dt>

<span data-ttu-id="26727-113">*true* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="26727-113">*true* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26727-114">Especifique siempre este valor.</span><span class="sxs-lookup"><span data-stu-id="26727-114">Always specify this value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26727-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26727-115">Return value</span></span>

<span data-ttu-id="26727-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="26727-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="26727-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="26727-117">Remarks</span></span>

<span data-ttu-id="26727-118">Este método no quita los archivos del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="26727-118">This method does not remove files from the user's computer.</span></span>

<span data-ttu-id="26727-119">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="26727-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="26727-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="26727-120">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="26727-121">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="26727-121">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="26727-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="26727-122">Examples</span></span>

<span data-ttu-id="26727-123">En el siguiente ejemplo de JScript se usa *MediaCollection*. **setDeleted** para trasladar un elemento multimedia determinado, almacenado en la variable denominada mediaObject, a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="26727-123">The following JScript example uses *MediaCollection*.**setDeleted** to move a particular media item, stored in the variable named mediaObject, to the deleted items folder.</span></span> <span data-ttu-id="26727-124">*MediaCollection*. el método **IsDeleted** primero comprueba si el elemento ya se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="26727-124">The *MediaCollection*.**isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="26727-125">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="26727-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="26727-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26727-126">Requirements</span></span>



| <span data-ttu-id="26727-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="26727-127">Requirement</span></span> | <span data-ttu-id="26727-128">Value</span><span class="sxs-lookup"><span data-stu-id="26727-128">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26727-129">Versión</span><span class="sxs-lookup"><span data-stu-id="26727-129">Version</span></span><br/> | <span data-ttu-id="26727-130">Windows Media Player versión 7,0, Windows Media Player versión 7,1 o Windows Media Player para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="26727-130">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="26727-131">Este método no es compatible con Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="26727-131">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="26727-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26727-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="26727-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26727-133"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="26727-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="26727-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26727-135">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="26727-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="26727-136">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="26727-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="26727-137">**MediaCollection. isDeleted**</span><span class="sxs-lookup"><span data-stu-id="26727-137">**MediaCollection.isDeleted**</span></span>](mediacollection-isdeleted.md)
</dt> <dt>

[<span data-ttu-id="26727-138">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="26727-138">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="26727-139">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="26727-139">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





