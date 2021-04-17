---
title: MediaCollection. isDeleted (método)
description: El método isDeleted recupera un valor que indica si el elemento multimedia especificado se encuentra en la carpeta elementos eliminados.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- método isDeleted Windows Media Player
- método isDeleted Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método isDeleted
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690294"
---
# <a name="mediacollectionisdeleted-method"></a><span data-ttu-id="7e9ca-106">MediaCollection. isDeleted (método)</span><span class="sxs-lookup"><span data-stu-id="7e9ca-106">MediaCollection.isDeleted method</span></span>

<span data-ttu-id="7e9ca-107">El método **IsDeleted** recupera un valor que indica si el elemento multimedia especificado se encuentra en la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="7e9ca-107">The **isDeleted** method retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e9ca-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e9ca-108">Syntax</span></span>


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a><span data-ttu-id="7e9ca-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e9ca-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e9ca-110">*elemento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7e9ca-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e9ca-111">Objeto **multimedia** que se puede eliminar.</span><span class="sxs-lookup"><span data-stu-id="7e9ca-111">**Media** object that might be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e9ca-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e9ca-112">Return value</span></span>

<span data-ttu-id="7e9ca-113">Este método devuelve un **valor booleano**.</span><span class="sxs-lookup"><span data-stu-id="7e9ca-113">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e9ca-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e9ca-114">Remarks</span></span>

<span data-ttu-id="7e9ca-115">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7e9ca-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7e9ca-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="7e9ca-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7e9ca-117">**Windows Media Player 10 Mobile:** Este método siempre devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="7e9ca-117">**Windows Media Player 10 Mobile:** This method always returns **false**.</span></span>

## <a name="examples"></a><span data-ttu-id="7e9ca-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7e9ca-118">Examples</span></span>

<span data-ttu-id="7e9ca-119">En el siguiente ejemplo de JScript se usa *MediaCollection*. **IsDeleted** para probar si un elemento multimedia determinado, almacenado en la variable denominada mediaObject, se encuentra en la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="7e9ca-119">The following JScript example uses *MediaCollection*.**isDeleted** to test whether a particular media item, stored in the variable named mediaObject, is in the deleted items folder.</span></span> <span data-ttu-id="7e9ca-120">Si el elemento multimedia no se ha eliminado ya, se mueve a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="7e9ca-120">If the media item has not been deleted already, it is moved to the deleted items folder.</span></span> <span data-ttu-id="7e9ca-121">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="7e9ca-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a><span data-ttu-id="7e9ca-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e9ca-122">Requirements</span></span>



| <span data-ttu-id="7e9ca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e9ca-123">Requirement</span></span> | <span data-ttu-id="7e9ca-124">Value</span><span class="sxs-lookup"><span data-stu-id="7e9ca-124">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e9ca-125">Versión</span><span class="sxs-lookup"><span data-stu-id="7e9ca-125">Version</span></span><br/> | <span data-ttu-id="7e9ca-126">Windows Media Player versión 7,0, Windows Media Player versión 7,1 o Windows Media Player para Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7e9ca-126">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="7e9ca-127">Este método no es compatible con Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="7e9ca-127">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="7e9ca-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e9ca-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="7e9ca-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e9ca-129"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="7e9ca-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e9ca-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e9ca-131">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="7e9ca-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7e9ca-132">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="7e9ca-132">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="7e9ca-133">**MediaCollection.setDeleted**</span><span class="sxs-lookup"><span data-stu-id="7e9ca-133">**MediaCollection.setDeleted**</span></span>](mediacollection-setdeleted.md)
</dt> <dt>

[<span data-ttu-id="7e9ca-134">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7e9ca-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7e9ca-135">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7e9ca-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





