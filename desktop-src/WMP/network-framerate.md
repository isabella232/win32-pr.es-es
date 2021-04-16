---
title: Red. velocidad de fotogramas
description: La propiedad de velocidad de fotogramas recupera la velocidad actual de fotogramas de vídeo en fotogramas por cien segundos. Por ejemplo, un valor de 2998 indica 29,98 fotogramas por segundo.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Red. velocidad de Media Player de Windows
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708972"
---
# <a name="networkframerate"></a><span data-ttu-id="2130f-105">Red. velocidad de fotogramas</span><span class="sxs-lookup"><span data-stu-id="2130f-105">Network.frameRate</span></span>

<span data-ttu-id="2130f-106">La propiedad de **velocidad** de fotogramas recupera la velocidad actual de fotogramas de vídeo en fotogramas por cien segundos.</span><span class="sxs-lookup"><span data-stu-id="2130f-106">The **frameRate** property retrieves the current video frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="2130f-107">Por ejemplo, un valor de 2998 indica 29,98 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="2130f-107">For example, a value of 2998 indicates 29.98 frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="2130f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2130f-108">Syntax</span></span>

<span data-ttu-id="2130f-109">*reproductor*. *red*. **velocidad de fotograma**</span><span class="sxs-lookup"><span data-stu-id="2130f-109">*player*.*network*.**frameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="2130f-110">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="2130f-110">Possible Values</span></span>

<span data-ttu-id="2130f-111">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="2130f-111">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="2130f-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2130f-112">Examples</span></span>

<span data-ttu-id="2130f-113">En el siguiente ejemplo de JScript se usa *Network*. **velocidad de** fotogramas para mostrar la velocidad de fotogramas actual.</span><span class="sxs-lookup"><span data-stu-id="2130f-113">The following JScript example uses *Network*.**frameRate** to display the current frame rate.</span></span> <span data-ttu-id="2130f-114">La información se muestra en un DIV HTML creado con ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="2130f-114">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="2130f-115">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="2130f-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="2130f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2130f-116">Requirements</span></span>



| <span data-ttu-id="2130f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2130f-117">Requirement</span></span> | <span data-ttu-id="2130f-118">Value</span><span class="sxs-lookup"><span data-stu-id="2130f-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2130f-119">Versión</span><span class="sxs-lookup"><span data-stu-id="2130f-119">Version</span></span><br/> | <span data-ttu-id="2130f-120">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="2130f-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2130f-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2130f-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="2130f-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2130f-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2130f-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2130f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2130f-124">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="2130f-124">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="2130f-125">**Network. encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="2130f-125">**Network.encodedFrameRate**</span></span>](network-encodedframerate.md)
</dt> </dl>

 

 





