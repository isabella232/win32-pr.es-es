---
title: IWMPControls currentItem (propiedad)
description: La propiedad currentItem obtiene o establece el elemento multimedia actual en una lista de reproducción.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- propiedad currentItem Media Player de Windows
- propiedad currentItem Windows Media Player, interfaz IWMPControls
- Interfaz IWMPControls Windows Media Player, propiedad currentItem
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690891"
---
# <a name="iwmpcontrolscurrentitem-property"></a><span data-ttu-id="9d020-106">IWMPControls:: currentItem (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9d020-106">IWMPControls::currentItem property</span></span>

<span data-ttu-id="9d020-107">La propiedad **CurrentItem** obtiene o establece el elemento multimedia actual en una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9d020-107">The **currentItem** property gets or sets the current media item in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d020-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d020-108">Syntax</span></span>


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="9d020-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9d020-109">Property value</span></span>

<span data-ttu-id="9d020-110">Una interfaz **WMPLib. IWMPMedia** que representa el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="9d020-110">A **WMPLib.IWMPMedia** interface that represents the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d020-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9d020-111">Remarks</span></span>

<span data-ttu-id="9d020-112">Esta propiedad solo funciona con los elementos de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="9d020-112">This property works only with items in the current playlist.</span></span> <span data-ttu-id="9d020-113">No se admite el establecimiento de **CurrentItem** en la interfaz de un elemento multimedia guardado.</span><span class="sxs-lookup"><span data-stu-id="9d020-113">Setting **currentItem** to the interface of a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="9d020-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9d020-114">Examples</span></span>

<span data-ttu-id="9d020-115">En el ejemplo siguiente se usa **CurrentItem** para establecer el elemento multimedia actual del reproductor en un elemento seleccionado en un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="9d020-115">The following example uses **currentItem** to set the player's current media item to an item selected from a list box.</span></span> <span data-ttu-id="9d020-116">El cuadro de lista se ha rellenado con todos los elementos de la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="9d020-116">The list box has been filled with all of the items in the current playlist.</span></span> <span data-ttu-id="9d020-117">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="9d020-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="9d020-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d020-118">Requirements</span></span>



| <span data-ttu-id="9d020-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d020-119">Requirement</span></span> | <span data-ttu-id="9d020-120">Value</span><span class="sxs-lookup"><span data-stu-id="9d020-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d020-121">Versión</span><span class="sxs-lookup"><span data-stu-id="9d020-121">Version</span></span><br/>   | <span data-ttu-id="9d020-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="9d020-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="9d020-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9d020-123">Namespace</span></span><br/> | <span data-ttu-id="9d020-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="9d020-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="9d020-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="9d020-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9d020-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9d020-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d020-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="9d020-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d020-128">**IWMPControlsInterface (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9d020-128">**IWMPControlsInterface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9d020-129">**IWMPMediaInterface (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9d020-129">**IWMPMediaInterface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9d020-130">**IWMPPlaylistCollection. getByName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="9d020-130">**IWMPPlaylistCollection.getByName(VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





