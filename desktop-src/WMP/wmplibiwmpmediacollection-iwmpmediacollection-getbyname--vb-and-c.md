---
title: IWMPMediaCollection getByName, método
description: El método getByName devuelve una interfaz IWMPPlaylist que proporciona acceso a los elementos multimedia con el nombre especificado.
ms.assetid: 137e938c-eb9f-4a87-8962-880e71a11ca2
keywords:
- método getByName de Windows Media Player
- método getByName Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método getByName
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64c68e2a5359eadf9c6212571ed948c103c01bdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671751"
---
# <a name="iwmpmediacollectiongetbyname-method"></a><span data-ttu-id="a01ac-106">IWMPMediaCollection:: getByName (método)</span><span class="sxs-lookup"><span data-stu-id="a01ac-106">IWMPMediaCollection::getByName method</span></span>

<span data-ttu-id="a01ac-107">El `getByName` método devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="a01ac-107">The `getByName` method returns an **IWMPPlaylist** interface that provides access to media items with the specified name.</span></span>

## <a name="syntax"></a><span data-ttu-id="a01ac-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a01ac-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByName(
  System.String bstrName
);
```


```VB

Public Function getByName( _
  ByVal bstrName As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByName
```





## <a name="parameters"></a><span data-ttu-id="a01ac-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a01ac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a01ac-110">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a01ac-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a01ac-111">**System. String** que es el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="a01ac-111">The **System.String** that is the specified name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a01ac-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a01ac-112">Return value</span></span>

<span data-ttu-id="a01ac-113">Una interfaz **WMPLib. IWMPPlaylist** para los elementos multimedia recuperados.</span><span class="sxs-lookup"><span data-stu-id="a01ac-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="a01ac-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a01ac-114">Remarks</span></span>

<span data-ttu-id="a01ac-115">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a01ac-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="a01ac-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="a01ac-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="a01ac-117">Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del `getByName` método depende de cuál de esas dos maneras se usa.</span><span class="sxs-lookup"><span data-stu-id="a01ac-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByName` method depends on which of those two ways you use.</span></span> <span data-ttu-id="a01ac-118">Si recupera la interfaz llamando a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el `getByName` método devuelve todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a01ac-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByName` method returns all the media items in the library.</span></span> <span data-ttu-id="a01ac-119">Sin embargo, si recupera la interfaz llamando a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el `getByName` método solo devuelve los elementos de audio de la biblioteca que tienen el atributo y el valor especificados.</span><span class="sxs-lookup"><span data-stu-id="a01ac-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByName` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="a01ac-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a01ac-120">Examples</span></span>

<span data-ttu-id="a01ac-121">En el ejemplo siguiente `getByName` se usa para recuperar tres elementos de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a01ac-121">The following example uses `getByName` to retrieve three items from the library.</span></span> <span data-ttu-id="a01ac-122">Después, cada elemento se anexa a la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="a01ac-122">Each item is then appended to the current playlist.</span></span> <span data-ttu-id="a01ac-123">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="a01ac-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// In each case, use the name exactly as it appears in the library.
// Windows Media Player does not include file name extensions or file paths
// in the name. Internet URLs include the entire path, but not the 
// file name extension.

// Get an interface to a playlist that contains an Internet URL.
WMPLib.IWMPPlaylist one = player.mediaCollection.getByName("https://www.proseware.com/Media/Laure");

// Get an interface to a playlist that contains a file on a network server.
WMPLib.IWMPPlaylist two = player.mediaCollection.getByName("Jeanne");

// Get an interface to a playlist that contains a file on a local drive.
WMPLib.IWMPPlaylist three = player.mediaCollection.getByName("house");

// Append each item to the current playlist. Since each playlist retrieved
// using getByName contains one digital media item, use the get_Item
// method with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.get_Item(0));
player.currentPlaylist.appendItem(two.get_Item(0));
player.currentPlaylist.appendItem(three.get_Item(0));
```


```VB

' In each case, use the name exactly as it appears in the library.
&#39; Windows Media Player does not include file name extensions or file paths
&#39; in the name. Internet URLs include the entire path, but not the 
&#39; file name extension.

&#39; Get an interface to a playlist that contains an Internet URL.
Dim one As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;https://www.proseware.com/Media/Laure&quot;)

&#39; Get an interface to a playlist that contains a file on a network server.
Dim two As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;Jeanne&quot;)

&#39; Get an interface to a playlist that contains a file on a local drive.
Dim three As WMPLib.IWMPPlaylist = player.mediaCollection.getByName(&quot;house&quot;)

&#39; Append each item to the current playlist. Since each playlist retrieved
&#39; using getByName contains one digital media item, use the Item
&#39; property with an index of zero to reference that item.
player.currentPlaylist.appendItem(one.Item(0))
player.currentPlaylist.appendItem(two.Item(0))
player.currentPlaylist.appendItem(three.Item(0))
```





## <a name="requirements"></a><span data-ttu-id="a01ac-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a01ac-124">Requirements</span></span>



| <span data-ttu-id="a01ac-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a01ac-125">Requirement</span></span> | <span data-ttu-id="a01ac-126">Value</span><span class="sxs-lookup"><span data-stu-id="a01ac-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a01ac-127">Versión</span><span class="sxs-lookup"><span data-stu-id="a01ac-127">Version</span></span><br/>   | <span data-ttu-id="a01ac-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a01ac-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a01ac-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a01ac-129">Namespace</span></span><br/> | <span data-ttu-id="a01ac-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a01ac-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a01ac-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a01ac-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a01ac-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a01ac-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a01ac-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="a01ac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a01ac-134">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a01ac-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a01ac-135">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a01ac-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





