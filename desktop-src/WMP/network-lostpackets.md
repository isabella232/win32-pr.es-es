---
title: Network. lostPackets
description: La propiedad lostPackets recupera el número de paquetes perdidos.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Windows Media Player de red. lostPackets
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649844"
---
# <a name="networklostpackets"></a><span data-ttu-id="fe778-104">Network. lostPackets</span><span class="sxs-lookup"><span data-stu-id="fe778-104">Network.lostPackets</span></span>

<span data-ttu-id="fe778-105">La propiedad **lostPackets** recupera el número de paquetes perdidos.</span><span class="sxs-lookup"><span data-stu-id="fe778-105">The **lostPackets** property retrieves the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe778-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe778-106">Syntax</span></span>

<span data-ttu-id="fe778-107">*reproductor*. *red*. **lostPackets**</span><span class="sxs-lookup"><span data-stu-id="fe778-107">*player*.*network*.**lostPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fe778-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="fe778-108">Possible Values</span></span>

<span data-ttu-id="fe778-109">Esta propiedad es un **número** de solo lectura (**Long**).</span><span class="sxs-lookup"><span data-stu-id="fe778-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe778-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fe778-110">Remarks</span></span>

<span data-ttu-id="fe778-111">Esta propiedad solo es válida para streaming multimedia y será igual a cero cuando se use el protocolo HTTP, que es sin pérdida.</span><span class="sxs-lookup"><span data-stu-id="fe778-111">This property is only valid for streaming media, and will equal zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="fe778-112">Los paquetes se pueden perder por una serie de motivos, como el tipo y la calidad de la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="fe778-112">Packets may be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="fe778-113">Cada vez que se detiene y se reinicia la reproducción, esta propiedad se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="fe778-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="fe778-114">No se restablece si la reproducción se pausa y se reinicia.</span><span class="sxs-lookup"><span data-stu-id="fe778-114">It is not reset if playback is paused and restarted.</span></span> <span data-ttu-id="fe778-115">Esta propiedad devuelve información válida solo durante el tiempo de ejecución y solo si el *reproductor*. La propiedad de **dirección URL** está establecida.</span><span class="sxs-lookup"><span data-stu-id="fe778-115">This property returns valid information only during run time, and only if the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="fe778-116">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="fe778-116">Examples</span></span>

<span data-ttu-id="fe778-117">En el siguiente ejemplo de JScript se usa *Network*. **lostPackets** para mostrar el número total de paquetes perdidos durante la reproducción cuando el usuario hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="fe778-117">The following JScript example uses *Network*.**lostPackets** to display the total number of packets lost during playback when the user clicks a button.</span></span> <span data-ttu-id="fe778-118">La información se muestra en un DIV HTML creado con ID = "LP".</span><span class="sxs-lookup"><span data-stu-id="fe778-118">The information is displayed in an HTML DIV created with ID = "LP".</span></span> <span data-ttu-id="fe778-119">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="fe778-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a><span data-ttu-id="fe778-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe778-120">Requirements</span></span>



| <span data-ttu-id="fe778-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe778-121">Requirement</span></span> | <span data-ttu-id="fe778-122">Value</span><span class="sxs-lookup"><span data-stu-id="fe778-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe778-123">Versión</span><span class="sxs-lookup"><span data-stu-id="fe778-123">Version</span></span><br/> | <span data-ttu-id="fe778-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="fe778-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fe778-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fe778-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe778-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe778-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe778-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe778-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe778-128">**Objeto de red**</span><span class="sxs-lookup"><span data-stu-id="fe778-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="fe778-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="fe778-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





