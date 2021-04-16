---
title: Propiedad maxBandwidth de IWMPNetwork
description: La propiedad maxBandwidth obtiene o establece el ancho de banda máximo permitido.
ms.assetid: ff7548d8-b80f-4cb4-bdd6-86d585fef329
keywords:
- propiedad maxBandwidth Media Player de Windows
- propiedad maxBandwidth Media Player de Windows, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, propiedad maxBandwidth
topic_type:
- apiref
api_name:
- IWMPNetwork.maxBandwidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3620d609db0f1786da673923f54d726b3c99994a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649937"
---
# <a name="iwmpnetworkmaxbandwidth-property"></a><span data-ttu-id="1b44b-106">IWMPNetwork:: maxBandwidth (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1b44b-106">IWMPNetwork::maxBandwidth property</span></span>

<span data-ttu-id="1b44b-107">La propiedad **maxBandwidth** obtiene o establece el ancho de banda máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="1b44b-107">The **maxBandwidth** property gets or sets the maximum allowed bandwidth.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b44b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b44b-108">Syntax</span></span>


```CSharp
public System.Int32 maxBandwidth {get; set;}
```


```VB

Public Property maxBandwidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="1b44b-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1b44b-109">Property value</span></span>

<span data-ttu-id="1b44b-110">**System. Int32** que es el ancho de banda máximo.</span><span class="sxs-lookup"><span data-stu-id="1b44b-110">A **System.Int32** that is the maximum bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b44b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b44b-111">Remarks</span></span>

<span data-ttu-id="1b44b-112">Esta propiedad no tiene un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1b44b-112">This property does not have a default value.</span></span> <span data-ttu-id="1b44b-113">El valor se puede especificar mientras se reproduce Windows Media Player, pero el cambio no surtirá efecto hasta que se libere el elemento multimedia actual; para ello, se abre otro o se llama a **AxWindowsMediaPlayer. Close**.</span><span class="sxs-lookup"><span data-stu-id="1b44b-113">The value can be specified while Windows Media Player is playing, but the change will not take effect until the current media item is released by opening another one or by calling **AxWindowsMediaPlayer.close**.</span></span> <span data-ttu-id="1b44b-114">Windows Media Player intenta lograr el ancho de banda más alto posible.</span><span class="sxs-lookup"><span data-stu-id="1b44b-114">Windows Media Player attempts to achieve the highest bandwidth possible.</span></span> <span data-ttu-id="1b44b-115">No se producirá una reducción intencionada del ancho de banda a menos que se establezca este valor.</span><span class="sxs-lookup"><span data-stu-id="1b44b-115">No intentional reduction of bandwidth will occur unless this value is set.</span></span>

<span data-ttu-id="1b44b-116">Esta configuración es útil para reducir la cantidad de ancho de banda que se usa, especialmente en el caso de una secuencia de velocidad de bits múltiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="1b44b-116">This setting is useful for reducing the amount of bandwidth used, particularly in the case of a multiple bit rate (MBR) stream.</span></span> <span data-ttu-id="1b44b-117">Una secuencia MBR contiene varias secuencias con velocidades de bits diferentes.</span><span class="sxs-lookup"><span data-stu-id="1b44b-117">An MBR stream contains multiple streams with different bit rates.</span></span> <span data-ttu-id="1b44b-118">En algunos casos, puede ser conveniente usar una secuencia con una velocidad de bits menor que la que requiere el cliente.</span><span class="sxs-lookup"><span data-stu-id="1b44b-118">In some cases, it may be desirable to use a stream with a lower bit rate than the client requires.</span></span> <span data-ttu-id="1b44b-119">En este caso, si se especifica una velocidad de bits inferior con la propiedad **IWMPNetwork. maxBandwidth** , se seleccionará una secuencia de velocidad de bits inferior.</span><span class="sxs-lookup"><span data-stu-id="1b44b-119">In this case, specifying a lower bit rate with the **IWMPNetwork.maxBandwidth** property will select a lower bit-rate stream.</span></span> <span data-ttu-id="1b44b-120">Por ejemplo, una secuencia MBR podría incluir secuencias codificadas a 20 kilobits por segundo (kbps), 37 Kbps y 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="1b44b-120">For example, an MBR stream might include streams encoded at 20 kilobits per second (Kbps), 37 Kbps, and 200 Kbps.</span></span> <span data-ttu-id="1b44b-121">El uso de **IWMPNetwork. maxBandwidth** para especificar una velocidad de bits de 50.000 (50 Kbps) seleccionará la secuencia de 37 kbps en lugar de la secuencia de 200 Kbps.</span><span class="sxs-lookup"><span data-stu-id="1b44b-121">Using **IWMPNetwork.maxBandwidth** to specify a bit rate of 50,000 (50 Kbps) will select the 37 Kbps stream instead of the 200 Kbps stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b44b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b44b-122">Requirements</span></span>



| <span data-ttu-id="1b44b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b44b-123">Requirement</span></span> | <span data-ttu-id="1b44b-124">Value</span><span class="sxs-lookup"><span data-stu-id="1b44b-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b44b-125">Versión</span><span class="sxs-lookup"><span data-stu-id="1b44b-125">Version</span></span><br/>   | <span data-ttu-id="1b44b-126">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="1b44b-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1b44b-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1b44b-127">Namespace</span></span><br/> | <span data-ttu-id="1b44b-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1b44b-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1b44b-129">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="1b44b-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1b44b-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1b44b-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b44b-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b44b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b44b-132">**AxWindowsMediaPlayer. Close (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1b44b-132">**AxWindowsMediaPlayer.close (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-close.md)
</dt> <dt>

[<span data-ttu-id="1b44b-133">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1b44b-133">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





