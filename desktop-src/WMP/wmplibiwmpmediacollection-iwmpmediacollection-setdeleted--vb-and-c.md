---
title: IWMPMediaCollection setDeleted, método
description: El método setDeleted mueve el elemento multimedia especificado a la carpeta elementos eliminados. | IWMPMediaCollection setDeleted, método
ms.assetid: 3fa7989e-8b98-44e1-93ca-8136aba358ea
keywords:
- método setDeleted de Windows Media Player
- método setDeleted Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método setDeleted
topic_type:
- apiref
api_name:
- IWMPMediaCollection.setDeleted
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ccf8cf2d36ab7e4aaf76fdbe5c28582650fcda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700334"
---
# <a name="iwmpmediacollectionsetdeleted-method"></a><span data-ttu-id="88ce7-107">IWMPMediaCollection:: setDeleted (método)</span><span class="sxs-lookup"><span data-stu-id="88ce7-107">IWMPMediaCollection::setDeleted method</span></span>

<span data-ttu-id="88ce7-108">El `setDeleted` método mueve el elemento multimedia especificado a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="88ce7-108">The `setDeleted` method moves the specified media item to the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ce7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88ce7-109">Syntax</span></span>


```CSharp
public void setDeleted(
  IWMPMedia pItem,
  System.Boolean varfIsDeleted
);
```


```VB

Public Sub setDeleted( _
  ByVal pItem As IWMPMedia, _
  ByVal varfIsDeleted As System.Boolean _
)
Implements IWMPMediaCollection.setDeleted
```





## <a name="parameters"></a><span data-ttu-id="88ce7-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="88ce7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88ce7-111">*pItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88ce7-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88ce7-112">Una interfaz **WMPLib. IWMPMedia** para el elemento que se va a desplace.</span><span class="sxs-lookup"><span data-stu-id="88ce7-112">A **WMPLib.IWMPMedia** interface for the item to be moved.</span></span>

</dd> <dt>

<span data-ttu-id="88ce7-113">*varfIsDeleted* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="88ce7-113">*varfIsDeleted* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88ce7-114">Valor **System. Boolean** que especifica si el elemento debe moverse a la carpeta de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="88ce7-114">A **System.Boolean** value that specifies whether the item should be moved to the deleted items folder.</span></span> <span data-ttu-id="88ce7-115">Este valor siempre debe ser **true**.</span><span class="sxs-lookup"><span data-stu-id="88ce7-115">This value must always be **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88ce7-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="88ce7-116">Return value</span></span>

<span data-ttu-id="88ce7-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="88ce7-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ce7-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88ce7-118">Remarks</span></span>

<span data-ttu-id="88ce7-119">Este método no quita los archivos del equipo del usuario, simplemente los mueve a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="88ce7-119">This method does not remove files from the user's computer, it just moves them to the deleted items folder.</span></span>

<span data-ttu-id="88ce7-120">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="88ce7-120">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="88ce7-121">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="88ce7-121">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="88ce7-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="88ce7-122">Examples</span></span>

<span data-ttu-id="88ce7-123">En el ejemplo siguiente `setDeleted` se usa para trasladar un elemento multimedia determinado a la carpeta elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="88ce7-123">The following example uses `setDeleted` to move a particular media item to the deleted items folder.</span></span> <span data-ttu-id="88ce7-124">El método **IsDeleted** comprueba primero si el elemento ya se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="88ce7-124">The **isDeleted** method first tests whether the item has already been deleted.</span></span> <span data-ttu-id="88ce7-125">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="88ce7-125">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Test whether the media item has already been deleted.
if (!player.mediaCollection.isDeleted(media))
{
    // The item is available to be deleted; move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, true);

    // Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show("Item moved to deleted items folder.");
}
else
{
    // Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show("Item is already deleted!");
}
```


```VB

' Test whether the media item has already been deleted.
If (Not player.mediaCollection.isDeleted(media)) Then

    &#39; The item is available to be deleted move it to the deleted items folder.
    player.mediaCollection.setDeleted(media, True)

    &#39; Inform the user that the operation succeeded.
    System.Windows.Forms.MessageBox.Show(&quot;Item moved to deleted items folder.&quot;)

Else

    &#39; Tell the user the operation is unnecessary.
    System.Windows.Forms.MessageBox.Show(&quot;Item is already deleted!&quot;)

End If
```





## <a name="requirements"></a><span data-ttu-id="88ce7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88ce7-126">Requirements</span></span>



| <span data-ttu-id="88ce7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="88ce7-127">Requirement</span></span> | <span data-ttu-id="88ce7-128">Value</span><span class="sxs-lookup"><span data-stu-id="88ce7-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ce7-129">Versión</span><span class="sxs-lookup"><span data-stu-id="88ce7-129">Version</span></span><br/>   | <span data-ttu-id="88ce7-130">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="88ce7-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="88ce7-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="88ce7-131">Namespace</span></span><br/> | <span data-ttu-id="88ce7-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="88ce7-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="88ce7-133">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="88ce7-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="88ce7-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="88ce7-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88ce7-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="88ce7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88ce7-136">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="88ce7-136">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="88ce7-137">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="88ce7-137">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





