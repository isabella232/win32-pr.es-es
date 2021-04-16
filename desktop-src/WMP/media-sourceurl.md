---
title: Media. sourceURL
description: La propiedad sourceURL recupera la dirección URL del elemento multimedia.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- Media Player Windows Media. sourceURL
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699953"
---
# <a name="mediasourceurl"></a><span data-ttu-id="aa0b6-104">Media. sourceURL</span><span class="sxs-lookup"><span data-stu-id="aa0b6-104">Media.sourceURL</span></span>

<span data-ttu-id="aa0b6-105">La propiedad **sourceURL** recupera la dirección URL del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="aa0b6-105">The **sourceURL** property retrieves the URL of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0b6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa0b6-106">Syntax</span></span>

<span data-ttu-id="aa0b6-107">*reproductor*. *currentMedia*. sourceURL</span><span class="sxs-lookup"><span data-stu-id="aa0b6-107">*player*.*currentMedia*.sourceURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="aa0b6-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="aa0b6-108">Possible Values</span></span>

<span data-ttu-id="aa0b6-109">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aa0b6-109">This property is a read-only **String**.</span></span>

## <a name="examples"></a><span data-ttu-id="aa0b6-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="aa0b6-110">Examples</span></span>

<span data-ttu-id="aa0b6-111">En el siguiente ejemplo de JScript se utiliza el *medio*. **sourceURL** para recuperar la dirección URL del primer elemento multimedia de la lista de reproducción de ejemplo; la dirección URL del elemento multimedia se asigna entonces a la propiedad **dirección URL** del objeto de reproductor.</span><span class="sxs-lookup"><span data-stu-id="aa0b6-111">The following JScript example uses *Media*.**sourceURL** to retrieve the URL of the first media item in the sample playlist; the URL of the media item is then assigned to the player object **URL** property.</span></span> <span data-ttu-id="aa0b6-112">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="aa0b6-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="aa0b6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa0b6-113">Requirements</span></span>



| <span data-ttu-id="aa0b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa0b6-114">Requirement</span></span> | <span data-ttu-id="aa0b6-115">Value</span><span class="sxs-lookup"><span data-stu-id="aa0b6-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0b6-116">Versión</span><span class="sxs-lookup"><span data-stu-id="aa0b6-116">Version</span></span><br/> | <span data-ttu-id="aa0b6-117">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="aa0b6-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="aa0b6-118">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa0b6-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="aa0b6-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa0b6-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa0b6-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa0b6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa0b6-121">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="aa0b6-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





