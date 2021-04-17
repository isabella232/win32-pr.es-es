---
title: MediaCollection. Add (método)
description: El método Add agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca. | MediaCollection. Add (método)
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Agregar método Media Player de Windows
- Agregar método Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, Add (método)
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690642"
---
# <a name="mediacollectionadd-method"></a><span data-ttu-id="ecb81-107">MediaCollection. Add (método)</span><span class="sxs-lookup"><span data-stu-id="ecb81-107">MediaCollection.add method</span></span>

<span data-ttu-id="ecb81-108">El método **Add** agrega un nuevo elemento multimedia o lista de reproducción a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ecb81-108">The **add** method adds a new media item or playlist to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecb81-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ecb81-109">Syntax</span></span>


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a><span data-ttu-id="ecb81-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecb81-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb81-111">*ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ecb81-111">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ecb81-112">**Cadena** que contiene la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="ecb81-112">**String** containing the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb81-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecb81-113">Return value</span></span>

<span data-ttu-id="ecb81-114">Este método devuelve un objeto **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="ecb81-114">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecb81-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecb81-115">Remarks</span></span>

<span data-ttu-id="ecb81-116">Este método carga un elemento multimedia o una lista de reproducción existente en la biblioteca, dada una ruta de acceso a un archivo.</span><span class="sxs-lookup"><span data-stu-id="ecb81-116">This method loads an existing media item or playlist into the library, given a path to a file.</span></span> <span data-ttu-id="ecb81-117">Este método no mueve ni cambia el archivo.</span><span class="sxs-lookup"><span data-stu-id="ecb81-117">This method does not move or change the file.</span></span> <span data-ttu-id="ecb81-118">Este método produce un error si se proporciona una ruta de acceso local no válida, pero no se comprueba la validez de los archivos multimedia digitales antes de que se agreguen a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ecb81-118">This method fails if given an invalid local path, but digital media files are not checked for validity before they are added to the library.</span></span>

<span data-ttu-id="ecb81-119">Este método acepta archivos de lista de reproducción estática y automática.</span><span class="sxs-lookup"><span data-stu-id="ecb81-119">This method accepts both static and auto playlist files.</span></span> <span data-ttu-id="ecb81-120">*PlaylistCollection*. el método **importPlaylist** también se puede usar para agregar una lista de reproducción estática a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ecb81-120">The *PlaylistCollection*.**importPlaylist** method can also be used to add a static playlist to the library.</span></span>

<span data-ttu-id="ecb81-121">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ecb81-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="ecb81-122">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ecb81-122">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ecb81-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ecb81-123">Examples</span></span>

<span data-ttu-id="ecb81-124">En el siguiente ejemplo de Microsoft JScript se agregan tres objetos multimedia a la colección de medios de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ecb81-124">The following Microsoft JScript example adds three media objects to the Windows Media Player media collection.</span></span> <span data-ttu-id="ecb81-125">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="ecb81-125">The **Player** object was created with ID="Player".</span></span>


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a><span data-ttu-id="ecb81-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecb81-126">Requirements</span></span>



| <span data-ttu-id="ecb81-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecb81-127">Requirement</span></span> | <span data-ttu-id="ecb81-128">Value</span><span class="sxs-lookup"><span data-stu-id="ecb81-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb81-129">Versión</span><span class="sxs-lookup"><span data-stu-id="ecb81-129">Version</span></span><br/> | <span data-ttu-id="ecb81-130">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ecb81-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ecb81-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ecb81-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="ecb81-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecb81-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb81-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecb81-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecb81-134">**Administrar listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="ecb81-134">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="ecb81-135">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="ecb81-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="ecb81-136">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="ecb81-136">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="ecb81-137">**MediaCollection. Remove**</span><span class="sxs-lookup"><span data-stu-id="ecb81-137">**MediaCollection.remove**</span></span>](mediacollection-remove.md)
</dt> <dt>

[<span data-ttu-id="ecb81-138">**PlaylistCollection.importPlaylist**</span><span class="sxs-lookup"><span data-stu-id="ecb81-138">**PlaylistCollection.importPlaylist**</span></span>](playlistcollection-importplaylist.md)
</dt> <dt>

[<span data-ttu-id="ecb81-139">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ecb81-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ecb81-140">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ecb81-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





