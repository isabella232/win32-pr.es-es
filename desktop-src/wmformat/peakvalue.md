---
title: PeakValue
description: El atributo PeakValue contiene un valor de amplitud de 16 bits que designa el nivel de volumen máximo del contenido de audio.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- PeakValue formato de Windows Media
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704845"
---
# <a name="peakvalue"></a><span data-ttu-id="8283b-104">PeakValue</span><span class="sxs-lookup"><span data-stu-id="8283b-104">PeakValue</span></span>

<span data-ttu-id="8283b-105">El atributo **PeakValue** contiene un valor de amplitud de 16 bits que designa el nivel de volumen máximo del contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="8283b-105">The **PeakValue** attribute contains contains a 16-bit amplitude value designating the peak volume level of audio content.</span></span> <span data-ttu-id="8283b-106">Con [**AverageLevel**](averagelevel.md), este atributo se usa para la normalización.</span><span class="sxs-lookup"><span data-stu-id="8283b-106">With [**AverageLevel**](averagelevel.md), this attribute is used for normalization.</span></span> <span data-ttu-id="8283b-107">La normalización es el proceso por el que se ajusta el nivel de volumen de reproducción de los archivos de audio para que las partes más fuertes de los archivos que se reproducen en el mismo nivel y el volumen medio para cada uno sea el mismo.</span><span class="sxs-lookup"><span data-stu-id="8283b-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same..</span></span>

## <a name="global-constant"></a><span data-ttu-id="8283b-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="8283b-108">Global Constant</span></span>

<span data-ttu-id="8283b-109">g \_ wszPeakValue</span><span class="sxs-lookup"><span data-stu-id="8283b-109">g\_wszPeakValue</span></span>

## <a name="data-type"></a><span data-ttu-id="8283b-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8283b-110">Data Type</span></span>

<span data-ttu-id="8283b-111">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8283b-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="8283b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8283b-112">Remarks</span></span>

<span data-ttu-id="8283b-113">Este atributo lo establece el objeto de escritor basándose en la información del códec.</span><span class="sxs-lookup"><span data-stu-id="8283b-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="8283b-114">Solo las secuencias comprimidas con uno de los códecs Windows Media Audio tienen un valor establecido automáticamente.</span><span class="sxs-lookup"><span data-stu-id="8283b-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="8283b-115">**PeakValue** no es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8283b-115">**PeakValue** is not read-only.</span></span> <span data-ttu-id="8283b-116">Sin embargo, si el archivo lo reproducirá el Media Player de Windows, no debe modificar este valor.</span><span class="sxs-lookup"><span data-stu-id="8283b-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="8283b-117">El Media Player de Windows lo usa para normalizar los niveles de los archivos de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="8283b-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="8283b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="8283b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8283b-119">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="8283b-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




