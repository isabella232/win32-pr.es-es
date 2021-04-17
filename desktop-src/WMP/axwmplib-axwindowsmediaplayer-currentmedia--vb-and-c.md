---
title: Propiedad AxWindowsMediaPlayer. currentMedia
description: La propiedad currentMedia obtiene o establece la interfaz IWMPMedia que corresponde al elemento multimedia actual.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- propiedades de currentMedia Media Player de Windows
- propiedad currentMedia Media Player de Windows, clase AxWindowsMediaPlayer
- Clase AxWindowsMediaPlayer Windows Media Player, propiedad currentMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700090"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a><span data-ttu-id="c5de4-106">Propiedad AxWindowsMediaPlayer. currentMedia</span><span class="sxs-lookup"><span data-stu-id="c5de4-106">AxWindowsMediaPlayer.currentMedia property</span></span>

<span data-ttu-id="c5de4-107">La propiedad currentMedia obtiene o establece la interfaz IWMPMedia que corresponde al elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="c5de4-107">The currentMedia property gets or sets the IWMPMedia interface that corresponds to the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5de4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5de4-108">Syntax</span></span>


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="c5de4-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c5de4-109">Property value</span></span>

<span data-ttu-id="c5de4-110">La interfaz WMPLib. IWMPMedia que proporciona acceso al elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="c5de4-110">The WMPLib.IWMPMedia interface that provides access to the current media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5de4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5de4-111">Remarks</span></span>

<span data-ttu-id="c5de4-112">Si AxWindowsMediaPlayer. Settings. la propiedad **autoStart** es true, la reproducción se inicia automáticamente cada vez que se establece **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="c5de4-112">If the AxWindowsMediaPlayer.settings.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="c5de4-113">Puede recuperar una interfaz IWMPMedia para un elemento multimedia determinado a través de la propiedad IWMPPlaylist. Item (el método IWMPPlaylist. Get \_ Item en C#).</span><span class="sxs-lookup"><span data-stu-id="c5de4-113">You can retrieve an IWMPMedia interface for a given media item through the IWMPPlaylist.Item property (the IWMPPlaylist.get\_Item method in C#).</span></span> <span data-ttu-id="c5de4-114">Para cargar un elemento multimedia con un nombre de archivo, establezca la propiedad URL o use newMedia.</span><span class="sxs-lookup"><span data-stu-id="c5de4-114">To load a media item using a file name, set the URL property or use newMedia.</span></span>

## <a name="examples"></a><span data-ttu-id="c5de4-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c5de4-115">Examples</span></span>

<span data-ttu-id="c5de4-116">En el ejemplo siguiente se recupera el primer elemento multimedia de la biblioteca y se usa la propiedad currentMedia para establecer el elemento multimedia recuperado como el elemento multimedia actual y mostrar su nombre.</span><span class="sxs-lookup"><span data-stu-id="c5de4-116">The following example retrieves the first media item in the library and uses the currentMedia property to set the retrieved media item as the current media item and display its name.</span></span> <span data-ttu-id="c5de4-117">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="c5de4-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
```





## <a name="requirements"></a><span data-ttu-id="c5de4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5de4-118">Requirements</span></span>



| <span data-ttu-id="c5de4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5de4-119">Requirement</span></span> | <span data-ttu-id="c5de4-120">Value</span><span class="sxs-lookup"><span data-stu-id="c5de4-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5de4-121">Versión</span><span class="sxs-lookup"><span data-stu-id="c5de4-121">Version</span></span><br/>   | <span data-ttu-id="c5de4-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="c5de4-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="c5de4-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c5de4-123">Namespace</span></span><br/> | <span data-ttu-id="c5de4-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="c5de4-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="c5de4-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="c5de4-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="c5de4-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="c5de4-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5de4-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5de4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5de4-128">**Objeto AxWindowsMediaPlayer (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c5de4-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c5de4-129">**AxWindowsMediaPlayer. newMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c5de4-129">**AxWindowsMediaPlayer.newMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[<span data-ttu-id="c5de4-130">**AxWindowsMediaPlayer. URL (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c5de4-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c5de4-131">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c5de4-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c5de4-132">**IWMPPlaylist. Item (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c5de4-132">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="c5de4-133">**IWMPSettings. autoStart (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="c5de4-133">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





