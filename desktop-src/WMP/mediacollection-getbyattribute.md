---
title: MediaCollection. getByAttribute, método
description: El método getByAttribute recupera una lista de reproducción de elementos multimedia que contienen un valor especificado para un atributo especificado.
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- método getByAttribute de Windows Media Player
- método getByAttribute de Windows Media Player, clase MediaCollection
- Clase MediaCollection Windows Media Player, método getByAttribute
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690636"
---
# <a name="mediacollectiongetbyattribute-method"></a><span data-ttu-id="5891d-106">MediaCollection. getByAttribute, método</span><span class="sxs-lookup"><span data-stu-id="5891d-106">MediaCollection.getByAttribute method</span></span>

<span data-ttu-id="5891d-107">El método **getByAttribute** recupera una lista de reproducción de elementos multimedia que contienen un valor especificado para un atributo especificado.</span><span class="sxs-lookup"><span data-stu-id="5891d-107">The **getByAttribute** method retrieves a playlist of media items that contain a specified value for a specified attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="5891d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5891d-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="5891d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5891d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5891d-110">*atributo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5891d-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891d-111">**Cadena** que indica el nombre del atributo que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="5891d-111">**String** indicating the name of the attribute to search.</span></span> <span data-ttu-id="5891d-112">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5891d-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="5891d-113">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="5891d-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5891d-114">**Cadena** que indica el valor que debe tener el atributo.</span><span class="sxs-lookup"><span data-stu-id="5891d-114">**String** indicating the value that the attribute should have.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5891d-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5891d-115">Return value</span></span>

<span data-ttu-id="5891d-116">Este método devuelve un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="5891d-116">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5891d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5891d-117">Remarks</span></span>

<span data-ttu-id="5891d-118">Este método se puede utilizar para crear una consulta genérica para los elementos multimedia que coinciden con un valor para un atributo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5891d-118">This method can be used to create a generic query for media items that match a value for an attribute in the database.</span></span> <span data-ttu-id="5891d-119">Esto es útil en el caso de los atributos definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="5891d-119">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="5891d-120">Si el atributo no existe, se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="5891d-120">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="5891d-121">Puede utilizar este método para recuperar todos los elementos multimedia de un tipo específico.</span><span class="sxs-lookup"><span data-stu-id="5891d-121">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="5891d-122">Use el nombre de atributo "MediaType" y uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="5891d-122">Use the attribute name "MediaType" and one of the following values:</span></span>



| <span data-ttu-id="5891d-123">Value</span><span class="sxs-lookup"><span data-stu-id="5891d-123">Value</span></span>    | <span data-ttu-id="5891d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="5891d-124">Description</span></span>                                                |
|----------|------------------------------------------------------------|
| <span data-ttu-id="5891d-125">audio</span><span class="sxs-lookup"><span data-stu-id="5891d-125">audio</span></span>    | <span data-ttu-id="5891d-126">Música y otros elementos de solo audio.</span><span class="sxs-lookup"><span data-stu-id="5891d-126">Music and other audio-only items.</span></span>                          |
| <span data-ttu-id="5891d-127">automáticas</span><span class="sxs-lookup"><span data-stu-id="5891d-127">playlist</span></span> | <span data-ttu-id="5891d-128">Listas de reproducción representadas como objetos **multimedia** .</span><span class="sxs-lookup"><span data-stu-id="5891d-128">Playlists represented as **Media** objects.</span></span>                |
| <span data-ttu-id="5891d-129">radio</span><span class="sxs-lookup"><span data-stu-id="5891d-129">radio</span></span>    | <span data-ttu-id="5891d-130">Elementos de la estación de radio.</span><span class="sxs-lookup"><span data-stu-id="5891d-130">Radio station items.</span></span> <span data-ttu-id="5891d-131">No lo usa Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="5891d-131">Not used by Windows Media Player 10.</span></span>  |
| <span data-ttu-id="5891d-132">video</span><span class="sxs-lookup"><span data-stu-id="5891d-132">video</span></span>    | <span data-ttu-id="5891d-133">Elementos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5891d-133">Video items.</span></span>                                               |
| <span data-ttu-id="5891d-134">álbum</span><span class="sxs-lookup"><span data-stu-id="5891d-134">photo</span></span>    | <span data-ttu-id="5891d-135">Elementos de fotografía.</span><span class="sxs-lookup"><span data-stu-id="5891d-135">Photo items.</span></span> <span data-ttu-id="5891d-136">Requiere Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="5891d-136">Requires Windows Media Player 10.</span></span>             |
| <span data-ttu-id="5891d-137">Otros</span><span class="sxs-lookup"><span data-stu-id="5891d-137">other</span></span>    | <span data-ttu-id="5891d-138">Otros elementos, como archivos ASF o direcciones URL, a medios de streaming.</span><span class="sxs-lookup"><span data-stu-id="5891d-138">Other items, such as ASF files or URLs to streaming media.</span></span> |



 

<span data-ttu-id="5891d-139">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="5891d-139">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5891d-140">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5891d-140">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5891d-141">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5891d-141">Examples</span></span>

<span data-ttu-id="5891d-142">En el siguiente ejemplo de JScript se usa *MediaCollection*. **getByAttribute** para reproducir todo el contenido de la biblioteca por el intérprete llamado Triode 48.</span><span class="sxs-lookup"><span data-stu-id="5891d-142">The following JScript example uses *MediaCollection*.**getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="5891d-143">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5891d-143">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="5891d-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5891d-144">Requirements</span></span>



| <span data-ttu-id="5891d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="5891d-145">Requirement</span></span> | <span data-ttu-id="5891d-146">Value</span><span class="sxs-lookup"><span data-stu-id="5891d-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5891d-147">Versión</span><span class="sxs-lookup"><span data-stu-id="5891d-147">Version</span></span><br/> | <span data-ttu-id="5891d-148">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5891d-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5891d-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5891d-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="5891d-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5891d-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5891d-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="5891d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5891d-152">**Objeto MediaCollection**</span><span class="sxs-lookup"><span data-stu-id="5891d-152">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="5891d-153">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="5891d-153">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="5891d-154">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5891d-154">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5891d-155">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5891d-155">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





