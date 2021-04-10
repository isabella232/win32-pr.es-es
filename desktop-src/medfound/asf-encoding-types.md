---
description: Tipos de codificación ASF
ms.assetid: ffa99c6b-3b62-4068-96d5-ad57c340d088
title: Tipos de codificación ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6187f4bbf49eafaf50a46a8af92b71b4e72885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153691"
---
# <a name="asf-encoding-types"></a><span data-ttu-id="652af-103">Tipos de codificación ASF</span><span class="sxs-lookup"><span data-stu-id="652af-103">ASF Encoding Types</span></span>

<span data-ttu-id="652af-104">Los métodos de codificación se centran en el búfer usado por el codificador para administrar los datos de entrada sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="652af-104">The encoding methods all focus on the buffer used by the encoder to manage uncompressed input data.</span></span> <span data-ttu-id="652af-105">Este búfer se define por la velocidad de bits de la secuencia, en bits por segundo, y la ventana de búfer, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="652af-105">This buffer is defined by the bit rate of the stream, in bits per second, and the buffer window, in milliseconds.</span></span> <span data-ttu-id="652af-106">Al codificar en archivos ASF, los codificadores multimedia de Windows respetan las restricciones del búfer.</span><span class="sxs-lookup"><span data-stu-id="652af-106">When encoding to ASF files, the Windows Media encoders abide by the constraints of the buffer.</span></span> <span data-ttu-id="652af-107">Para obtener más información acerca de la ventana de búfer, vea [el modelo de búfer de depósitos con fugas](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="652af-107">For more information about the buffer window, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span> <span data-ttu-id="652af-108">Saber cómo y Cuándo usar cada método puede ayudarle a crear contenido comprimido de alta calidad.</span><span class="sxs-lookup"><span data-stu-id="652af-108">Knowing how and when to use each method can help you create high-quality compressed content.</span></span> <span data-ttu-id="652af-109">La tabla siguiente contiene vínculos a temas sobre cada uno de los métodos de codificación disponibles que una aplicación puede usar para codificar datos multimedia en ASF.</span><span class="sxs-lookup"><span data-stu-id="652af-109">The following table contains links to topics about each of the available encoding methods that an application can use to encode media data to ASF.</span></span>



| <span data-ttu-id="652af-110">Método de codificación</span><span class="sxs-lookup"><span data-stu-id="652af-110">Encoding method</span></span>                                                                                      | <span data-ttu-id="652af-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="652af-111">Description</span></span>                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="652af-112">Codificación de velocidad de bits constante</span><span class="sxs-lookup"><span data-stu-id="652af-112">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                         | <span data-ttu-id="652af-113">El codificador comprime los datos a una velocidad de bits especificada.</span><span class="sxs-lookup"><span data-stu-id="652af-113">The encoder compresses data to a specified bit rate.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="652af-114">Codificación de velocidad de bits variable basada en la calidad</span><span class="sxs-lookup"><span data-stu-id="652af-114">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="652af-115">El codificador comprime los datos en un valor de calidad determinado para que la calidad de los medios codificados sea coherente a lo largo de su duración, independientemente de los requisitos de búfer del flujo resultante.</span><span class="sxs-lookup"><span data-stu-id="652af-115">The encoder compresses data to a particular quality value so that the quality of the encoded media is consistent throughout its duration, regardless of the buffer requirements of the resulting stream.</span></span> |
| [<span data-ttu-id="652af-116">Codificación de velocidad de bits variable sin restricciones</span><span class="sxs-lookup"><span data-stu-id="652af-116">Unconstrained Variable Bit Rate Encoding</span></span>](unconstrained-variable-bit-rate--vbr--encoding.md)       | <span data-ttu-id="652af-117">El codificador comprime los datos con la máxima calidad posible manteniendo una velocidad de bits especificada.</span><span class="sxs-lookup"><span data-stu-id="652af-117">The encoder compresses data to the highest possible quality while maintaining a specified bit rate.</span></span> <span data-ttu-id="652af-118">Este modo también se denomina codificación de velocidad de bits variable (VBR) de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="652af-118">This mode is also called 2-pass variable bit rate (VBR) encoding.</span></span>                                    |
| [<span data-ttu-id="652af-119">Codificación de velocidad de bits variable máxima limitada</span><span class="sxs-lookup"><span data-stu-id="652af-119">Peak-Constrained Variable Bit Rate Encoding</span></span>](peak-constrained-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="652af-120">El codificador comprime los datos a una velocidad de bits especificada y mantiene los valores de búfer en la ventana de búfer máxima especificada y la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="652af-120">The encoder compresses data to a specified bit rate while keeping the buffer values under the specified maximum buffer window and bit rate.</span></span> <span data-ttu-id="652af-121">Este modo también se denomina VBR máxima de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="652af-121">This mode is also called 2-pass peak VBR.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="652af-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="652af-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="652af-123">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="652af-123">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="652af-124">Codificadores de Windows Media</span><span class="sxs-lookup"><span data-stu-id="652af-124">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



