---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de audio.
ms.assetid: 5d6c6a95-abb7-4191-a961-bcb30ca96bb6
title: Propiedades de audio (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Audio
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1bdab201fc987d5bc1aff3638fbb57358115fdce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699407"
---
# <a name="audio-properties"></a><span data-ttu-id="0689a-103">Propiedades de audio</span><span class="sxs-lookup"><span data-stu-id="0689a-103">Audio Properties</span></span>

<span data-ttu-id="0689a-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de audio.</span><span class="sxs-lookup"><span data-stu-id="0689a-104">Windows Portable Devices supports the following audio properties.</span></span>



| <span data-ttu-id="0689a-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0689a-105">Property</span></span>                         | <span data-ttu-id="0689a-106">VarType</span><span class="sxs-lookup"><span data-stu-id="0689a-106">VarType</span></span>     | <span data-ttu-id="0689a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0689a-107">Description</span></span>                                                                                                                                                                                                        |
|----------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0689a-108">**\_profundidad de \_ bits de audio de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0689a-108">**WPD\_AUDIO\_BIT\_DEPTH**</span></span>       | <span data-ttu-id="0689a-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="0689a-109">**VT\_UI4**</span></span> | <span data-ttu-id="0689a-110">La profundidad de bits del audio.</span><span class="sxs-lookup"><span data-stu-id="0689a-110">The bit-depth of the audio.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="0689a-111">**velocidad de bits de \_ audio WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0689a-111">**WPD\_AUDIO\_BITRATE**</span></span>          | <span data-ttu-id="0689a-112">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="0689a-112">**VT\_UI4**</span></span> | <span data-ttu-id="0689a-113">Velocidad de bits del audio, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="0689a-113">The bit rate of the audio, in bits per second.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="0689a-114">**\_alineación del \_ bloque de audio de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0689a-114">**WPD\_AUDIO\_BLOCK\_ALIGNMENT**</span></span> | <span data-ttu-id="0689a-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="0689a-115">**VT\_UI4**</span></span> | <span data-ttu-id="0689a-116">La alineación de bloque del archivo de audio, en bytes.</span><span class="sxs-lookup"><span data-stu-id="0689a-116">The block alignment of the audio file, in bytes.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="0689a-117">**recuento de canales de audio de WPD \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0689a-117">**WPD\_AUDIO\_CHANNEL\_COUNT**</span></span>   | <span data-ttu-id="0689a-118">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="0689a-118">**VT\_R4**</span></span>  | <span data-ttu-id="0689a-119">El número de canales de este archivo de audio, por ejemplo, 1, 2 o 5,1.</span><span class="sxs-lookup"><span data-stu-id="0689a-119">The number of channels in this audio file, for example, 1, 2, or 5.1.</span></span>                                                                                                                                              |
| <span data-ttu-id="0689a-120">**\_código de \_ formato de audio de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="0689a-120">**WPD\_AUDIO\_FORMAT\_CODE**</span></span>     | <span data-ttu-id="0689a-121">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="0689a-121">**VT\_UI4**</span></span> | <span data-ttu-id="0689a-122">Número de código del formato de onda registrado.</span><span class="sxs-lookup"><span data-stu-id="0689a-122">The registered WAVE format code number.</span></span> <span data-ttu-id="0689a-123">Para obtener una lista de formatos de onda registrados, consulte el artículo [registro de códigos FourCC y formatos de onda](https://msdn2.microsoft.com/library/ms867195.aspx) en el sitio web de MSDN.</span><span class="sxs-lookup"><span data-stu-id="0689a-123">For a listing of registered WAVE formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0689a-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0689a-124">Requirements</span></span>



| <span data-ttu-id="0689a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0689a-125">Requirement</span></span> | <span data-ttu-id="0689a-126">Value</span><span class="sxs-lookup"><span data-stu-id="0689a-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0689a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0689a-127">Header</span></span><br/> | <dl> <span data-ttu-id="0689a-128"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="0689a-128"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0689a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="0689a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0689a-130">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="0689a-130">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




