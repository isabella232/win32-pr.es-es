---
title: AverageLevel
description: El atributo AverageLevel contiene un valor de amplitud de 16 bits que designa el nivel de volumen medio del contenido de audio.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- AverageLevel formato de Windows Media
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076723"
---
# <a name="averagelevel"></a><span data-ttu-id="4d4d7-104">AverageLevel</span><span class="sxs-lookup"><span data-stu-id="4d4d7-104">AverageLevel</span></span>

<span data-ttu-id="4d4d7-105">El atributo **AverageLevel** contiene un valor de amplitud de 16 bits que designa el nivel de volumen medio del contenido de audio.</span><span class="sxs-lookup"><span data-stu-id="4d4d7-105">The **AverageLevel** attribute contains a 16-bit amplitude value designating the average volume level of audio content.</span></span> <span data-ttu-id="4d4d7-106">Con [**PeakValue**](peakvalue.md), este atributo se usa para la normalización.</span><span class="sxs-lookup"><span data-stu-id="4d4d7-106">With [**PeakValue**](peakvalue.md), this attribute is used for normalization.</span></span> <span data-ttu-id="4d4d7-107">La normalización es el proceso por el que se ajusta el nivel de volumen de reproducción de los archivos de audio para que las partes más fuertes de los archivos que se reproducen en el mismo nivel y el volumen medio para cada uno sea el mismo.</span><span class="sxs-lookup"><span data-stu-id="4d4d7-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same.</span></span>

## <a name="global-constant"></a><span data-ttu-id="4d4d7-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="4d4d7-108">Global Constant</span></span>

<span data-ttu-id="4d4d7-109">g \_ wszAverageLevel</span><span class="sxs-lookup"><span data-stu-id="4d4d7-109">g\_wszAverageLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="4d4d7-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="4d4d7-110">Data Type</span></span>

<span data-ttu-id="4d4d7-111">**tipo de WMT \_ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="4d4d7-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="4d4d7-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4d4d7-112">Remarks</span></span>

<span data-ttu-id="4d4d7-113">Este atributo lo establece el objeto de escritor basándose en la información del códec.</span><span class="sxs-lookup"><span data-stu-id="4d4d7-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="4d4d7-114">Solo las secuencias comprimidas con uno de los códecs Windows Media Audio tienen un valor establecido automáticamente.</span><span class="sxs-lookup"><span data-stu-id="4d4d7-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="4d4d7-115">**AverageLevel** no es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4d4d7-115">**AverageLevel** is not read-only.</span></span> <span data-ttu-id="4d4d7-116">Sin embargo, si el archivo lo reproducirá el Media Player de Windows, no debe modificar este valor.</span><span class="sxs-lookup"><span data-stu-id="4d4d7-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="4d4d7-117">El Media Player de Windows lo usa para normalizar los niveles de los archivos de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="4d4d7-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="4d4d7-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d4d7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d4d7-119">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="4d4d7-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




