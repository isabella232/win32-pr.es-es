---
description: Cuando el filtro navegador de DVD entra en modo de vídeo, informa al descodificador de audio a través de la propiedad \_ \_ DVDKARAOKE ENABLE de AM \_ PROPERTY.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Conjunto de propiedades DVD Dvd Dvd Dvdmedia.h
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909073"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="f531a-103">Conjunto de propiedades DVD Dvd Dvd</span><span class="sxs-lookup"><span data-stu-id="f531a-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="f531a-104">Cuando el [filtro navegador de DVD](dvd-navigator-filter.md) entra en modo de vídeo, informa al descodificador de audio a través de la propiedad **\_ \_ DVDKARAOKE \_ ENABLE de AM PROPERTY.**</span><span class="sxs-lookup"><span data-stu-id="f531a-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="f531a-105">A continuación, el descodificador debe silenciar los canales de audio del 2 al 5 hasta que reciba desde el navegador de DVD una propiedad DE AM **\_ PROPERTY \_ DVDKARAOKE \_ DATA** con un puntero a una estructura de datos [**\_ DVDKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) de AM que indica cómo se van a mezclar los canales auxiliares.</span><span class="sxs-lookup"><span data-stu-id="f531a-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



| <span data-ttu-id="f531a-106">Etiqueta</span><span class="sxs-lookup"><span data-stu-id="f531a-106">Label</span></span> | <span data-ttu-id="f531a-107">Value</span><span class="sxs-lookup"><span data-stu-id="f531a-107">Value</span></span> |
|-------------------|-----------------------------|
| <span data-ttu-id="f531a-108">GUID del conjunto de propiedades</span><span class="sxs-lookup"><span data-stu-id="f531a-108">Property Set GUID</span></span> | <span data-ttu-id="f531a-109">DVDKaraoke de AM \_ KSPROPSETID \_</span><span class="sxs-lookup"><span data-stu-id="f531a-109">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="f531a-110">Id. de propiedad</span><span class="sxs-lookup"><span data-stu-id="f531a-110">Property ID</span></span>                      | <span data-ttu-id="f531a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f531a-111">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f531a-112">HABILITACIÓN \_ \_ DE DVDKARAOKE DE LA PROPIEDAD \_ AM</span><span class="sxs-lookup"><span data-stu-id="f531a-112">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="f531a-113">Valor booleano.</span><span class="sxs-lookup"><span data-stu-id="f531a-113">BOOLEAN value.</span></span> <span data-ttu-id="f531a-114">El navegador de DVD envía al descodificador una PROPIEDAD DE AM DVDKARAOKE ENABLE con un valor de TRUE para habilitar la remezclación de alias o \_ \_ FALSE para \_ deshabilitarla.  </span><span class="sxs-lookup"><span data-stu-id="f531a-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="f531a-115">DATOS \_ \_ DVDKARAOKE DE LA PROPIEDAD \_ AM</span><span class="sxs-lookup"><span data-stu-id="f531a-115">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="f531a-116">El navegador de DVD envía al descodificador una propiedad DVDKARAOKE DATA de AM PROPERTY con un puntero a una estructura \_ \_ \_ [**\_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) de AM para cambiar la configuración de la mezcla inferior; es decir, para activar o desactivar determinados canales y dirigirlos al canal de salida derecho o izquierdo.</span><span class="sxs-lookup"><span data-stu-id="f531a-116">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="f531a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f531a-117">Requirements</span></span>



| <span data-ttu-id="f531a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f531a-118">Requirement</span></span> | <span data-ttu-id="f531a-119">Value</span><span class="sxs-lookup"><span data-stu-id="f531a-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f531a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f531a-120">Header</span></span><br/> | <dl> <span data-ttu-id="f531a-121"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="f531a-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f531a-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f531a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f531a-123">Conjuntos de propiedades</span><span class="sxs-lookup"><span data-stu-id="f531a-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




