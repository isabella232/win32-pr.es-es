---
description: Establecer un tipo de salida para un codificador WMA
ms.assetid: 0a1a22bb-460f-4ac2-be76-4249997441de
title: Establecer un tipo de salida para un codificador WMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c6b078dc2426b062a90f706c5d113960f54ce32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153668"
---
# <a name="setting-an-output-type-for-a-wma-encoder"></a><span data-ttu-id="90292-103">Establecer un tipo de salida para un codificador WMA</span><span class="sxs-lookup"><span data-stu-id="90292-103">Setting an Output Type for a WMA Encoder</span></span>

<span data-ttu-id="90292-104">Para crear un tipo de salida válido para un codificador Windows Media Audio (WMA), debe tener la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="90292-104">To create a valid output type for a Windows Media Audio (WMA) encoder, you must have the following information:</span></span>

-   <span data-ttu-id="90292-105">El subtipo de audio que repesents el formato WMA codificado.</span><span class="sxs-lookup"><span data-stu-id="90292-105">The audio subtype that repesents the encoded WMA format.</span></span> <span data-ttu-id="90292-106">Vea [GUID de subtipo de audio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="90292-106">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>
-   <span data-ttu-id="90292-107">Propiedades de configuración que se van a establecer en el codificador.</span><span class="sxs-lookup"><span data-stu-id="90292-107">The configuration properties to set on the encoder.</span></span>

    <span data-ttu-id="90292-108">Las propiedades de configuración se documentan en la documentación del códec de Windows Media Audio y vídeo y de las API de DSP.</span><span class="sxs-lookup"><span data-stu-id="90292-108">The configuration properties are documented in the Windows Media Audio and Video Codec and DSP APIs documentation.</span></span> <span data-ttu-id="90292-109">Para obtener más información, vea "propiedades de secuencia de audio" en [propiedades de codificación](configuring-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="90292-109">For more information, see "Audio Stream Properties" in [Encoding Properties](configuring-the-encoder.md).</span></span>

### <a name="windows-vista-or-later"></a><span data-ttu-id="90292-110">Windows Vista o posterior</span><span class="sxs-lookup"><span data-stu-id="90292-110">Windows Vista or Later</span></span>

<span data-ttu-id="90292-111">Para obtener un tipo de salida válido para el codificador, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="90292-111">To get a valid output type for the encoder, perform the following steps.</span></span>

1.  <span data-ttu-id="90292-112">Utilice la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) o [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) para crear una instancia del codificador.</span><span class="sxs-lookup"><span data-stu-id="90292-112">Use the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function to create an instance of the encoder.</span></span>
2.  <span data-ttu-id="90292-113">Consulte el codificador para la interfaz **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="90292-113">Query the encoder for the **IPropertyStore** interface.</span></span>
3.  <span data-ttu-id="90292-114">Use la interfaz **IPropertyStore** para configurar el codificador.</span><span class="sxs-lookup"><span data-stu-id="90292-114">Use the **IPropertyStore** interface to configure the encoder.</span></span>
4.  <span data-ttu-id="90292-115">Recupere los tipos de salida admitidos mediante una llamada a [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) en un bucle hasta que el codificador devuelva **MF \_ e \_ no haya \_ más \_ tipos** y elija el tipo de medio de destino.</span><span class="sxs-lookup"><span data-stu-id="90292-115">Retrieve the supported output types by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) in a loop until the encoder returns **MF\_E\_NO\_MORE\_TYPES** and you choose the target media type.</span></span> <span data-ttu-id="90292-116">I</span><span class="sxs-lookup"><span data-stu-id="90292-116">I</span></span>
5.  <span data-ttu-id="90292-117">Llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de medio de compresión en el codificador.</span><span class="sxs-lookup"><span data-stu-id="90292-117">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

### <a name="windows-7"></a><span data-ttu-id="90292-118">Windows 7</span><span class="sxs-lookup"><span data-stu-id="90292-118">Windows 7</span></span>

<span data-ttu-id="90292-119">Para obtener un tipo de salida válido para el codificador en Windows 7, Media Foundation proporciona la función [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="90292-119">To get a valid output type for the encoder in Windows 7, Media Foundation provides the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="90292-120">Una aplicación debe pasar el subtipo de audio que repesents los WMA codificados y las propiedades de codificación.</span><span class="sxs-lookup"><span data-stu-id="90292-120">An application must pass required the audio subtype that repesents the encoded WMA and the encoding properties.</span></span> <span data-ttu-id="90292-121">Las propiedades son necesarias porque el codificador cambia los tipos de salida admitidos en función del conjunto de modos.</span><span class="sxs-lookup"><span data-stu-id="90292-121">The properties are required because the encoder changes the supported output types depending upon the mode set.</span></span>

> [!Note]  
> <span data-ttu-id="90292-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)solo se admite para la [codificación de velocidad de bits constante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="90292-122">[**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes)is only supported for [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span>

 

<span data-ttu-id="90292-123">Si la llamada se realiza correctamente, la aplicación recibe una lista de punteros IUnknown de los tipos de medios de salida admitidos en un objeto [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) .</span><span class="sxs-lookup"><span data-stu-id="90292-123">If the call succeeds, the application receives a list of IUnknown pointers of the supported output media types in an [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) object.</span></span> <span data-ttu-id="90292-124">Para establecer el tipo de medio de salida, busque el que coincida con su tipo de destino y llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el tipo de medio de compresión en el codificador.</span><span class="sxs-lookup"><span data-stu-id="90292-124">To set the output media type, find the one that matches your target type and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the compression media type on the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90292-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90292-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90292-126">Crear instancias de una MFT del codificador</span><span class="sxs-lookup"><span data-stu-id="90292-126">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="90292-127">Codificadores de Windows Media</span><span class="sxs-lookup"><span data-stu-id="90292-127">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



