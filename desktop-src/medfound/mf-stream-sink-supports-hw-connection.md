---
description: Indica si un receptor de medios admite el flujo de datos de hardware.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: MF_STREAM_SINK_SUPPORTS_HW_CONNECTION atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95bfecba4cf53b6ef7c8863ec0456e310d8bcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497657"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>El \_ receptor de Stream MF \_ admite el atributo de \_ \_ conexión de HW \_

Indica si un receptor de medios admite el flujo de datos de hardware.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se usa cuando un receptor de medios envía un proxy a un dispositivo de hardware y puede recibir datos a través de un bus de hardware. Por ejemplo, un descodificador de audio de hardware podría enviar datos de audio directamente al hardware de representación de audio.

En este escenario, el descodificador y el receptor todavía se representan en el Microsoft Media Foundation mediante una [transformación de Media Foundation](media-foundation-transforms.md) (MFT) y un receptor de medios. Sin embargo, los datos no fluyen entre estos dos objetos en la capa de canalización, solo en el nivel de hardware, como se muestra en el diagrama siguiente.

![diagrama que muestra un origen de proxy de hardware.](images/proxy-mft4.png)

La conexión entre la MFT y el receptor multimedia se negocia como se indica a continuación.

1.  La canalización comprueba si MFT es un proxy de hardware, comprobando el atributo de [ \_ \_ \_ \_ atributo de dirección URL de hardware de enumeración MFT](mft-enum-hardware-url-attribute.md) en la MFT. Para obtener más información, consulte [hardware MFTs](hardware-mfts.md).
2.  La canalización obtiene un puntero a la interfaz [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del receptor de la secuencia en el receptor de medios.
3.  La canalización usa el puntero [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) para consultar el receptor de la \_ secuencia MF \_ \_ compatible con el atributo de conexión de \_ HW \_ . Si este atributo está presente y es igual a **true**, el origen de medios admite conexiones de hardware.
4.  La canalización establece el atributo de [ \_ \_ \_ atributo Stream conectado de MFT](mft-connected-stream-attribute.md) en el receptor de la secuencia. El valor de este atributo es el puntero [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) desde la MFT.
5.  La canalización establece el atributo [MFT \_ conectado \_ a \_ HW \_ Stream](mft-connected-to-hw-stream.md) en **true** en el receptor de la secuencia y en la MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




