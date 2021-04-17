---
title: IWMPPlaylist. Item (VB y C)
description: La propiedad Item (el \_ método get item en C \) obtiene una interfaz para el elemento multimedia en el índice especificado.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- IWMPPlaylist. Item (VB y C) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689958"
---
# <a name="iwmpplaylistitem-vb-and-c"></a><span data-ttu-id="56020-104">IWMPPlaylist. Item (VB y C#)</span><span class="sxs-lookup"><span data-stu-id="56020-104">IWMPPlaylist.Item (VB and C#)</span></span>

<span data-ttu-id="56020-105">La propiedad **Item** (el método **Get \_ Item** en C#) obtiene una interfaz para el elemento multimedia en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="56020-105">The **Item** property (the **get\_Item** method in C#) gets an interface to the media item at the specified index.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a><span data-ttu-id="56020-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56020-106">Parameters</span></span>

<span data-ttu-id="56020-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="56020-107">*lIndex*</span></span>

<span data-ttu-id="56020-108">**System. Int32** que es el índice del elemento multimedia de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="56020-108">A **System.Int32** that is the index of the media item in the playlist.</span></span>

## <a name="property-value"></a><span data-ttu-id="56020-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="56020-109">Property Value</span></span>

<span data-ttu-id="56020-110">Una interfaz **WMPLib. IWMPMedia** que proporciona acceso al elemento multimedia en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="56020-110">An **WMPLib.IWMPMedia** interface that provides access to the media item at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="56020-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56020-111">Remarks</span></span>

<span data-ttu-id="56020-112">**IWMPPlaylist. Item** es una propiedad de solo lectura en Visual Basic que toma un parámetro, mientras que en C# se conoce como el método **IWMPPlaylist. Get \_ Item** .</span><span class="sxs-lookup"><span data-stu-id="56020-112">**IWMPPlaylist.Item** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_Item** method.</span></span>

## <a name="examples"></a><span data-ttu-id="56020-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56020-113">Examples</span></span>

<span data-ttu-id="56020-114">En el ejemplo siguiente se usa la propiedad **Item** (el método **Get \_ Item** en C#) para recuperar un elemento multimedia de una lista de reproducción basada en una selección de usuario.</span><span class="sxs-lookup"><span data-stu-id="56020-114">The following example uses the **Item** property (the **get\_Item** method in C#) to retrieve a media item from a playlist based on a user selection.</span></span> <span data-ttu-id="56020-115">Se ha creado un cuadro de lista con el nombre weblist y se han rellenado con los títulos de la lista de reproducción denominada audioPlaylist.</span><span class="sxs-lookup"><span data-stu-id="56020-115">A list box was created with the name weblist, and filled with the titles from the playlist called audioPlaylist.</span></span> <span data-ttu-id="56020-116">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="56020-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

End Sub
```





## <a name="requirements"></a><span data-ttu-id="56020-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56020-117">Requirements</span></span>



| <span data-ttu-id="56020-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="56020-118">Requirement</span></span> | <span data-ttu-id="56020-119">Value</span><span class="sxs-lookup"><span data-stu-id="56020-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56020-120">Versión</span><span class="sxs-lookup"><span data-stu-id="56020-120">Version</span></span><br/>   | <span data-ttu-id="56020-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="56020-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="56020-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56020-122">Namespace</span></span><br/> | <span data-ttu-id="56020-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="56020-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="56020-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="56020-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="56020-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="56020-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56020-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="56020-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56020-127">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="56020-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56020-128">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="56020-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56020-129">**IWMPPlaylist. insertItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="56020-129">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56020-130">**IWMPPlaylist. removeItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="56020-130">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56020-131">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="56020-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="56020-132">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="56020-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





