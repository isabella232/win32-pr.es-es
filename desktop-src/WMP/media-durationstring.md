---
title: Media. durationString
description: La propiedad durationString recupera un valor de cadena que indica la duración del elemento multimedia actual en formato HH MM SS.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media Player Windows Media. durationString
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709097"
---
# <a name="mediadurationstring"></a><span data-ttu-id="90183-104">Media. durationString</span><span class="sxs-lookup"><span data-stu-id="90183-104">Media.durationString</span></span>

<span data-ttu-id="90183-105">La propiedad **durationString** recupera un valor de **cadena** que indica la duración del elemento multimedia actual en formato HH: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="90183-105">The **durationString** property retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span>

## <a name="syntax"></a><span data-ttu-id="90183-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="90183-106">Syntax</span></span>

<span data-ttu-id="90183-107">*reproductor*. *currentMedia*. **durationString**</span><span class="sxs-lookup"><span data-stu-id="90183-107">*player*.*currentMedia*.**durationString**</span></span>

## <a name="possible-values"></a><span data-ttu-id="90183-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="90183-108">Possible Values</span></span>

<span data-ttu-id="90183-109">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="90183-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="90183-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90183-110">Remarks</span></span>

<span data-ttu-id="90183-111">Si esta propiedad se utiliza con un elemento multimedia distinto del especificado en el *reproductor*. **currentMedia**, puede que no contenga un valor válido.</span><span class="sxs-lookup"><span data-stu-id="90183-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span> <span data-ttu-id="90183-112">Si el elemento multimedia tiene una longitud inferior a una hora, se omite la parte HH: del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="90183-112">If the media item is less than an hour long, the HH: portion of the return value is omitted.</span></span>

<span data-ttu-id="90183-113">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="90183-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="90183-114">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="90183-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="90183-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="90183-115">Examples</span></span>

<span data-ttu-id="90183-116">En el siguiente ejemplo de JScript se utiliza el *medio*. **durationString** para mostrar la duración del elemento multimedia actual como texto con formato.</span><span class="sxs-lookup"><span data-stu-id="90183-116">The following JScript example uses *Media*.**durationString** to display the duration of the current media item as formatted text.</span></span> <span data-ttu-id="90183-117">Un elemento HTML DIV denominado MediaInfo muestra la información de duración.</span><span class="sxs-lookup"><span data-stu-id="90183-117">An HTML DIV element named MediaInfo displays the duration information.</span></span> <span data-ttu-id="90183-118">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="90183-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="90183-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90183-119">Requirements</span></span>



| <span data-ttu-id="90183-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="90183-120">Requirement</span></span> | <span data-ttu-id="90183-121">Value</span><span class="sxs-lookup"><span data-stu-id="90183-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="90183-122">Versión</span><span class="sxs-lookup"><span data-stu-id="90183-122">Version</span></span><br/> | <span data-ttu-id="90183-123">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="90183-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="90183-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="90183-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="90183-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90183-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90183-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="90183-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90183-127">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="90183-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="90183-128">**Media. Duration**</span><span class="sxs-lookup"><span data-stu-id="90183-128">**Media.duration**</span></span>](media-duration.md)
</dt> <dt>

[<span data-ttu-id="90183-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="90183-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="90183-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="90183-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="90183-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="90183-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





