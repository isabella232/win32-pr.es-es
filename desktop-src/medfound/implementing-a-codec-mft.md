---
description: En este tema se proporcionan algunas directrices para implementar un descodificador o codificador como una transformación de Media Foundation (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implementar un MFT de códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279050"
---
# <a name="implementing-a-codec-mft"></a>Implementar un MFT de códec

En este tema se proporcionan algunas directrices para implementar un descodificador o codificador como una transformación de Media Foundation (MFT).

-   [Codificadores](#encoders)
    -   [Negociación del formato del codificador](#encoder-format-negotiation)
-   [Descodificadores](#decoders)
    -   [Descodificadores de solo transcodificación](#transcode-only-decoders)
    -   [Atributos de telecine](#telecine-attributes)
-   [Temas relacionados](#related-topics)

## <a name="encoders"></a>Codificadores

### <a name="encoder-format-negotiation"></a>Negociación del formato del codificador

El siguiente procedimiento se usa para inicializar un codificador:

1.  Consulte la MFT para la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .
2.  Llame a [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) para establecer las propiedades de codificación.
3.  Llame a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para establecer el formato de codificación.
4.  Llame a [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para obtener una lista de tipos de entrada compatibles. (Este paso se podría omitir).
5.  Llame a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para establecer el formato de entrada sin comprimir.

Después de establecer el tipo de salida en el paso 3, el método [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) debe devolver una lista de tipos de entrada que sean compatibles con el tipo de salida actual. En otras palabras, los tipos devueltos por **GetInputAvailableType** en este punto deben ser válidos para [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

En el caso de los descodificadores, se invierte el orden en el que se establecen los tipos: el tipo de entrada se establece primero, seguido del tipo de salida. Una vez establecido el tipo de entrada, el método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) debe devolver una lista de tipos que se pueden pasar al método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) .

Los codificadores y descodificadores deben admitir NV12 como un formato no comprimido común. Esto garantiza que los componentes de canalización pueden interoperar con conversiones mínimas de ColorSpace. Por supuesto, también se pueden admitir otros formatos.

## <a name="decoders"></a>Descodificadores

### <a name="transcode-only-decoders"></a>Descodificadores Transcode-Only

Algunos descodificadores están optimizados para la transcodificación (descodificación y recodificación de una secuencia) y no son adecuados para su uso durante la reproducción.

Si una MFT del descodificador está destinada únicamente a la transcodificación, establezca la marca de **\_ enumeración de MFT \_ \_ \_ solo Transcode** Flag al registrar la MFT. (Consulte [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)).

De forma predeterminada, la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) no devuelve los descodificadores de Transcode. Para enumerar los descodificadores de transcodificación, llame a **MFTEnumEx** y establezca la marca de **\_ enumeración de MFT \_ \_ \_ solo** en el parámetro *Flags* . Cuando se usa en la función **MFTEnumEx** , este marcador enumera los descodificadores de transcodificación y otros descodificadores.



| MFTRegister **\_ marca de enumeración de MFT \_ \_ \_ solo Transcode** | MFTEnumEx **\_ marca de enumeración de MFT \_ \_ \_ solo Transcode** | ¿Se ha enumerado MFT? |
|--------------------------------------------------|------------------------------------------------|--------------------|
| 1                                                | 1                                              | Sí                |
| 1                                                | 0                                              | No                 |
| 0                                                | 1                                              | Sí                |
| 0                                                | 0                                              | Sí                |



 

### <a name="telecine-attributes"></a>Atributos de telecine

El origen multimedia podría adjuntar los siguientes atributos de telecine a los ejemplos de medios que ofrece.



| Atributo                                                                                   | Descripción                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md) | Equivalente a la marca "repetir primer campo" (RFF). |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) | Inversa del marcador "primer campo primero" (TFF).       |



 

Estas marcas proporcionan una sugerencia al representador de vídeo mejorado (EVR) cuando realiza el desentrelazado. Un descodificador debe propagar estas marcas de nivel inferior copiándolas a los ejemplos de salida, de modo que lleguen a EVR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir una MFT personalizada](writing-a-custom-mft.md)
</dt> </dl>

 

 
