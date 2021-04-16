---
title: Network. encodedFrameRate
description: La propiedad encodedFrameRate recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido en fotogramas por segundo.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Windows Media Player de red. encodedFrameRate
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709013"
---
# <a name="networkencodedframerate"></a><span data-ttu-id="1569a-104">Network. encodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="1569a-104">Network.encodedFrameRate</span></span>

<span data-ttu-id="1569a-105">La propiedad **encodedFrameRate** recupera la velocidad de fotogramas de vídeo especificada por el autor del contenido en fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="1569a-105">The **encodedFrameRate** property retrieves the video frame rate specified by the content author in frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="1569a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1569a-106">Syntax</span></span>

<span data-ttu-id="1569a-107">*reproductor*. *red*. **encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="1569a-107">*player*.*network*.**encodedFrameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="1569a-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="1569a-108">Possible Values</span></span>

<span data-ttu-id="1569a-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="1569a-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="1569a-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1569a-110">Examples</span></span>

<span data-ttu-id="1569a-111">En el siguiente ejemplo de JScript se usa *Network*. **encodedFrameRate** para mostrar la velocidad de fotogramas especificada al codificar el archivo.</span><span class="sxs-lookup"><span data-stu-id="1569a-111">The following JScript example uses *Network*.**encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="1569a-112">La información se muestra en un DIV HTML creado con ID = "FR".</span><span class="sxs-lookup"><span data-stu-id="1569a-112">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="1569a-113">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1569a-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="1569a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1569a-114">Requirements</span></span>



| <span data-ttu-id="1569a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1569a-115">Requirement</span></span> | <span data-ttu-id="1569a-116">Value</span><span class="sxs-lookup"><span data-stu-id="1569a-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1569a-117">Versión</span><span class="sxs-lookup"><span data-stu-id="1569a-117">Version</span></span><br/> | <span data-ttu-id="1569a-118">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1569a-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1569a-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1569a-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="1569a-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1569a-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1569a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1569a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1569a-122">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="1569a-122">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="1569a-123">**Red. velocidad de fotogramas**</span><span class="sxs-lookup"><span data-stu-id="1569a-123">**Network.frameRate**</span></span>](network-framerate.md)
</dt> </dl>

 

 





