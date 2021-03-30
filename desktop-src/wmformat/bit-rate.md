---
title: Velocidad de bits
description: Velocidad de bits
ms.assetid: 7c35a07b-03d3-42d7-aefc-8e6a0033ac48
keywords:
- Windows Media Format SDK, velocidades de bits
- Advanced Systems Format (ASF), velocidades de bits
- ASF (formato de sistemas avanzados), velocidades de bits
- velocidades de bits, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d793be8fe04746a61eea48bcf066d95d641221a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779248"
---
# <a name="bit-rate"></a><span data-ttu-id="62d52-107">Velocidad de bits</span><span class="sxs-lookup"><span data-stu-id="62d52-107">Bit Rate</span></span>

<span data-ttu-id="62d52-108">La velocidad de bits hace referencia a la cantidad de datos por segundo que se entrega desde un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="62d52-108">Bit rate refers to the amount of data per second that is delivered from an ASF file.</span></span> <span data-ttu-id="62d52-109">Las medidas de velocidad de bits están en bits por segundo (BPS) o kilobits por segundo (kbps).</span><span class="sxs-lookup"><span data-stu-id="62d52-109">Bit rate measurements are in bits per second (bps) or kilobits per second (Kbps).</span></span> <span data-ttu-id="62d52-110">La velocidad de bits suele confundirse con el ancho de banda, que es una medida de la capacidad de transferencia de datos de una red.</span><span class="sxs-lookup"><span data-stu-id="62d52-110">Bit rate is often confused with bandwidth, which is a measurement of the data transfer capacity of a network.</span></span> <span data-ttu-id="62d52-111">El ancho de banda también se mide en bps y kbps.</span><span class="sxs-lookup"><span data-stu-id="62d52-111">Bandwidth is also measured in bps and Kbps.</span></span>

<span data-ttu-id="62d52-112">El SDK de Windows Media Format se puede usar para crear aplicaciones que entreguen contenido basado en Windows Media de streaming desde ubicaciones de Internet o intranet.</span><span class="sxs-lookup"><span data-stu-id="62d52-112">The Windows Media Format SDK can be used to create applications that deliver streaming Windows Media-based content from Internet or intranet locations.</span></span> <span data-ttu-id="62d52-113">Cuando se transmiten datos a través de una red o Internet, la velocidad de bits es de importancia vital para la experiencia del usuario final.</span><span class="sxs-lookup"><span data-stu-id="62d52-113">When you are streaming data across a network or the Internet, the bit rate is of vital importance to the end-user experience.</span></span> <span data-ttu-id="62d52-114">Si el ancho de banda disponible para la red es menor que la velocidad de bits del archivo ASF, la reproducción del archivo se interrumpirá de alguna manera.</span><span class="sxs-lookup"><span data-stu-id="62d52-114">If the bandwidth available to the network is less than the bit rate of the ASF file, the playback of the file will be interrupted in some way.</span></span> <span data-ttu-id="62d52-115">Normalmente, el ancho de banda insuficiente hará que se omitan los ejemplos o que se produzca una pausa en la reproducción mientras se almacenan en búfer más datos.</span><span class="sxs-lookup"><span data-stu-id="62d52-115">Usually, insufficient bandwidth will result in either samples being skipped, or a pause in playback while more data is buffered.</span></span>

<span data-ttu-id="62d52-116">A cada archivo ASF se le asigna un valor de velocidad de bits en el momento de la creación, en función del tipo y el número de secuencias que se incluyen en el perfil usado.</span><span class="sxs-lookup"><span data-stu-id="62d52-116">Every ASF file is assigned a bit rate value at the time of creation, based upon the type and number of streams that are included in the profile used.</span></span> <span data-ttu-id="62d52-117">Los flujos individuales tienen sus propias tasas de bits.</span><span class="sxs-lookup"><span data-stu-id="62d52-117">Individual streams have their own bit rates.</span></span> <span data-ttu-id="62d52-118">Las velocidades de bits pueden ser constantes (los datos originales se comprimen de manera que se mantenga un flujo constante de datos aproximadamente a la misma velocidad) o la variable (los datos originales se comprimen de manera que se mantenga la misma calidad en todo, incluso aunque esto pueda significar un flujo de datos desigual).</span><span class="sxs-lookup"><span data-stu-id="62d52-118">Bit rates can be constant (the original data is compressed in such a way as to maintain a constant flow of data at approximately the same rate) or variable (the original data is compressed in such a way as to maintain the same quality throughout, even though this may mean uneven data flow).</span></span> <span data-ttu-id="62d52-119">Se pueden aplicar distintos tipos de velocidad de bits a flujos diferentes dentro del mismo archivo.</span><span class="sxs-lookup"><span data-stu-id="62d52-119">Different bit rate types can be applied to different streams within the same file.</span></span>

<span data-ttu-id="62d52-120">Puede codificar el mismo contenido en varias secuencias diferentes, cada una con una velocidad de bits diferente.</span><span class="sxs-lookup"><span data-stu-id="62d52-120">You can encode the same content to several different streams, each with a different bit rate.</span></span> <span data-ttu-id="62d52-121">Después, puede configurar las secuencias para que sean mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="62d52-121">Then you can configure the streams so that they are mutually exclusive.</span></span> <span data-ttu-id="62d52-122">Esto le permite crear un único archivo que se puede transmitir a los usuarios con diferentes anchos de banda.</span><span class="sxs-lookup"><span data-stu-id="62d52-122">This enables you to create a single file that can be streamed to users with different bandwidths.</span></span> <span data-ttu-id="62d52-123">Esta característica se denomina velocidad de bits múltiple o MBR.</span><span class="sxs-lookup"><span data-stu-id="62d52-123">This feature is called multiple bit rate, or MBR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="62d52-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62d52-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62d52-125">**Conceptos**</span><span class="sxs-lookup"><span data-stu-id="62d52-125">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="62d52-126">**Codificación de velocidad de bits constante (CBR)**</span><span class="sxs-lookup"><span data-stu-id="62d52-126">**Constant Bit Rate (CBR) Encoding**</span></span>](constant-bit-rate--cbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="62d52-127">**Entradas, secuencias y salidas**</span><span class="sxs-lookup"><span data-stu-id="62d52-127">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="62d52-128">**Perfiles**</span><span class="sxs-lookup"><span data-stu-id="62d52-128">**Profiles**</span></span>](profiles.md)
</dt> <dt>

[<span data-ttu-id="62d52-129">**Codificación de velocidad de bits variable (VBR)**</span><span class="sxs-lookup"><span data-stu-id="62d52-129">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> </dl>

 

 




