---
title: IWMPMediaCollection getByAttribute, método
description: El método getByAttribute devuelve una interfaz IWMPPlaylist que corresponde al atributo especificado que tiene el valor especificado.
ms.assetid: ece70a2c-38bc-4652-8319-efcde5f9720a
keywords:
- método getByAttribute de Windows Media Player
- método getByAttribute Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método getByAttribute
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getByAttribute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd7adba98fbfa450cd938b56ec6d91598b918d0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671812"
---
# <a name="iwmpmediacollectiongetbyattribute-method"></a><span data-ttu-id="882ad-106">IWMPMediaCollection:: getByAttribute (método)</span><span class="sxs-lookup"><span data-stu-id="882ad-106">IWMPMediaCollection::getByAttribute method</span></span>

<span data-ttu-id="882ad-107">El método **getByAttribute** devuelve una interfaz **IWMPPlaylist** que corresponde al atributo especificado que tiene el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="882ad-107">The **getByAttribute** method returns an **IWMPPlaylist** interface that corresponds to the specified attribute having the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="882ad-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="882ad-108">Syntax</span></span>


```CSharp
public IWMPPlaylist getByAttribute(
  System.String bstrAttribute,
  System.String bstrValue
);
```


```VB

Public Function getByAttribute( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrValue As System.String _
) As IWMPPlaylist
Implements IWMPMediaCollection.getByAttribute
```





## <a name="parameters"></a><span data-ttu-id="882ad-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="882ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="882ad-110">*bstrAttribute* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="882ad-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882ad-111">**System. String** que es el atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="882ad-111">The **System.String** that is the specified attribute.</span></span>

</dd> <dt>

<span data-ttu-id="882ad-112">*bstrValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="882ad-112">*bstrValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="882ad-113">**System. String** que es el valor especificado.</span><span class="sxs-lookup"><span data-stu-id="882ad-113">The **System.String** that is the specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="882ad-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="882ad-114">Return value</span></span>

<span data-ttu-id="882ad-115">Una interfaz **WMPLib. IWMPPlaylist** para los elementos multimedia recuperados.</span><span class="sxs-lookup"><span data-stu-id="882ad-115">A **WMPLib.IWMPPlaylist** interface for the retrieved media items.</span></span>

## <a name="remarks"></a><span data-ttu-id="882ad-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="882ad-116">Remarks</span></span>

<span data-ttu-id="882ad-117">Este método se puede utilizar para crear una consulta genérica para los elementos multimedia que coinciden con un valor para un atributo de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="882ad-117">This method can be used to create a generic query for media items that match a value for an attribute in the library.</span></span> <span data-ttu-id="882ad-118">Esto es útil en el caso de los atributos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="882ad-118">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="882ad-119">Si el atributo no existe, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="882ad-119">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="882ad-120">Puede utilizar este método para recuperar todos los elementos multimedia de un tipo específico.</span><span class="sxs-lookup"><span data-stu-id="882ad-120">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="882ad-121">Use el nombre de atributo **mediatype** y uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="882ad-121">Use the attribute name **MediaType** and one of the following values.</span></span>



| <span data-ttu-id="882ad-122">Value</span><span class="sxs-lookup"><span data-stu-id="882ad-122">Value</span></span>    | <span data-ttu-id="882ad-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="882ad-123">Description</span></span>                                               |
|----------|-----------------------------------------------------------|
| <span data-ttu-id="882ad-124">audio</span><span class="sxs-lookup"><span data-stu-id="882ad-124">audio</span></span>    | <span data-ttu-id="882ad-125">Música y otros elementos de solo audio</span><span class="sxs-lookup"><span data-stu-id="882ad-125">Music and other audio-only items</span></span>                          |
| <span data-ttu-id="882ad-126">Otros</span><span class="sxs-lookup"><span data-stu-id="882ad-126">other</span></span>    | <span data-ttu-id="882ad-127">Otros elementos, como un archivo. ASF o la dirección URL de una secuencia.</span><span class="sxs-lookup"><span data-stu-id="882ad-127">Other items, such as an .asf file or the URL of a stream.</span></span> |
| <span data-ttu-id="882ad-128">álbum</span><span class="sxs-lookup"><span data-stu-id="882ad-128">photo</span></span>    | <span data-ttu-id="882ad-129">Elementos de fotografía.</span><span class="sxs-lookup"><span data-stu-id="882ad-129">Photo items.</span></span> <span data-ttu-id="882ad-130">Requiere Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="882ad-130">Requires Windows Media Player 10.</span></span>            |
| <span data-ttu-id="882ad-131">automáticas</span><span class="sxs-lookup"><span data-stu-id="882ad-131">playlist</span></span> | <span data-ttu-id="882ad-132">Listas de reproducción representadas como elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="882ad-132">Playlists represented as media items.</span></span>                     |
| <span data-ttu-id="882ad-133">radio</span><span class="sxs-lookup"><span data-stu-id="882ad-133">radio</span></span>    | <span data-ttu-id="882ad-134">Elementos de la estación de radio.</span><span class="sxs-lookup"><span data-stu-id="882ad-134">Radio station items.</span></span> <span data-ttu-id="882ad-135">No lo usa Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="882ad-135">Not used by Windows Media Player 10.</span></span> |
| <span data-ttu-id="882ad-136">video</span><span class="sxs-lookup"><span data-stu-id="882ad-136">video</span></span>    | <span data-ttu-id="882ad-137">Elementos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="882ad-137">Video items.</span></span>                                              |



 

