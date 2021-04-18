---
title: IWMPMediaCollection getAll (método)
description: El método getAll devuelve una interfaz IWMPPlaylist que corresponde a la lista de reproducción que contiene todos los elementos multimedia de la biblioteca.
ms.assetid: f2bbb4a4-7397-4c97-afd9-e8ee380af9da
keywords:
- getAll (método) de Windows Media Player
- getAll (método) Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método getAll
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAll
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08548ae29db12ded788f34563ef5e319c27d61
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670361"
---
# <a name="iwmpmediacollectiongetall-method"></a><span data-ttu-id="aff57-106">IWMPMediaCollection:: getAll (método)</span><span class="sxs-lookup"><span data-stu-id="aff57-106">IWMPMediaCollection::getAll method</span></span>

<span data-ttu-id="aff57-107">El método **getAll** devuelve una interfaz **IWMPPlaylist** que corresponde a la lista de reproducción que contiene todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="aff57-107">The **getAll** method returns an **IWMPPlaylist** interface that corresponds to the playlist that contains all media items in the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff57-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aff57-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getAll();
```


```VB

Public Function getAll() As IWMPPlaylist
Implements IWMPMediaCollection.getAll
```





## <a name="parameters"></a><span data-ttu-id="aff57-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aff57-109">Parameters</span></span>

<span data-ttu-id="aff57-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="aff57-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aff57-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aff57-111">Return value</span></span>

<span data-ttu-id="aff57-112">La interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción que contiene todos los elementos multimedia solicitados.</span><span class="sxs-lookup"><span data-stu-id="aff57-112">The **WMPLib.IWMPPlaylist** interface for the playlist that contains all of the requested media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="aff57-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aff57-113">Remarks</span></span>

<span data-ttu-id="aff57-114">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="aff57-114">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="aff57-115">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="aff57-115">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="aff57-116">Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del método **getAll** depende de cuál de esas dos formas se usa.</span><span class="sxs-lookup"><span data-stu-id="aff57-116">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getAll** method depends on which of those two ways you use.</span></span> <span data-ttu-id="aff57-117">Si recupera la interfaz llamando a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el método **getAll** devuelve todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="aff57-117">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getAll** method returns all the media items in the library.</span></span> <span data-ttu-id="aff57-118">Sin embargo, si recupera la interfaz llamando a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el método **getAll** solo devuelve los elementos de audio de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="aff57-118">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getAll** method returns only the audio items in the library.</span></span>

## <a name="examples"></a><span data-ttu-id="aff57-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="aff57-119">Examples</span></span>

<span data-ttu-id="aff57-120">En el ejemplo siguiente se usa **getAll** para reproducir elementos multimedia aleatoriamente de la colección de medios.</span><span class="sxs-lookup"><span data-stu-id="aff57-120">The following example uses **getAll** to play media items randomly from the media collection.</span></span> <span data-ttu-id="aff57-121">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="aff57-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a random number generator. 
System.Random randGenerator = new System.Random();

// Store the count of all media items in the media collection.
int count = player.mediaCollection.getAll().count;

// Get a random integer using the count as the max value.
int rand = randGenerator.Next(count);

// Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().get_Item(rand);

// Play the media item.
player.Ctlcontrols.play();
```


```VB

' Create a random number generator. 
Dim randGenerator As System.Random = New System.Random()

&#39; Store the count of all media items in the media collection.
Dim count As Integer = player.mediaCollection.getAll().count

&#39; Get a random integer using the count as the max value.
Dim rand As Integer = randGenerator.Next(count)

&#39; Make the random media item the current media item.
player.currentMedia = player.mediaCollection.getAll().Item(rand)

&#39; Play the media item.
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="aff57-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aff57-122">Requirements</span></span>



| <span data-ttu-id="aff57-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="aff57-123">Requirement</span></span> | <span data-ttu-id="aff57-124">Value</span><span class="sxs-lookup"><span data-stu-id="aff57-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff57-125">Versión</span><span class="sxs-lookup"><span data-stu-id="aff57-125">Version</span></span><br/>   | <span data-ttu-id="aff57-126">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="aff57-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="aff57-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aff57-127">Namespace</span></span><br/> | <span data-ttu-id="aff57-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="aff57-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="aff57-129">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="aff57-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="aff57-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="aff57-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff57-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="aff57-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff57-132">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="aff57-132">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aff57-133">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="aff57-133">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





