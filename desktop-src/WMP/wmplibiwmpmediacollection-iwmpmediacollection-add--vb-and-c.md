---
title: IWMPMediaCollection Add (método)
description: El método Add agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca. | IWMPMediaCollection Add (método)
ms.assetid: a3539646-797b-4481-a31e-86771f3633a9
keywords:
- Agregar método Media Player de Windows
- Agregar método Windows Media Player, interfaz IWMPMediaCollection
- Interfaz IWMPMediaCollection Windows Media Player, método Add
topic_type:
- apiref
api_name:
- IWMPMediaCollection.add
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7953067281e394df71a1a53c874cb80837a5f35d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670362"
---
# <a name="iwmpmediacollectionadd-method"></a><span data-ttu-id="8e93b-107">IWMPMediaCollection:: Add (método)</span><span class="sxs-lookup"><span data-stu-id="8e93b-107">IWMPMediaCollection::add method</span></span>

<span data-ttu-id="8e93b-108">El método **Add** agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8e93b-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e93b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e93b-109">Syntax</span></span>


```CSharp
public IWMPMedia add(
  System.String bstrURL
);
```


```VB

Public Function add( _
  ByVal bstrURL As System.String _
) As IWMPMedia
Implements IWMPMediaCollection.add
```





## <a name="parameters"></a><span data-ttu-id="8e93b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8e93b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e93b-111">*bstrURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8e93b-111">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e93b-112">**System. String** que es la dirección URL que especifica la ubicación del elemento multimedia o de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="8e93b-112">A **System.String** that is the URL that specifies the location of the media item or playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e93b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8e93b-113">Return value</span></span>

<span data-ttu-id="8e93b-114">La interfaz **WMPLib. IWMPMedia** para el elemento o la lista de reproducción agregados.</span><span class="sxs-lookup"><span data-stu-id="8e93b-114">The **WMPLib.IWMPMedia** interface for the added item or playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e93b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e93b-115">Remarks</span></span>

<span data-ttu-id="8e93b-116">Este método carga un elemento multimedia o una lista de reproducción existente en la biblioteca, dada una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="8e93b-116">This method loads an existing media item or playlist into the library, given a path.</span></span> <span data-ttu-id="8e93b-117">Este método no mueve ni cambia el archivo.</span><span class="sxs-lookup"><span data-stu-id="8e93b-117">This method does not move or change the file.</span></span> <span data-ttu-id="8e93b-118">Este método produce un error si se proporciona una ruta de acceso local no válida, pero no se comprueba la validez de los elementos multimedia en sí antes de que se agreguen a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8e93b-118">This method fails if given an invalid local path, but media items themselves are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="8e93b-119">Este método acepta archivos de lista de reproducción estática y automática.</span><span class="sxs-lookup"><span data-stu-id="8e93b-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="8e93b-120">También se puede usar el método **IWMPPlaylistCollection. importPlaylist** para agregar una lista de reproducción estática a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8e93b-120">The **IWMPPlaylistCollection.importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="8e93b-121">Antes de llamar a este método, debe tener acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8e93b-121">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="8e93b-122">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8e93b-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8e93b-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8e93b-123">Examples</span></span>

<span data-ttu-id="8e93b-124">En el ejemplo siguiente se agregan tres objetos multimedia a la colección de medios de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8e93b-124">The following example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="8e93b-125">El objeto AxWMPLib. AxWindowsMediaPlayer se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="8e93b-125">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Adding a media object using a website.
player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"\\yourservername\Public\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Either use the @ symbol to denote a quoted string literal or add additional
// backlashes as an escape for every original backslash.
player.mediaCollection.add(@"C:\WMSDK\WMPSDK\samples\media\house.wma");
```


```VB

' Adding a media object using a website.
player.mediaCollection.add(&quot;http:&#39;www.proseware.com/Media/Laure.wma&quot;)

&#39; Adding a media object from a local network.
player.mediaCollection.add(&quot;\\yourservername\Public\Jeanne.wma&quot;)

&#39; Adding a media object from a file on a local drive.
player.mediaCollection.add(&quot;C:\WMSDK\WMPSDK\samples\media\house.wma&quot;)
```





## <a name="requirements"></a><span data-ttu-id="8e93b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e93b-126">Requirements</span></span>



| <span data-ttu-id="8e93b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e93b-127">Requirement</span></span> | <span data-ttu-id="8e93b-128">Value</span><span class="sxs-lookup"><span data-stu-id="8e93b-128">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e93b-129">Versión</span><span class="sxs-lookup"><span data-stu-id="8e93b-129">Version</span></span><br/>   | <span data-ttu-id="8e93b-130">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="8e93b-130">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8e93b-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e93b-131">Namespace</span></span><br/> | <span data-ttu-id="8e93b-132">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8e93b-132">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8e93b-133">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="8e93b-133">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8e93b-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8e93b-134"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e93b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e93b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e93b-136">**Interfaz IWMPMediaCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="8e93b-136">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e93b-137">**IWMPMediaCollection. Remove (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="8e93b-137">**IWMPMediaCollection.remove (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-remove--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8e93b-138">**IWMPPlaylistCollection. importPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="8e93b-138">**IWMPPlaylistCollection.importPlaylist (VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-importplaylist--vb-and-c.md)
</dt> </dl>

 

 





