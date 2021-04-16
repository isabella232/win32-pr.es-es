---
title: IWMPMediaCollection getByAlbum, método
description: El método getByAlbum devuelve una interfaz IWMPPlaylist que proporciona acceso a los elementos multimedia del álbum especificado.
ms.assetid: 26f004c0-de46-4792-8212-9d4ac749bb21
keywords:
- método getByAlbum de Windows Media Player
- método getByAlbum Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método getByAlbum
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAlbum
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c455e9bd61038a4d72bb6537d7c62b30a5d0b733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671813"
---
# <a name="iwmpmediacollectiongetbyalbum-method"></a><span data-ttu-id="edb6b-106">IWMPMediaCollection:: getByAlbum (método)</span><span class="sxs-lookup"><span data-stu-id="edb6b-106">IWMPMediaCollection::getByAlbum method</span></span>

<span data-ttu-id="edb6b-107">El método **getByAlbum** devuelve una interfaz **IWMPPlaylist** que proporciona acceso a los elementos multimedia del álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="edb6b-107">The **getByAlbum** method returns an **IWMPPlaylist** interface that provides access to media items from the specified album.</span></span>

## <a name="syntax"></a><span data-ttu-id="edb6b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="edb6b-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAlbum(
  System.String bstrAlbum
);
```


```VB

Public Function getByAlbum( _
  ByVal bstrAlbum As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAlbum
```





## <a name="parameters"></a><span data-ttu-id="edb6b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="edb6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edb6b-110">*bstrAlbum* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="edb6b-110">*bstrAlbum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edb6b-111">**System. String** que es el título del álbum.</span><span class="sxs-lookup"><span data-stu-id="edb6b-111">The **System.String** that is the title of the album.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edb6b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="edb6b-112">Return value</span></span>

<span data-ttu-id="edb6b-113">Una interfaz **WMPLib. IWMPPlaylist** para los elementos multimedia recuperados.</span><span class="sxs-lookup"><span data-stu-id="edb6b-113">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="edb6b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="edb6b-114">Remarks</span></span>

<span data-ttu-id="edb6b-115">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="edb6b-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="edb6b-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="edb6b-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="edb6b-117">Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del método **getByAlbum** depende de cuál de esas dos maneras se usa.</span><span class="sxs-lookup"><span data-stu-id="edb6b-117">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAlbum** method depends on which of those two ways you use.</span></span> <span data-ttu-id="edb6b-118">Si recupera la interfaz llamando a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el método **getByAlbum** devuelve todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="edb6b-118">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAlbum** method returns all the media items in the library.</span></span> <span data-ttu-id="edb6b-119">Sin embargo, si recupera la interfaz llamando a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el método **getByAlbum** devuelve solo los elementos de audio de la biblioteca que pertenecen al álbum especificado.</span><span class="sxs-lookup"><span data-stu-id="edb6b-119">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAlbum** method returns only the audio items in the library that belong to the specified album.</span></span>

## <a name="examples"></a><span data-ttu-id="edb6b-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="edb6b-120">Examples</span></span>

<span data-ttu-id="edb6b-121">En el ejemplo siguiente se usa **getByAlbum** para crear una lista de reproducción de elementos multimedia cuando el usuario hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="edb6b-121">The following example uses **getByAlbum** to create a playlist of media items when the user clicks a button.</span></span> <span data-ttu-id="edb6b-122">La lista de reproducción contiene elementos con el álbum especificado por el usuario en un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="edb6b-122">The playlist contains items with the album specified by the user in a text box.</span></span> <span data-ttu-id="edb6b-123">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="edb6b-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playAlbum_Click(object sender, System.EventArgs e)
{ 
    // ...Add code to ensure that the text box contains a valid value.
 
    // Retrieve the album title text that the user entered in the text box. 
    string album = getAlbum.Text;

    // Create the playlist using getByAlbum. 
    WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAlbum(album);

    // Make the new playlist the current playlist. 
    player.currentPlaylist = pl;

    // Play the media in the current playlist. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playAlbum_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playAlbum.Click

    &#39; ...Add code to ensure that the text box contains a valid value.

    &#39; Retrieve the album title text that the user entered in the text box. 
    Dim album As String = getAlbum.Text

    &#39; Create the playlist using getByAlbum. 
    Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAlbum(album)

    &#39; Make the new playlist the current playlist. 
    player.currentPlaylist = pl

    &#39; Play the media in the current playlist. 
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="edb6b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="edb6b-124">Requirements</span></span>



| <span data-ttu-id="edb6b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="edb6b-125">Requirement</span></span> | <span data-ttu-id="edb6b-126">Value</span><span class="sxs-lookup"><span data-stu-id="edb6b-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edb6b-127">Versión</span><span class="sxs-lookup"><span data-stu-id="edb6b-127">Version</span></span><br/>   | <span data-ttu-id="edb6b-128">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="edb6b-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="edb6b-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="edb6b-129">Namespace</span></span><br/> | <span data-ttu-id="edb6b-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="edb6b-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="edb6b-131">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="edb6b-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="edb6b-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="edb6b-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edb6b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="edb6b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edb6b-134">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="edb6b-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="edb6b-135">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="edb6b-135">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





