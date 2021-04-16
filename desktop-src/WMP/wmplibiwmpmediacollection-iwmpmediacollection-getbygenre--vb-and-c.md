---
title: IWMPMediaCollection getByGenre, método
description: El método getByGenre devuelve una interfaz IWMPPlaylist que proporciona acceso a los elementos multimedia del género especificado.
ms.assetid: 0681e5a2-b56d-4c33-95ce-d9ef3cd5473d
keywords:
- método getByGenre de Windows Media Player
- método getByGenre Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método getByGenre
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByGenre
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb6477a4cd212f354f5af3ab7e50fc2a87092cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671661"
---
# <a name="iwmpmediacollectiongetbygenre-method"></a><span data-ttu-id="94416-106">IWMPMediaCollection:: getByGenre (método)</span><span class="sxs-lookup"><span data-stu-id="94416-106">IWMPMediaCollection::getByGenre method</span></span>

<span data-ttu-id="94416-107">El `getByGenre` método devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia del género especificado.</span><span class="sxs-lookup"><span data-stu-id="94416-107">The `getByGenre` method returns an **IWMPPlaylist** interface that provides access to media items of the specified genre.</span></span>

## <a name="syntax"></a><span data-ttu-id="94416-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94416-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByGenre(
  System.String bstrGenre
);
```


```VB

Public Function getByGenre( _
  ByVal bstrGenre As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByGenre
```





## <a name="parameters"></a><span data-ttu-id="94416-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94416-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94416-110">*bstrGenre* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="94416-110">*bstrGenre* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94416-111">**System. String** que es el nombre del género.</span><span class="sxs-lookup"><span data-stu-id="94416-111">The **System.String** that is the name of the genre.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94416-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94416-112">Return value</span></span>

<span data-ttu-id="94416-113">Una interfaz **WMPLib. IWMPPlaylist** para los elementos multimedia recuperados.</span><span class="sxs-lookup"><span data-stu-id="94416-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="94416-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94416-114">Remarks</span></span>

<span data-ttu-id="94416-115">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="94416-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="94416-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="94416-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="94416-117">Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del `getByGenre` método depende de cuál de esas dos maneras se usa.</span><span class="sxs-lookup"><span data-stu-id="94416-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByGenre` method depends on which of those two ways you use.</span></span> <span data-ttu-id="94416-118">Si recupera la interfaz llamando a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el `getByGenre` método devuelve todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="94416-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByGenre` method returns all the media items in the library.</span></span> <span data-ttu-id="94416-119">Sin embargo, si recupera la interfaz llamando a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el `getByGenre` método solo devuelve los elementos de audio de la biblioteca que tienen el atributo y el valor especificados.</span><span class="sxs-lookup"><span data-stu-id="94416-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByGenre` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="94416-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="94416-120">Examples</span></span>

<span data-ttu-id="94416-121">En el ejemplo siguiente `getByGenre` se usa para recuperar una lista de reproducción de elementos multimedia cuando el usuario hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="94416-121">The following example uses `getByGenre` to retrieve a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="94416-122">La lista de reproducción contiene elementos con el género especificado por el usuario en un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="94416-122">The playlist contains items with the genre specified by the user in a text box.</span></span> <span data-ttu-id="94416-123">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="94416-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playGenre_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the genre that the user entered in the text box. 
    string genre = getGenre.Text;

    // Create the playlist using getByGenre. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByGenre(genre);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playGenre.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the genre that the user entered in the text box. 
    Dim genre As String = getGenre.Text

    &#39; Create the playlist using getByGenre. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByGenre(genre)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="94416-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94416-124">Requirements</span></span>



| <span data-ttu-id="94416-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="94416-125">Requirement</span></span> | <span data-ttu-id="94416-126">Value</span><span class="sxs-lookup"><span data-stu-id="94416-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94416-127">Versión</span><span class="sxs-lookup"><span data-stu-id="94416-127">Version</span></span><br/>   | <span data-ttu-id="94416-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="94416-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="94416-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="94416-129">Namespace</span></span><br/> | <span data-ttu-id="94416-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="94416-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="94416-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="94416-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="94416-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="94416-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94416-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="94416-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94416-134">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="94416-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="94416-135">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="94416-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





