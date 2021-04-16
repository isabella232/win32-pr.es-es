---
title: IWMPMediaCollection getByAuthor, método
description: El método getByAuthor devuelve una interfaz IWMPPlaylist que proporciona acceso a los elementos multimedia por el autor especificado.
ms.assetid: eb3793f6-bad1-4c80-991e-c6d0093ae57f
keywords:
- método getByAuthor de Windows Media Player
- método getByAuthor Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método getByAuthor
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAuthor
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e594de010a65c15088e2a31a3ccbac2ac5a1fc6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671811"
---
# <a name="iwmpmediacollectiongetbyauthor-method"></a><span data-ttu-id="2e942-106">IWMPMediaCollection:: getByAuthor (método)</span><span class="sxs-lookup"><span data-stu-id="2e942-106">IWMPMediaCollection::getByAuthor method</span></span>

<span data-ttu-id="2e942-107">El `getByAuthor` método devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia por el autor especificado.</span><span class="sxs-lookup"><span data-stu-id="2e942-107">The `getByAuthor` method returns an **IWMPPlaylist** interface that provides access to the media items by the specified author.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e942-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e942-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAuthor(
  System.String bstrAuthor
);
```


```VB

Public Function getByAuthor( _
  ByVal bstrAuthor As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAuthor
```





## <a name="parameters"></a><span data-ttu-id="2e942-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e942-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e942-110">*bstrAuthor* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e942-110">*bstrAuthor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e942-111">**System. String** que es el nombre del autor.</span><span class="sxs-lookup"><span data-stu-id="2e942-111">The **System.String** that is the name of the author.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e942-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e942-112">Return value</span></span>

<span data-ttu-id="2e942-113">Una interfaz **WMPLib. IWMPPlaylist** para los elementos multimedia recuperados.</span><span class="sxs-lookup"><span data-stu-id="2e942-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e942-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e942-114">Remarks</span></span>

<span data-ttu-id="2e942-115">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e942-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="2e942-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2e942-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="2e942-117">Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del `getByAuthor` método depende de cuál de esas dos maneras se usa.</span><span class="sxs-lookup"><span data-stu-id="2e942-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the `getByAuthor` method depends on which of those two ways you use.</span></span> <span data-ttu-id="2e942-118">Si recupera la interfaz llamando a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el `getByAuthor` método devuelve todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="2e942-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the `getByAuthor` method returns all the media items in the library.</span></span> <span data-ttu-id="2e942-119">Sin embargo, si recupera la interfaz llamando a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el `getByAuthor` método solo devuelve los elementos de audio de la biblioteca que tienen el atributo y el valor especificados.</span><span class="sxs-lookup"><span data-stu-id="2e942-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the `getByAuthor` method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="2e942-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2e942-120">Examples</span></span>

<span data-ttu-id="2e942-121">En el ejemplo siguiente `getByAuthor` se usa para crear una lista de reproducción de elementos multimedia cuando el usuario hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="2e942-121">The following example uses `getByAuthor` to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="2e942-122">La lista de reproducción contiene elementos que coinciden con el nombre del autor especificado por el usuario en un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="2e942-122">The playlist contains items matching the author's name specified by the user in a text box.</span></span> <span data-ttu-id="2e942-123">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="2e942-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAuthor_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the author's name from the text box. 
    string author = getAuthor.Text;

    // Create the playlist using getByAuthor. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAuthor(author);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAuthor_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAuthor.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the author&#39;s name from the text box. 
    Dim author As String = getAuthor.Text

    &#39; Create the playlist using getByAuthor. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAuthor(author)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2e942-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e942-124">Requirements</span></span>



| <span data-ttu-id="2e942-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e942-125">Requirement</span></span> | <span data-ttu-id="2e942-126">Value</span><span class="sxs-lookup"><span data-stu-id="2e942-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e942-127">Versión</span><span class="sxs-lookup"><span data-stu-id="2e942-127">Version</span></span><br/>   | <span data-ttu-id="2e942-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="2e942-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2e942-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e942-129">Namespace</span></span><br/> | <span data-ttu-id="2e942-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2e942-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2e942-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="2e942-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2e942-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2e942-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e942-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e942-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e942-134">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2e942-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2e942-135">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="2e942-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





