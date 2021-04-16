---
title: IWMPPlaylist removeItem (método)
description: El método removeItem quita el elemento multimedia especificado de la lista de reproducción.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- método removeItem Media Player Windows
- método removeItem Windows Media Player, interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Windows Media Player, método removeItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec845b7657e04f17c47119dd169032ebe5815786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708273"
---
# <a name="iwmpplaylistremoveitem-method"></a><span data-ttu-id="6ba1e-106">IWMPPlaylist:: removeItem (método)</span><span class="sxs-lookup"><span data-stu-id="6ba1e-106">IWMPPlaylist::removeItem method</span></span>

<span data-ttu-id="6ba1e-107">El método **RemoveItem** quita el elemento multimedia especificado de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-107">The **removeItem** method removes the specified media item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba1e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ba1e-108">Syntax</span></span>


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a><span data-ttu-id="6ba1e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ba1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba1e-110">*pIWMPMedia* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ba1e-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ba1e-111">Una interfaz **WMPLib. IWMPMedia** que representa el elemento multimedia que se va a quitar de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-111">A **WMPLib.IWMPMedia** interface that represents the media item to remove from the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba1e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ba1e-112">Return value</span></span>

<span data-ttu-id="6ba1e-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ba1e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ba1e-114">Remarks</span></span>

<span data-ttu-id="6ba1e-115">Si el elemento quitado es la pista que se está reproduciendo, se detiene la reproducción y el siguiente elemento de la lista de reproducción se convierte en el actual.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-115">If the item removed is the currently playing track, playback stops and the next item in the playlist becomes the current one.</span></span>

<span data-ttu-id="6ba1e-116">Si no hay ningún elemento siguiente, se usa el elemento anterior.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-116">If there is no next item, the previous item is used.</span></span> <span data-ttu-id="6ba1e-117">Si no hay ningún otro elemento, la propiedad **AxWindowsMediaPlayer. currentMedia** devolverá **null**.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-117">If there are no other items, then the **AxWindowsMediaPlayer.currentMedia** property will return **NULL**.</span></span>

<span data-ttu-id="6ba1e-118">Antes de llamar a este método, debe tener acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6ba1e-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="6ba1e-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6ba1e-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba1e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ba1e-120">Requirements</span></span>



| <span data-ttu-id="6ba1e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba1e-121">Requirement</span></span> | <span data-ttu-id="6ba1e-122">Value</span><span class="sxs-lookup"><span data-stu-id="6ba1e-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba1e-123">Versión</span><span class="sxs-lookup"><span data-stu-id="6ba1e-123">Version</span></span><br/>   | <span data-ttu-id="6ba1e-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="6ba1e-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6ba1e-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6ba1e-125">Namespace</span></span><br/> | <span data-ttu-id="6ba1e-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6ba1e-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="6ba1e-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6ba1e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6ba1e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba1e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ba1e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba1e-130">**AxWindowsMediaPlayer. currentMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6ba1e-131">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6ba1e-132">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-132">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6ba1e-133">**IWMPPlaylist. insertItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-133">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6ba1e-134">**IWMPPlaylist. Item (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-134">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6ba1e-135">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6ba1e-136">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="6ba1e-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





