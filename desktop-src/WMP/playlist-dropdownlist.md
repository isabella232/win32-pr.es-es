---
title: Lista de reproducción. dropDownList
description: El atributo dropDownList especifica o recupera un valor que indica qué elementos se muestran en el cuadro de lista desplegable para una instancia determinada del elemento PLAYLIST.
ms.assetid: 583041b0-25dc-4015-a3b2-37f3cfdcd496
keywords:
- Lista de reproducción. dropDownList Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.dropDownList
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acf98dec7d50e2a3cd0b53acc07b0b8695f8461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708302"
---
# <a name="playlistdropdownlist"></a><span data-ttu-id="7eeb7-104">Lista de reproducción. dropDownList</span><span class="sxs-lookup"><span data-stu-id="7eeb7-104">PLAYLIST.dropDownList</span></span>

<span data-ttu-id="7eeb7-105">El atributo **dropDownList** especifica o recupera un valor que indica qué elementos se muestran en el cuadro de lista desplegable para una instancia determinada del elemento **playlist** .</span><span class="sxs-lookup"><span data-stu-id="7eeb7-105">The **dropDownList** attribute specifies or retrieves a value indicating which elements show up in the drop-down list box for a given instance of the **PLAYLIST** element.</span></span>

``` syntax
        elementID.dropDownList
```

## <a name="possible-values"></a><span data-ttu-id="7eeb7-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="7eeb7-106">Possible Values</span></span>

<span data-ttu-id="7eeb7-107">Este atributo es una **cadena** de lectura/escritura que contiene uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="7eeb7-108">Value</span><span class="sxs-lookup"><span data-stu-id="7eeb7-108">Value</span></span>       | <span data-ttu-id="7eeb7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="7eeb7-109">Description</span></span>                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eeb7-110">showAlbums</span><span class="sxs-lookup"><span data-stu-id="7eeb7-110">showAlbums</span></span>  | <span data-ttu-id="7eeb7-111">Muestra álbumes.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-111">Shows albums.</span></span>                                                                                    |
| <span data-ttu-id="7eeb7-112">showAll</span><span class="sxs-lookup"><span data-stu-id="7eeb7-112">showAll</span></span>     | <span data-ttu-id="7eeb7-113">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-113">Default.</span></span> <span data-ttu-id="7eeb7-114">Muestra todos los elementos disponibles, como listas de reproducción de CD, listas de reproducción de usuario y valores preestablecidos de radio.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-114">Shows all available elements including CD playlists, user playlists, and radio presets.</span></span> |
| <span data-ttu-id="7eeb7-115">showCD</span><span class="sxs-lookup"><span data-stu-id="7eeb7-115">showCD</span></span>      | <span data-ttu-id="7eeb7-116">Muestra la lista de reproducción del CD.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-116">Shows the CD playlist.</span></span>                                                                           |
| <span data-ttu-id="7eeb7-117">showClips</span><span class="sxs-lookup"><span data-stu-id="7eeb7-117">showClips</span></span>   | <span data-ttu-id="7eeb7-118">Muestra todos los clips.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-118">Shows all clips.</span></span>                                                                                 |
| <span data-ttu-id="7eeb7-119">showCurrent</span><span class="sxs-lookup"><span data-stu-id="7eeb7-119">showCurrent</span></span> | <span data-ttu-id="7eeb7-120">Muestra la lista de reproducción actual y no guardada.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-120">Shows the current, unsaved playlist.</span></span>                                                             |
| <span data-ttu-id="7eeb7-121">showLibrary</span><span class="sxs-lookup"><span data-stu-id="7eeb7-121">showLibrary</span></span> | <span data-ttu-id="7eeb7-122">Muestra solo listas de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-122">Shows only library playlists.</span></span>                                                                    |
| <span data-ttu-id="7eeb7-123">showRadio</span><span class="sxs-lookup"><span data-stu-id="7eeb7-123">showRadio</span></span>   | <span data-ttu-id="7eeb7-124">Muestra los valores preestablecidos de radio.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-124">Shows radio presets.</span></span>                                                                             |
| <span data-ttu-id="7eeb7-125">showQueries</span><span class="sxs-lookup"><span data-stu-id="7eeb7-125">showQueries</span></span> | <span data-ttu-id="7eeb7-126">Muestra las consultas.</span><span class="sxs-lookup"><span data-stu-id="7eeb7-126">Shows queries.</span></span>                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="7eeb7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eeb7-127">Requirements</span></span>



| <span data-ttu-id="7eeb7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eeb7-128">Requirement</span></span> | <span data-ttu-id="7eeb7-129">Value</span><span class="sxs-lookup"><span data-stu-id="7eeb7-129">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="7eeb7-130">Versión</span><span class="sxs-lookup"><span data-stu-id="7eeb7-130">Version</span></span><br/> | <span data-ttu-id="7eeb7-131">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="7eeb7-131">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7eeb7-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="7eeb7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eeb7-133">**Elemento PLAYLIST**</span><span class="sxs-lookup"><span data-stu-id="7eeb7-133">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





