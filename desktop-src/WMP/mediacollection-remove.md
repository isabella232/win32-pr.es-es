---
title: MediaCollection. Remove (método)
description: El método Remove quita un elemento de la colección de medios.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- quitar Media Player de Windows de método
- método Remove Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, Remove (método)
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690293"
---
# <a name="mediacollectionremove-method"></a><span data-ttu-id="eeddd-106">MediaCollection. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="eeddd-106">MediaCollection.remove method</span></span>

<span data-ttu-id="eeddd-107">El método **Remove** quita un elemento de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="eeddd-107">The **remove** method removes an item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeddd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eeddd-108">Syntax</span></span>


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a><span data-ttu-id="eeddd-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eeddd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eeddd-110">*elemento* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="eeddd-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeddd-111">Objeto **multimedia** que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="eeddd-111">**Media** object to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="eeddd-112">*eliminar* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="eeddd-112">*delete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eeddd-113">**Valor booleano** que indica si se va a quitar el elemento.</span><span class="sxs-lookup"><span data-stu-id="eeddd-113">**Boolean** indicating whether to remove the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eeddd-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eeddd-114">Return value</span></span>

<span data-ttu-id="eeddd-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="eeddd-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eeddd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eeddd-116">Remarks</span></span>

<span data-ttu-id="eeddd-117">Este método elimina un elemento de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="eeddd-117">This method deletes an item from the library.</span></span> <span data-ttu-id="eeddd-118">Este método no elimina archivos del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="eeddd-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="eeddd-119">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="eeddd-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="eeddd-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="eeddd-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="eeddd-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="eeddd-121">Examples</span></span>

<span data-ttu-id="eeddd-122">En el siguiente ejemplo de JScript, después de solicitar al usuario, se elimina de forma permanente el primer elemento multimedia de la colección de medios mediante *MediaCollection*. **quitar**.</span><span class="sxs-lookup"><span data-stu-id="eeddd-122">The following JScript example, after prompting the user, permanently deletes the first media item in the media collection by using *MediaCollection*.**remove**.</span></span> <span data-ttu-id="eeddd-123">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="eeddd-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a><span data-ttu-id="eeddd-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eeddd-124">Requirements</span></span>



| <span data-ttu-id="eeddd-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeddd-125">Requirement</span></span> | <span data-ttu-id="eeddd-126">Value</span><span class="sxs-lookup"><span data-stu-id="eeddd-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eeddd-127">Versión</span><span class="sxs-lookup"><span data-stu-id="eeddd-127">Version</span></span><br/> | <span data-ttu-id="eeddd-128">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="eeddd-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="eeddd-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eeddd-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="eeddd-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeddd-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeddd-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="eeddd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeddd-132">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="eeddd-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="eeddd-133">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="eeddd-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="eeddd-134">**MediaCollection. Add**</span><span class="sxs-lookup"><span data-stu-id="eeddd-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="eeddd-135">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="eeddd-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="eeddd-136">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="eeddd-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





