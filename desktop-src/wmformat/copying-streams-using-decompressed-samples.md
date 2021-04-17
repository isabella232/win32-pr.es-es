---
title: Copiar secuencias mediante ejemplos descomprimidos
description: Copiar secuencias mediante ejemplos descomprimidos
ms.assetid: 03ad8415-1dff-4362-94b4-7ec69c3e7888
keywords:
- SDK de Windows Media Format, copiar flujos
- Advanced Systems Format (ASF), copiar flujos
- ASF (formato de sistemas avanzados), copiar flujos
- flujos, copiar mediante datos descomprimidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c5c0f98b02090d98814983ad518ee3cd7e5d8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704773"
---
# <a name="copying-streams-using-decompressed-samples"></a><span data-ttu-id="ed569-107">Copiar secuencias mediante ejemplos descomprimidos</span><span class="sxs-lookup"><span data-stu-id="ed569-107">Copying Streams Using Decompressed Samples</span></span>

<span data-ttu-id="ed569-108">Se recomienda encarecidamente no copiar flujos de un archivo a otro mediante ejemplos descomprimidos.</span><span class="sxs-lookup"><span data-stu-id="ed569-108">It is strongly recommended that you not copy streams from one file to another using decompressed samples.</span></span> <span data-ttu-id="ed569-109">El proceso de descomprimir y volver a comprimir los ejemplos degradará la calidad de la salida.</span><span class="sxs-lookup"><span data-stu-id="ed569-109">The process of decompressing and recompressing samples will degrade the quality of the output.</span></span> <span data-ttu-id="ed569-110">Si necesita descomprimir los ejemplos y copiarlos después en otro flujo, puede encontrarse con cierta dificultad con secuencias codificadas de velocidad de bits variable (VBR) basadas en la calidad.</span><span class="sxs-lookup"><span data-stu-id="ed569-110">If you do need to decompress your samples and then copy them to another stream, you may encounter some difficulty with quality-based variable bit rate (VBR) encoded streams.</span></span>

<span data-ttu-id="ed569-111">Cuando el códec termina de comprimir una secuencia VBR basada en la calidad, registra la velocidad de bits y la ventana de búfer del contenido resultante.</span><span class="sxs-lookup"><span data-stu-id="ed569-111">When the codec finishes compressing a quality-based VBR stream, it records the bit rate and buffer window of the resulting content.</span></span> <span data-ttu-id="ed569-112">Cuando se lee un archivo que contiene una secuencia codificada con VBR basada en la calidad, el perfil obtenido del lector observará la velocidad de bits y la ventana del búfer, así como las ventanas velocidad de bits máxima y búfer máximo.</span><span class="sxs-lookup"><span data-stu-id="ed569-112">When you read a file containing a stream encoded with quality-based VBR, the profile obtained from the reader will note the bit rate and buffer window as well as the maximum bit rate and maximum buffer window.</span></span> <span data-ttu-id="ed569-113">Esta configuración en el perfil normalmente significa un flujo de velocidad de bits variable restringido de velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="ed569-113">This configuration in the profile normally signifies a bit-rate constrained variable bit rate stream.</span></span> <span data-ttu-id="ed569-114">Como resultado, cuando se establece el perfil en el escritor, se espera un paso de preprocesamiento para el flujo, ya que las secuencias VBR con restricción de velocidad de bits requieren codificación de dos pasos.</span><span class="sxs-lookup"><span data-stu-id="ed569-114">As a result, when you set the profile on the writer, it will expect a preprocessing pass for the stream, because bit-rate constrained VBR streams require two-pass encoding.</span></span> <span data-ttu-id="ed569-115">Debe tratar el flujo como si fuera una secuencia VBR restringida de velocidad de bits y ofrecer los ejemplos para el preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="ed569-115">You should treat the stream as if it were a bit-rate constrained VBR stream and deliver the samples for preprocessing.</span></span> <span data-ttu-id="ed569-116">Dado que está usando los valores devueltos después de codificar el contenido en un nivel de calidad determinado, esos valores representan el nivel de calidad deseado.</span><span class="sxs-lookup"><span data-stu-id="ed569-116">Because you are using the values returned after encoding the content at a particular quality level, those values represent the desired quality level.</span></span> <span data-ttu-id="ed569-117">Por supuesto, la calidad de la salida recodificada se degradará en cierto modo, como resultado de la recodificación.</span><span class="sxs-lookup"><span data-stu-id="ed569-117">Of course, the quality of the re-encoded output will be somewhat degraded anyway, as a result of the re-encoding.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed569-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed569-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed569-119">**Copiar datos de un archivo a otro**</span><span class="sxs-lookup"><span data-stu-id="ed569-119">**Copying Data from One File to Another**</span></span>](copying-data-from-one-file-to-another.md)
</dt> <dt>

[<span data-ttu-id="ed569-120">**Copiar secuencias sin descomprimir los datos**</span><span class="sxs-lookup"><span data-stu-id="ed569-120">**Copying Streams Without Decompressing the Data**</span></span>](copying-streams-without-decompressing-the-data.md)
</dt> </dl>

 

 




