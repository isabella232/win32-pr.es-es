---
title: Network. bufferingCount
description: La propiedad bufferingCount recupera el número de veces que se ha producido el almacenamiento en búfer durante la reproducción del clip.
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- Windows Media Player de red. bufferingCount
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708312"
---
# <a name="networkbufferingcount"></a><span data-ttu-id="6260a-104">Network. bufferingCount</span><span class="sxs-lookup"><span data-stu-id="6260a-104">Network.bufferingCount</span></span>

<span data-ttu-id="6260a-105">La propiedad **bufferingCount** recupera el número de veces que se ha producido el almacenamiento en búfer durante la reproducción del clip.</span><span class="sxs-lookup"><span data-stu-id="6260a-105">The **bufferingCount** property retrieves the number of times buffering occurred during clip playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="6260a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6260a-106">Syntax</span></span>

<span data-ttu-id="6260a-107">*reproductor*. *red*. **bufferingCount**</span><span class="sxs-lookup"><span data-stu-id="6260a-107">*player*.*network*.**bufferingCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="6260a-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="6260a-108">Possible Values</span></span>

<span data-ttu-id="6260a-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="6260a-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="6260a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6260a-110">Remarks</span></span>

<span data-ttu-id="6260a-111">Cada vez que se detiene y se reinicia la reproducción, esta propiedad se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="6260a-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="6260a-112">No se restablece si la reproducción está en pausa.</span><span class="sxs-lookup"><span data-stu-id="6260a-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="6260a-113">El almacenamiento en búfer solo se aplica al contenido de streaming.</span><span class="sxs-lookup"><span data-stu-id="6260a-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="6260a-114">Esta propiedad devuelve información válida solo durante el tiempo de ejecución cuando el *reproductor*. La propiedad de **dirección URL** está establecida.</span><span class="sxs-lookup"><span data-stu-id="6260a-114">This property returns valid information only during run time when the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="6260a-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6260a-115">Examples</span></span>

<span data-ttu-id="6260a-116">En el siguiente ejemplo de JScript se usa *Network*. **bufferingCount** para mostrar el número de veces que se produce el almacenamiento en búfer durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="6260a-116">The following JScript example uses *Network*.**bufferingCount** to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="6260a-117">La información se muestra en un DIV HTML creado con ID = "CB".</span><span class="sxs-lookup"><span data-stu-id="6260a-117">The information is displayed in an HTML DIV created with ID = "CB".</span></span> <span data-ttu-id="6260a-118">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="6260a-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="6260a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6260a-119">Requirements</span></span>



| <span data-ttu-id="6260a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6260a-120">Requirement</span></span> | <span data-ttu-id="6260a-121">Value</span><span class="sxs-lookup"><span data-stu-id="6260a-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6260a-122">Versión</span><span class="sxs-lookup"><span data-stu-id="6260a-122">Version</span></span><br/> | <span data-ttu-id="6260a-123">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6260a-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6260a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6260a-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="6260a-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6260a-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6260a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6260a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6260a-127">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="6260a-127">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="6260a-128">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="6260a-128">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





