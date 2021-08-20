---
description: En este tema se proporcionan algunas directrices para implementar un descodificador o codificador como un Media Foundation transform (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implementación de un MFT de códec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca6d0ce72ea65f400cb0c3c9249250f95c3c746e6f25c982a0a721bb87f12c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878322"
---
# <a name="implementing-a-codec-mft"></a>Implementación de un MFT de códec

En este tema se proporcionan algunas directrices para implementar un descodificador o codificador como un Media Foundation transform (MFT).

-   [Codificadores](#encoders)
    -   [Negociación del formato del codificador](#encoder-format-negotiation)
-   [Decodificadores](#decoders)
    -   [Descodificadores de solo transcodificación](#transcode-only-decoders)
    -   [Atributos de Televisa](#telecine-attributes)
-   [Temas relacionados](#related-topics)

## <a name="encoders"></a>Codificadores

### <a name="encoder-format-negotiation"></a>Negociación del formato del codificador

El procedimiento siguiente se usa para inicializar un codificador:

1.  Consulte MFT para la [**interfaz ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)
2.  Llame [**a ICodecAPI::SetValue para**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) establecer las propiedades de codificación.
3.  Llame [**a IMFTransform::SetOutputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) establecer el formato de codificación.
4.  Llame [**a IMFTransform::GetInputAvailableType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) obtener una lista de tipos de entrada compatibles. (Este paso puede omitirse).
5.  Llame [**a IMFTransform::SetInputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) establecer el formato de entrada sin comprimir.

Después de establecer el tipo de salida en el paso 3, el método [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) debe devolver una lista de tipos de entrada que sean compatibles con el tipo de salida actual. En otras palabras, los tipos devueltos por **GetInputAvailableType** en este momento deben ser válidos [**para SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

En el caso de los descodificadores, se invierte el orden en el que se establecen los tipos: el tipo de entrada se establece primero, seguido del tipo de salida. Una vez establecido el tipo de entrada, el método [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) debe devolver una lista de tipos que se pueden pasar al método [**IMFTransform::SetOutputType.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)

Los codificadores y descodificadores deben admitir NV12 como un formato común sin comprimir. Esto garantiza que los componentes de canalización pueden interoperar con conversiones de espacio de colores mínimas. Por supuesto, también se pueden admiten otros formatos.

## <a name="decoders"></a>Decodificadores

### <a name="transcode-only-decoders"></a>Transcode-Only descodificadores

Algunos descodificadores están optimizados para la transcodificación (descodificación y posterior codificación de una secuencia) y no son adecuados para su uso durante la reproducción.

Si un descodificador MFT solo está pensado para la transcodificación, establezca la marca **MFT \_ ENUM \_ FLAG \_ TRANSCODE \_ ONLY** al registrar el MFT. (Vea [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)).

De forma predeterminada, la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) no devuelve descodificadores de transcodificación. Para enumerar descodificadores de transcodificación, llame a **MFTEnumEx** y establezca la marca **MFT \_ ENUM \_ FLAG \_ TRANSCODE \_ ONLY** en *el parámetro Flags.* Cuando se usa en **la función MFTEnumEx,** esta marca enumera los descodificadores transcodificadores y otros descodificadores.



| MFTRegister **MFT \_ ENUM \_ FLAG \_ TRANSCODE \_ ONLY** | MFTEnumEx **MFT \_ ENUM \_ FLAG \_ TRANSCODE \_ ONLY** | ¿Se enumera MFT? |
|--------------------------------------------------|------------------------------------------------|--------------------|
| 1                                                | 1                                              | Sí                |
| 1                                                | 0                                              | No                 |
| 0                                                | 1                                              | Sí                |
| 0                                                | 0                                              | Sí                |



 

### <a name="telecine-attributes"></a>Atributos de Televisa

El origen de medios podría adjuntar los siguientes atributos de televisa a los ejemplos multimedia que entrega.



| Atributo                                                                                   | Descripción                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md) | Equivalente a la marca "repeat first field" (RFF). |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) | Inversa a la marca "top field first" (TFF).       |



 

Estas marcas proporcionan una sugerencia al representador de vídeo mejorado (EVR) cuando realiza el desinterlazado. Un descodificador debe propagar estas marcas de bajada al copiarlas en los ejemplos de salida para que lleguen al EVR.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritura de un MFT personalizado](writing-a-custom-mft.md)
</dt> </dl>

 

 
