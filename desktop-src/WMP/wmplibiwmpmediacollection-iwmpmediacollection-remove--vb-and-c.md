---
title: IWMPMediaCollection Remove (método)
description: El método Remove quita un elemento especificado de la colección de medios.
ms.assetid: 2ed45159-0a92-4353-8bf1-1d20de404bf7
keywords:
- quitar Media Player de Windows de método
- quitar método Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, Remove (método)
topic_type:
- apiref
api_name:
- IWMPMediaCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d341f8974255dab5e3cdce356a9b221eddff193c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700335"
---
# <a name="iwmpmediacollectionremove-method"></a><span data-ttu-id="77bed-106">IWMPMediaCollection:: Remove (método)</span><span class="sxs-lookup"><span data-stu-id="77bed-106">IWMPMediaCollection::remove method</span></span>

<span data-ttu-id="77bed-107">El `remove` método quita un elemento especificado de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="77bed-107">The `remove` method removes a specified item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="77bed-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="77bed-108">Syntax</span></span>


```CSharp
public void remove(
  IWMPMedia pItem,
  System.Boolean varfDeleteFile
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPMedia, _
  ByVal varfDeleteFile As System.Boolean _
)
Implements IWMPMediaCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="77bed-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="77bed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77bed-110">*pItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77bed-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77bed-111">Una interfaz **WMPLib. IWMPMedia** que identifica el elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="77bed-111">A **WMPLib.IWMPMedia** interface that identifies the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="77bed-112">*varfDeleteFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="77bed-112">*varfDeleteFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77bed-113">Valor **System. Boolean** que especifica si el método debe quitar el elemento especificado de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="77bed-113">A **System.Boolean** value that specifies whether the method should remove the specified item from the library.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77bed-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="77bed-114">Return value</span></span>

<span data-ttu-id="77bed-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="77bed-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="77bed-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="77bed-116">Remarks</span></span>

<span data-ttu-id="77bed-117">Este método elimina un elemento de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="77bed-117">This method deletes an item from the library.</span></span> <span data-ttu-id="77bed-118">Este método no elimina archivos del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="77bed-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="77bed-119">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="77bed-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="77bed-120">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="77bed-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="77bed-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="77bed-121">Examples</span></span>

<span data-ttu-id="77bed-122">En el ejemplo siguiente, después de solicitar al usuario, se elimina de forma permanente el primer elemento multimedia de la colección de medios mediante `remove` .</span><span class="sxs-lookup"><span data-stu-id="77bed-122">The following example, after prompting the user, permanently deletes the first media item in the media collection by using `remove`.</span></span> <span data-ttu-id="77bed-123">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="77bed-123">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first item from the media collection. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Store the name of the retrieved media item.
string mediaName = media.name;

// Prepare a message, a caption and buttons for the user prompt.
string message = ("OK to permanently delete " + mediaName + "?");
string caption = "Confirm deletion";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.OKCancel;

// Prompt the user for permission to delete the object.
System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

// Check the user response.
if (result == System.Windows.Forms.DialogResult.OK)
{
    // Permanently delete the item.
    player.mediaCollection.remove(media, true);

    // Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show("Deleted item " + mediaName);
}
```


```VB

' Get an interface to the first item from the media collection. 
Dim media As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Store the name of the retrieved media item.
Dim mediaName As String = media.name

&#39; Prepare a message, a caption and buttons for the user prompt.
Dim message As String = (&quot;OK to permanently delete &quot; + mediaName + &quot;?&quot;)
Dim caption As String = &quot;Confirm deletion&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.OKCancel

&#39; Prompt the user for permission to delete the object.
Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

&#39; Check the user response.
If (result = System.Windows.Forms.DialogResult.OK) Then

    &#39; Permanently delete the item.
    player.mediaCollection.remove(media, True)

    &#39; Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show(&quot;Deleted item &quot; + mediaName)

End If
```





## <a name="requirements"></a><span data-ttu-id="77bed-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77bed-124">Requirements</span></span>



| <span data-ttu-id="77bed-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="77bed-125">Requirement</span></span> | <span data-ttu-id="77bed-126">Value</span><span class="sxs-lookup"><span data-stu-id="77bed-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77bed-127">Versión</span><span class="sxs-lookup"><span data-stu-id="77bed-127">Version</span></span><br/>   | <span data-ttu-id="77bed-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="77bed-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="77bed-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="77bed-129">Namespace</span></span><br/> | <span data-ttu-id="77bed-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="77bed-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="77bed-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="77bed-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="77bed-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="77bed-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77bed-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="77bed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77bed-134">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="77bed-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77bed-135">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="77bed-135">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="77bed-136">**IWMPMediaCollection. Add (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="77bed-136">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> </dl>

 

 





