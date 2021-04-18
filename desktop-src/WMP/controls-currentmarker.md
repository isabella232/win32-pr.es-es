---
title: Controls. currentMarker
description: La propiedad currentMarker especifica o recupera el número de marcador actual.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Media Player de Windows Controls. currentMarker
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699928"
---
# <a name="controlscurrentmarker"></a><span data-ttu-id="cc79a-104">Controls. currentMarker</span><span class="sxs-lookup"><span data-stu-id="cc79a-104">Controls.currentMarker</span></span>

<span data-ttu-id="cc79a-105">La propiedad **currentMarker** especifica o recupera el número de marcador actual.</span><span class="sxs-lookup"><span data-stu-id="cc79a-105">The **currentMarker** property specifies or retrieves the current marker number.</span></span>

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a><span data-ttu-id="cc79a-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="cc79a-106">Possible Values</span></span>

<span data-ttu-id="cc79a-107">Esta propiedad es un **número** de lectura y escritura (**Long**) con un valor predeterminado de cero.</span><span class="sxs-lookup"><span data-stu-id="cc79a-107">This property is a read/write **Number** (**long**) with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc79a-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc79a-108">Remarks</span></span>

<span data-ttu-id="cc79a-109">La configuración de **currentMarker** hace que la reproducción se inicie desde el marcador especificado.</span><span class="sxs-lookup"><span data-stu-id="cc79a-109">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="cc79a-110">Antes de intentar establecer **currentMarker**, determine si un archivo tiene marcadores y cuántos tiene con **markerCount**.</span><span class="sxs-lookup"><span data-stu-id="cc79a-110">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **markerCount**.</span></span> <span data-ttu-id="cc79a-111">Si un archivo no tiene marcadores, si se establece **currentMarker** en cualquier cosa pero cero, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="cc79a-111">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="cc79a-112">Establecer **currentMarker** en un número mayor que **markerCount** también produce un error.</span><span class="sxs-lookup"><span data-stu-id="cc79a-112">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="cc79a-113">La propiedad **currentMarker** siempre devuelve el marcador actual o el último, lo que significa que la posición del archivo real puede estar en el marcador actual o antes del marcador siguiente.</span><span class="sxs-lookup"><span data-stu-id="cc79a-113">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="cc79a-114">Los marcadores se numeran a partir de 1, por lo que si un archivo tiene marcadores, puede establecer **currentMarker** en cero para cambiar la posición del archivo a cero.</span><span class="sxs-lookup"><span data-stu-id="cc79a-114">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="cc79a-115">Hasta que se establezca el elemento multimedia actual (mediante *Player*.**Dirección URL** o *reproductor*. **currentMedia**), **currentMarker** devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cc79a-115">Until the current media item is set (using *Player*.**URL** or *Player*.**currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="cc79a-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cc79a-116">Examples</span></span>

<span data-ttu-id="cc79a-117">En el siguiente ejemplo de JScript se usa **currentMarker** para iniciar la reproducción de vídeo desde el marcador que corresponde a la propiedad **SelectedIndex** de un elemento Select de HTML.</span><span class="sxs-lookup"><span data-stu-id="cc79a-117">The following JScript example uses **currentMarker** to start video playback from the marker that corresponds to the **selectedIndex** property of an HTML SELECT element.</span></span> <span data-ttu-id="cc79a-118">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="cc79a-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="cc79a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc79a-119">Requirements</span></span>



| <span data-ttu-id="cc79a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc79a-120">Requirement</span></span> | <span data-ttu-id="cc79a-121">Value</span><span class="sxs-lookup"><span data-stu-id="cc79a-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cc79a-122">Versión</span><span class="sxs-lookup"><span data-stu-id="cc79a-122">Version</span></span><br/> | <span data-ttu-id="cc79a-123">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="cc79a-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cc79a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc79a-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="cc79a-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc79a-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc79a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc79a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc79a-127">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="cc79a-127">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="cc79a-128">**Media. markerCount**</span><span class="sxs-lookup"><span data-stu-id="cc79a-128">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="cc79a-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="cc79a-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="cc79a-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="cc79a-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





