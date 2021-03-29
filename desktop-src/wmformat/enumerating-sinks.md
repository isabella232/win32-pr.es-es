---
title: Enumerar receptores
description: Enumerar receptores
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- Advanced Systems Format (ASF), enumeración de receptores
- ASF (formato de sistemas avanzados), enumeración de receptores
- Advanced Systems Format (ASF), receptores
- ASF (formato de sistemas avanzados), receptores
- receptores, enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "103789171"
---
# <a name="enumerating-sinks"></a><span data-ttu-id="a91e7-108">Enumerar receptores</span><span class="sxs-lookup"><span data-stu-id="a91e7-108">Enumerating Sinks</span></span>

<span data-ttu-id="a91e7-109">El escritor puede tener muchos receptores asociados.</span><span class="sxs-lookup"><span data-stu-id="a91e7-109">The writer can have many sinks associated with it.</span></span> <span data-ttu-id="a91e7-110">Puede enumerar los receptores que se han agregado al escritor mediante [**IWMWriterAdvanced:: GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) y [**IWMWriterAdvanced:: GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span><span class="sxs-lookup"><span data-stu-id="a91e7-110">You can enumerate the sinks that have been added to the writer by using [**IWMWriterAdvanced::GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) and [**IWMWriterAdvanced::GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span></span>

<span data-ttu-id="a91e7-111">El código de ejemplo de la [sección obtención de mensajes de error de un receptor](getting-error-messages-from-a-sink.md) muestra la enumeración de receptores.</span><span class="sxs-lookup"><span data-stu-id="a91e7-111">The example code in the [Getting Error Messages from a Sink](getting-error-messages-from-a-sink.md) demonstrates sink enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="a91e7-112">Al enumerar los receptores, el receptor de archivos predeterminado creado en respuesta a una llamada a [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) se enumerará junto con cualquier otro receptor que haya agregado.</span><span class="sxs-lookup"><span data-stu-id="a91e7-112">When enumerating sinks, the default file sink created in response to a call to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) will be enumerated along with any other sinks you have added.</span></span> <span data-ttu-id="a91e7-113">Si solo usa el receptor de archivos predeterminado, puede acceder a él mediante una llamada a **GetSink** para el índice de receptor 0.</span><span class="sxs-lookup"><span data-stu-id="a91e7-113">If you are using only the default file sink, you can access it by calling **GetSink** for sink index 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a91e7-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a91e7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a91e7-115">**Interfaz IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="a91e7-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="a91e7-116">**Trabajar con receptores de escritor**</span><span class="sxs-lookup"><span data-stu-id="a91e7-116">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