<span data-ttu-id="882ad-138">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="882ad-138">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="882ad-139">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="882ad-139">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="882ad-140">Para obtener información sobre los atributos que admite Windows Media Player, vea la [referencia de atributo](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="882ad-140">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="882ad-141">Hay dos maneras de recuperar una interfaz **IWMPMediaCollection** y el comportamiento del método **getByAttribute** depende de cuál de esas dos maneras se usa.</span><span class="sxs-lookup"><span data-stu-id="882ad-141">There are two ways you ways you can retrieve an **IWMPMediaCollection** interface, and the behavior of the **getByAttribute** method depends on which of those two ways you use.</span></span> <span data-ttu-id="882ad-142">Si recupera la interfaz llamando a [AxWindowsMediaPlayer. mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), el método **getByAttribute** devuelve todos los elementos multimedia de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="882ad-142">If you retrieve the interface by calling [AxWindowsMediaPlayer.mediaCollection](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md), then the **getByAttribute** method returns all the media items in the library.</span></span> <span data-ttu-id="882ad-143">Sin embargo, si recupera la interfaz llamando a [IWMPLibrary. mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), el método **getByAttribute** devuelve solo los elementos de audio de la biblioteca que tienen el atributo y el valor especificados.</span><span class="sxs-lookup"><span data-stu-id="882ad-143">However, if you retrieve the interface by calling [IWMPLibrary.mediaCollection](wmplibiwmplibrary-iwmplibrary-mediacollection--vb-and-c.md), then the **getByAttribute** method returns only the audio items in the library that have the specified attribute and value.</span></span>

## <a name="examples"></a><span data-ttu-id="882ad-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="882ad-144">Examples</span></span>

<span data-ttu-id="882ad-145">En el ejemplo de código siguiente se usa **getByAttribute** para reproducir todo el contenido de la biblioteca por el artista denominado Triode 48.</span><span class="sxs-lookup"><span data-stu-id="882ad-145">The following code example uses **getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="882ad-146">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="882ad-146">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to a playlist that contains media items by a particular artist.
WMPLib.IWMPPlaylist pl = player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
player.currentPlaylist = pl;

// Play the media items in the current playlist. 
player.Ctlcontrols.play();
```


```VB

' Get an interface to a playlist that contains media items by a particular artist.
Dim pl As WMPLib.IWMPPlaylist = player.mediaCollection.getByAttribute(&quot;Artist&quot;, &quot;Triode 48&quot;)

&#39; Make the new playlist the current one.
player.currentPlaylist = pl

&#39; Play the media items in the current playlist. 
player.Ctlcontrols.play()
```





## <a name="requirements"></a><span data-ttu-id="882ad-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="882ad-147">Requirements</span></span>



| <span data-ttu-id="882ad-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="882ad-148">Requirement</span></span> | <span data-ttu-id="882ad-149">Value</span><span class="sxs-lookup"><span data-stu-id="882ad-149">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="882ad-150">Versión</span><span class="sxs-lookup"><span data-stu-id="882ad-150">Version</span></span><br/>   | <span data-ttu-id="882ad-151">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="882ad-151">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="882ad-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="882ad-152">Namespace</span></span><br/> | <span data-ttu-id="882ad-153">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="882ad-153">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="882ad-154">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="882ad-154">Assembly</span></span><br/>  | <dl> <span data-ttu-id="882ad-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="882ad-155"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="882ad-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="882ad-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="882ad-157">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="882ad-157">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="882ad-158">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="882ad-158">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="882ad-159">**IWMPPlaylistCollection. getAll (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="882ad-159">**IWMPPlaylistCollection.getAll (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getall--vb-and-c.md)
</dt> </dl>

 

 





