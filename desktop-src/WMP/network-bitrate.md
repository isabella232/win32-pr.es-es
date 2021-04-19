---
title: Red. velocidad de bits
description: La propiedad de velocidad de bits recupera la velocidad de bits actual recibida.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Red. velocidad de bits de Windows Media Player
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708639"
---
# <a name="networkbitrate"></a><span data-ttu-id="5546b-104">Red. velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="5546b-104">Network.bitRate</span></span>

<span data-ttu-id="5546b-105">La propiedad de **velocidad** de bits recupera la velocidad de bits actual recibida.</span><span class="sxs-lookup"><span data-stu-id="5546b-105">The **bitRate** property retrieves the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="5546b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5546b-106">Syntax</span></span>

<span data-ttu-id="5546b-107">*reproductor*. *red*. **velocidad de bits**</span><span class="sxs-lookup"><span data-stu-id="5546b-107">*player*.*network*.**bitRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="5546b-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="5546b-108">Possible Values</span></span>

<span data-ttu-id="5546b-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="5546b-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5546b-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5546b-110">Remarks</span></span>

<span data-ttu-id="5546b-111">Este valor es una combinación de las velocidades de bits de las secuencias de audio y vídeo actuales.</span><span class="sxs-lookup"><span data-stu-id="5546b-111">This value is a combination of the bit rates of both the current video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="5546b-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5546b-112">Examples</span></span>

<span data-ttu-id="5546b-113">En el siguiente ejemplo de JScript se usa *Network*. **velocidad** de bits para mostrar la velocidad de bits multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="5546b-113">The following JScript example uses *Network*.**bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="5546b-114">La información se muestra en un DIV HTML creado con ID = "BR".</span><span class="sxs-lookup"><span data-stu-id="5546b-114">The information is displayed in an HTML DIV created with ID = "BR".</span></span> <span data-ttu-id="5546b-115">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="5546b-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

         break;

      default:
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="5546b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5546b-116">Requirements</span></span>



| <span data-ttu-id="5546b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5546b-117">Requirement</span></span> | <span data-ttu-id="5546b-118">Value</span><span class="sxs-lookup"><span data-stu-id="5546b-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5546b-119">Versión</span><span class="sxs-lookup"><span data-stu-id="5546b-119">Version</span></span><br/> | <span data-ttu-id="5546b-120">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5546b-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5546b-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5546b-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="5546b-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5546b-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5546b-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5546b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5546b-124">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="5546b-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





