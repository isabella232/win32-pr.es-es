---
description: Cuando el filtro del navegador de DVD entra en el modo de karaoke, informa al descodificador de audio a través de la \_ propiedad AM \_ DVDKARAOKE \_ enable.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Conjunto de propiedades de Karaoke de DVD (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e9fe53ad35dac0c3c0f54a8e04a6fbe698fc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679176"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="f8b73-103">Conjunto de propiedades de Karaoke de DVD</span><span class="sxs-lookup"><span data-stu-id="f8b73-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="f8b73-104">Cuando el filtro del [navegador de DVD](dvd-navigator-filter.md) entra en el modo de karaoke, informa al descodificador de audio a través de la **\_ propiedad AM \_ DVDKARAOKE \_ enable** .</span><span class="sxs-lookup"><span data-stu-id="f8b73-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="f8b73-105">A continuación, el descodificador debe silenciar los canales de audio del 2 al 5 hasta que reciba desde el navegador de DVD una propiedad de **\_ \_ \_ datos DVDKARAOKE de la propiedad AM** con un puntero a una estructura de datos [**AM \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) que indique cómo se van a mezclar los canales auxiliares.</span><span class="sxs-lookup"><span data-stu-id="f8b73-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



|                   |                             |
|-------------------|-----------------------------|
| <span data-ttu-id="f8b73-106">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="f8b73-106">Property Set GUID</span></span> | <span data-ttu-id="f8b73-107">\_DvdKaraoke KSPROPSETID \_ AM</span><span class="sxs-lookup"><span data-stu-id="f8b73-107">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="f8b73-108">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="f8b73-108">Property ID</span></span>                      | <span data-ttu-id="f8b73-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8b73-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b73-110">\_propiedad AM \_ DVDKARAOKE \_ enable</span><span class="sxs-lookup"><span data-stu-id="f8b73-110">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="f8b73-111">Valor BOOLEANO.</span><span class="sxs-lookup"><span data-stu-id="f8b73-111">BOOLEAN value.</span></span> <span data-ttu-id="f8b73-112">El navegador de DVD envía al descodificador una \_ propiedad AM \_ DVDKARAOKE \_ enable con un valor de **true** para habilitar Karaoke downmixing o **false** para deshabilitarlo.</span><span class="sxs-lookup"><span data-stu-id="f8b73-112">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="f8b73-113">\_ \_ datos DVDKARAOKE de la propiedad AM \_</span><span class="sxs-lookup"><span data-stu-id="f8b73-113">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="f8b73-114">El navegador de DVD envía al descodificador una \_ \_ propiedad de \_ datos DVDKARAOKE de la propiedad AM con un puntero a una estructura [**AM \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) para cambiar la configuración de downmix; es decir, para activar o desactivar determinados canales de karaoke y dirigirlos al canal de salida derecho o izquierdo.</span><span class="sxs-lookup"><span data-stu-id="f8b73-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f8b73-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8b73-115">Requirements</span></span>



| <span data-ttu-id="f8b73-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8b73-116">Requirement</span></span> | <span data-ttu-id="f8b73-117">Value</span><span class="sxs-lookup"><span data-stu-id="f8b73-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8b73-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8b73-118">Header</span></span><br/> | <dl> <span data-ttu-id="f8b73-119"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8b73-119"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8b73-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8b73-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8b73-121">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="f8b73-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




