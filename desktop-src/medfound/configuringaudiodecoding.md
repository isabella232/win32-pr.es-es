---
description: Configuración de la descodificación de audio
ms.assetid: 362bd3bc-1474-4132-a8a8-e5dc0bba80e7
title: Configuración de la descodificación de audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da4d6a9d41b5c504ff60f25db20265072218caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808149"
---
# <a name="configuring-audio-decoding-microsoft-media-foundation"></a><span data-ttu-id="67333-103">Configuración de la descodificación de audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="67333-103">Configuring Audio Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="67333-104">Descodificar el contenido Windows Media Audio es mucho más fácil que codificarlo.</span><span class="sxs-lookup"><span data-stu-id="67333-104">Decoding Windows Media Audio content is much easier than encoding it.</span></span> <span data-ttu-id="67333-105">Después de crear un objeto de descodificador de audio, establezca el tipo de entrada mediante el método **IMediaObject:: SetInputType** o **IMFTransform:: SetInputType** .</span><span class="sxs-lookup"><span data-stu-id="67333-105">After creating an audio decoder object, set the input type by using the **IMediaObject::SetInputType** or **IMFTransform::SetInputType** method.</span></span> <span data-ttu-id="67333-106">El tipo de medio que se usa para la entrada del descodificador debe coincidir con el tipo de salida que se usó al codificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="67333-106">The media type that you use for the decoder input must match the output type that was used when the content was encoded.</span></span> <span data-ttu-id="67333-107">Esto incluye los datos de formato extendido anexados a la estructura **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="67333-107">This includes the extended format data appended to the **WAVEFORMATEX** structure.</span></span> <span data-ttu-id="67333-108">Debe asegurarse de que estos datos son correctos, porque el descodificador no puede procesar ejemplos sin él.</span><span class="sxs-lookup"><span data-stu-id="67333-108">You must ensure that this data is correct, because the decoder cannot process samples without it.</span></span>

<span data-ttu-id="67333-109">Después de establecer el tipo de entrada, puede configurar las características del descodificador que desee usar.</span><span class="sxs-lookup"><span data-stu-id="67333-109">After setting the input type, you can configure any decoder features you want to use.</span></span> <span data-ttu-id="67333-110">Las características del descodificador, como las que se usan para la codificación, se establecen mediante los métodos de **IPropertyBag** o **IPropertyStore**.</span><span class="sxs-lookup"><span data-stu-id="67333-110">Decoder features, like those used for encoding, are set using the methods of **IPropertyBag** or **IPropertyStore**.</span></span>

<span data-ttu-id="67333-111">Una vez que se establece el tipo de entrada y se configuran todas las características del descodificador, se pueden enumerar los tipos de salida admitidos por el descodificador realizando llamadas a **IMediaObject:: GetOutputType** o **IMFTransform:: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="67333-111">After the input type is set and all decoder features are configured, you can enumerate the output types supported by the decoder by making calls to **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67333-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="67333-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67333-113">Trabajar con audio</span><span class="sxs-lookup"><span data-stu-id="67333-113">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



