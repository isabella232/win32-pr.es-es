---
title: Red. ancho de banda
description: La propiedad de ancho de banda recupera el ancho de banda actual del clip.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Red. ancho de banda Media Player Windows
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708641"
---
# <a name="networkbandwidth"></a><span data-ttu-id="50b10-104">Red. ancho de banda</span><span class="sxs-lookup"><span data-stu-id="50b10-104">Network.bandWidth</span></span>

<span data-ttu-id="50b10-105">La propiedad de **ancho** de banda recupera el ancho de banda actual del clip.</span><span class="sxs-lookup"><span data-stu-id="50b10-105">The **bandWidth** property retrieves the current bandwidth of the clip.</span></span>

## <a name="syntax"></a><span data-ttu-id="50b10-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50b10-106">Syntax</span></span>

<span data-ttu-id="50b10-107">*reproductor*. *red*. **ancho de banda**</span><span class="sxs-lookup"><span data-stu-id="50b10-107">*player*.*network*.**bandWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="50b10-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="50b10-108">Possible Values</span></span>

<span data-ttu-id="50b10-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="50b10-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="50b10-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="50b10-110">Remarks</span></span>

<span data-ttu-id="50b10-111">Esta propiedad devuelve cero si el *reproductor*. La propiedad de **dirección URL** no está establecida.</span><span class="sxs-lookup"><span data-stu-id="50b10-111">This property returns zero if the *Player*.**URL** property is not set.</span></span> <span data-ttu-id="50b10-112">Esta propiedad solo es válida para streaming multimedia.</span><span class="sxs-lookup"><span data-stu-id="50b10-112">This property is only valid for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="50b10-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="50b10-113">Examples</span></span>

<span data-ttu-id="50b10-114">En el siguiente ejemplo de Microsoft JScript se usa *Network*. **ancho de banda** para mostrar el ancho de banda multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="50b10-114">The following Microsoft JScript example uses *Network*.**bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="50b10-115">La información se muestra en un DIV HTML creado con ID = "BW".</span><span class="sxs-lookup"><span data-stu-id="50b10-115">The information is displayed in an HTML DIV created with ID = "BW".</span></span> <span data-ttu-id="50b10-116">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="50b10-116">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="50b10-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50b10-117">Requirements</span></span>



| <span data-ttu-id="50b10-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="50b10-118">Requirement</span></span> | <span data-ttu-id="50b10-119">Value</span><span class="sxs-lookup"><span data-stu-id="50b10-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50b10-120">Versión</span><span class="sxs-lookup"><span data-stu-id="50b10-120">Version</span></span><br/> | <span data-ttu-id="50b10-121">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="50b10-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="50b10-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="50b10-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="50b10-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50b10-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50b10-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="50b10-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50b10-125">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="50b10-125">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="50b10-126">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="50b10-126">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





