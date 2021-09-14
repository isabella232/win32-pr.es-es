---
description: Constantes IPropertyBag de códec y DSP.
ms.assetid: 078b0eea-16dd-4427-b984-9e52a43de559
title: Códec y constantes IPropertyBag de DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dcf85e22f55082bb9e2c49041490f4c7aceb2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361172"
---
# <a name="codec-and-dsp-ipropertybag-constants"></a>Códec y constantes IPropertyBag de DSP

Hay dos métodos para establecer propiedades en los objetos codec y DSP mediante programación, mediante la interfaz **IPropertyBag** o **la interfaz IPropertyStore.** Las propiedades más comunes están disponibles a través de ambas interfaces. El uso de **la interfaz IPropertyStore** es preferible a **IPropertyBag.**



| Constante de cadena IPropertyBag          | Clave de propiedad IPropertyStore                                                                         |
|---------------------------------------|-----------------------------------------------------------------------------------------------------|
| g \_ wszAvgFrameRate                    | [MFPKEY \_ ASFOVERHEADPERFRAME](mfpkey-asfoverheadperframeproperty.md)                               |
| g \_ wszWMACAvgBytesPerSecond           | [MFPKEY \_ WMAENC \_ AVGBYTESPERSEC](mfpkey-wmaenc-avgbytespersecproperty.md)                          |
| g \_ wszWMACDRCSetting                  | [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md)                                        |
| g \_ wszWMACHiResOutput                 | [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md)                                |
| g \_ wszWMACModeSpeechClassMode        | [MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) |
| g \_ wszWMACOriginalWaveFormat          | [MFPKEY \_ WMAENC \_ ORIGWAVEFORMAT](mfpkey-wmaenc-origwaveformatproperty.md)                          |
| g \_ wszWMACSpeakerConfig               | [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md)                                        |
| g \_ wszWMACVoiceBuffer                 | [MFPKEY \_ WMAVOICE \_ ENC \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md)                 |
| g \_ wszWMACVoiceBuffer                 | [MFPKEY \_ WMAVOICE \_ ENC \_ EDL](mfpkey-wmavoice-enc-edlproperty.md)                                   |
| g \_ wszWMADRCAverageReference          | [AVGREF DE MFPKEY \_ \_ WMADRC](mfpkey-wmadrc-avgrefproperty.md)                                          |
| g \_ wszWMADRCAverageTarget             | [MFPKEY \_ WMADRC \_ AVGTARGET](mfpkey-wmadrc-avgtargetproperty.md)                                    |
| g \_ wszWMADRCPeakReference             | [MFPKEY \_ WMADRC \_ PEAKREF](mfpkey-wmadrc-peakrefproperty.md)                                        |
| g \_ wszWMADRCPeakTarget                | [MFPKEY \_ WMADRC \_ PEAKTARGET](mfpkey-wmadrc-peaktargetproperty.md)                                  |
| g \_ wszWMCPAudioVBRQuality             | [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md)                                                 |
| g \_ wszWMCPAudioVBRSupported           | [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md)                                                 |
| g \_ wszWMCPMaxPasses                   | [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)                                   |
| g \_ wszWMVCAvgBitrate                  | [MFPKEY \_ ESTOG](mfpkey-ravgproperty.md)                                                             |
| g \_ wszWMVCBAvg                        | [MFPKEY \_ BAVG](mfpkey-bavgproperty.md)                                                             |
| g \_ wszWMVCBDeltaQP                    | [MFPKEY \_ BDELTAQP](mfpkey-bdeltaqpproperty.md)                                                     |
| g \_ wszWMVCBMax                        | [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md)                                                             |
| g \_ wszWMVCBufferFullnessInFirstByte   | [MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE](mfpkey-bufferfullnessinfirstbyteproperty.md)                   |
| g \_ wszWMVCCodedFrames                 | [MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md)                                               |
| g \_ wszWMVCComplexityEx                | [MFPKEY \_ COMPLEXITYEX](mfpkey-complexityexproperty.md)                                             |
| g \_ wszWMVCComplexityMode              | [COMPLEJIDAD DE \_ MFPKEY](mfpkey-complexityproperty.md)                                                 |
| g \_ wszWMVCCompressionOptimizationType | [MFPKEY \_ COMPRESSIONOPTIMIZATIONTYPE](mfpkey-compressionoptimizationtypeproperty.md)               |
| g \_ wszWMVCCrisp                       | [MFPKEY \_ CRISP](mfpkey-crispproperty.md)                                                           |
| g \_ wszWMVCDecoderComplexityProfile    | [MFPKEY \_ DECODERCOMPLEXITYPROFILE](mfpkey-decodercomplexityprofileproperty.md)                     |
| g \_ wszWMVCDecoderComplexityRequested  | [DESCODIFICADOR DE \_ MFPKEYCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md)                 |
| g \_ wszWMVCDecoderDeinterlacing        | [DESINTERLAZADO DEL \_ \_ DESCODIFICADOR MFPKEY](mfpkey-decoder-deinterlacingproperty.md)                          |
| g \_ wszWMVCDenoiseOption               | [MFPKEY \_ DENOISEOPTION](mfpkey-denoiseoptionproperty.md)                                           |
| g \_ wszWMVCEndOfPass                   | [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md)                                                   |
| g \_ wszWMVCForceFrameHeight            | [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md)                                     |
| g \_ wszWMVCForceFrameWidth             | [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md)                                       |
| g \_ wszWMVCForceMedianSetting          | [MFPKEY \_ FORCEMEDIANSETTING](mfpkey-forcemediansettingproperty.md)                                 |
| g \_ wszWMVCFOURCC                      | [MFPKEY \_ FOURCC](mfpkey-fourccproperty.md)                                                         |
| g \_ wszWMVCInterlacedCodingEnabled     | [MFPKEY \_ INTERLACEDCODINGENABLED](mfpkey-interlacedcodingenabledproperty.md)                       |
| g \_ wszWMVCLookAhead                   | [MFPKEY \_ LOOKAHEAD](mfpkey-lookaheadproperty.md)                                                   |
| g \_ wszWMVCLoopFilter                  | [MFPKEY \_ LOOPFILTER](mfpkey-loopfilterproperty.md)                                                 |
| g \_ wszWMVCMacroblockModeCostMethod    | [MACROBLOCKMODECOSTMETHOD DE MFPKEY \_](mfpkey-macroblockmodecostmethodproperty.md)                     |
| g \_ wszWMVCMaxBitrate                  | [MFPKEY \_ RMAX](mfpkey-rmaxproperty.md)                                                             |
| g \_ wszWMVCMotionMatchMethod           | [MFPKEY \_ MOTIONMATCHMETHOD](mfpkey-motionmatchmethodproperty.md)                                   |
| g \_ wszWMVCMotionSearchLevel           | [MFPKEY \_ MOTIONSEARCHLEVEL](mfpkey-motionsearchlevelproperty.md)                                   |
| g \_ wszWMVCMotionSearchRange           | [MFPKEY \_ MOTIONSEARCHRANGE](mfpkey-motionsearchrangeproperty.md)                                   |
| g \_ wszWMVCNoiseEdgeRemoval            | [MFPKEY \_ NOISEEDGEREMOVAL](mfpkey-noiseedgeremovalproperty.md)                                     |
| g \_ wszWMVCNumThreads                  | [MFPKEY \_ NUMTHREADS](mfpkey-numthreadsproperty.md)                                                 |
| g \_ wszWMVCPassesRecommended           | [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)                                   |
| g \_ wszWMVCPassesUsed                  | [MFPKEY \_ PASSESUSED](mfpkey-passesusedproperty.md)                                                 |
| g \_ wszWMVCPerceptualOptLevel          | [MFPKEY \_ PERCEPTUALOPTLEVEL](mfpkey-perceptualoptlevelproperty.md)                                 |
| g \_ wszWMVCProduceDummyFrames          | [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md)                                 |
| g \_ wszWMVCRangeRedux                  | [MFPKEY \_ RANGEREDUX](mfpkey-rangereduxproperty.md)                                                 |
| g \_ wszWMVCTotalFrames                 | [TOTALFRAMES de MFPKEY \_](mfpkey-totalframesproperty.md)                                               |
| g \_ wszWMVCVBREnabled                  | [MFPKEY \_ VBRENABLED](mfpkey-vbrenabledproperty.md)                                                 |
| g \_ wszWMVCVBRQuality                  | [MFPKEY \_ VBRQUALITY](mfpkey-vbrqualityproperty.md)                                                 |
| g \_ wszWMVCVideoScaling                | [VÍDEOS DE \_ MFPKEYCALING](mfpkey-videoscalingproperty.md)                                             |
| g \_ wszWMVCVType                       | [MFPKEY \_ VTYPE](mfpkey-vtypeproperty.md)                                                           |
| g \_ wszWMVCZeroByteFrames              | [MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md)                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Códecs de Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



