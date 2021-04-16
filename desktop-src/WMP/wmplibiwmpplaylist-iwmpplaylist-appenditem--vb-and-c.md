---
title: IWMPPlaylist appendItem, método
description: El método appendItem agrega un elemento multimedia al final de una lista de reproducción.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- método appendItem de Windows Media Player
- método appendItem Windows Media Player, interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Windows Media Player, método appendItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a94e1b515ec6301830af2de06bae32602bdf66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709144"
---
# <a name="iwmpplaylistappenditem-method"></a><span data-ttu-id="fd88c-106">IWMPPlaylist:: appendItem (método)</span><span class="sxs-lookup"><span data-stu-id="fd88c-106">IWMPPlaylist::appendItem method</span></span>

<span data-ttu-id="fd88c-107">El método **appendItem** agrega un elemento multimedia al final de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="fd88c-107">The **appendItem** method adds a media item to the end of a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd88c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd88c-108">Syntax</span></span>


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a><span data-ttu-id="fd88c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fd88c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd88c-110">*pIWMPMedia* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fd88c-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd88c-111">Una interfaz **WMPLib. IWMPMedia** que representa el elemento multimedia que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="fd88c-111">An **WMPLib.IWMPMedia** interface that represents the media item to be appended.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd88c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd88c-112">Return value</span></span>

<span data-ttu-id="fd88c-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fd88c-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd88c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd88c-114">Remarks</span></span>

<span data-ttu-id="fd88c-115">Antes de llamar a este método, debe tener acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fd88c-115">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="fd88c-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="fd88c-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="fd88c-117">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fd88c-117">Examples</span></span>

<span data-ttu-id="fd88c-118">En el ejemplo siguiente se usa **appendItem** para agregar el elemento multimedia actual a la lista de reproducción denominada "ThreeList".</span><span class="sxs-lookup"><span data-stu-id="fd88c-118">The following example uses **appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="fd88c-119">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="fd88c-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a><span data-ttu-id="fd88c-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd88c-120">Requirements</span></span>



| <span data-ttu-id="fd88c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd88c-121">Requirement</span></span> | <span data-ttu-id="fd88c-122">Value</span><span class="sxs-lookup"><span data-stu-id="fd88c-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd88c-123">Versión</span><span class="sxs-lookup"><span data-stu-id="fd88c-123">Version</span></span><br/>   | <span data-ttu-id="fd88c-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="fd88c-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fd88c-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fd88c-125">Namespace</span></span><br/> | <span data-ttu-id="fd88c-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fd88c-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fd88c-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="fd88c-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fd88c-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fd88c-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd88c-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd88c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd88c-130">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="fd88c-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fd88c-131">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="fd88c-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





