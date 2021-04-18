---
description: La codificación de dos pasos se puede usar para la velocidad de bits constante (CBR) y para la codificación de velocidad de bits variable (VBR) con algunos de los códecs de Windows Media.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Uso de la codificación de Two-Pass (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687304"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a><span data-ttu-id="a283a-103">Uso de la codificación de Two-Pass (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="a283a-103">Using Two-Pass Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="a283a-104">La codificación de dos pasos se puede usar para la velocidad de bits constante (CBR) y para la codificación de velocidad de bits variable (VBR) con algunos de los códecs de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a283a-104">Two-pass encoding can be used for constant bit rate (CBR) and for variable bit rate (VBR) encoding with some of the Windows Media codecs.</span></span> <span data-ttu-id="a283a-105">Puede encontrar el número máximo de pasos de codificación admitidos por un códec mediante la recuperación de la propiedad [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="a283a-105">You can find the maximum number of encoding passes supported by a codec by retrieving the [MFPKEY\_PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) property.</span></span> <span data-ttu-id="a283a-106">Ninguno de los códecs admite más de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="a283a-106">None of the codecs supports more than two passes.</span></span> <span data-ttu-id="a283a-107">Configure el DMO para que use dos pasos mediante el establecimiento de la propiedad [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md) en 2.</span><span class="sxs-lookup"><span data-stu-id="a283a-107">Configure the DMO to use two passes by setting the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2.</span></span>

<span data-ttu-id="a283a-108">Entregue los ejemplos al codificador DMO de uno en uno, como lo haría en un modo de un solo paso.</span><span class="sxs-lookup"><span data-stu-id="a283a-108">Deliver the samples to the encoder DMO one at a time, as you would in a one-pass mode.</span></span> <span data-ttu-id="a283a-109">Al procesar los ejemplos de entrada para el paso de preprocesamiento, las llamadas a [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) o [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) devolverán **S \_ false** para indicar que no se produce ninguna salida.</span><span class="sxs-lookup"><span data-stu-id="a283a-109">When you process the input samples for your preprocessing pass, the calls to [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) or [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will return **S\_FALSE**, to indicate that no output is produced.</span></span>

<span data-ttu-id="a283a-110">Al final del primer paso (después de procesar la última entrada por primera vez), debe establecer la propiedad [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) para notificar al códec que la siguiente entrada procesada es la primera entrada del segundo paso.</span><span class="sxs-lookup"><span data-stu-id="a283a-110">At the end of the first pass (after the last input is processed for the first time), you then must set the [MFPKEY\_ENDOFPASS](mfpkey-endofpassproperty.md) property to notify the codec that the next input processed is the first input of the second pass.</span></span> <span data-ttu-id="a283a-111">No se requiere ningún valor para esta propiedad, por lo que debe usar una estructura de **variante** vacía.</span><span class="sxs-lookup"><span data-stu-id="a283a-111">No value is required for this property, so you should use an empty **VARIANT** structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a283a-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a283a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a283a-113">Códecs de Windows Media</span><span class="sxs-lookup"><span data-stu-id="a283a-113">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 
