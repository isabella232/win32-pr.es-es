---
description: Indica si un receptor de medios admite el flujo de datos de hardware.
ms.assetid: 15838467-D253-4ECE-B9E7-AFD3A21B3AF2
title: MF_STREAM_SINK_SUPPORTS_HW_CONNECTION atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a9f663c492e5ae15590cc9240762e90298122790fa350fae51d09dd1199f6d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714385"
---
# <a name="mf_stream_sink_supports_hw_connection-attribute"></a>MF \_ STREAM SINK ADMITE el atributo HW \_ \_ \_ \_ CONNECTION

Indica si un receptor de medios admite el flujo de datos de hardware.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se usa cuando un receptor de medios hace proxy a un dispositivo de hardware y es capaz de recibir datos a través de un bus de hardware. Por ejemplo, un descodificador de audio de hardware podría enviar datos de audio directamente al hardware de representación de audio.

En este escenario, el descodificador y el receptor se siguen representando en la Microsoft Media Foundation mediante una [transformación de](media-foundation-transforms.md) Media Foundation (MFT) y un receptor multimedia. Sin embargo, no hay ningún flujo de datos entre estos dos objetos en la capa de canalización, solo en la capa de hardware, como se muestra en el diagrama siguiente.

![diagrama que muestra un origen de proxy de hardware.](images/proxy-mft4.png)

La conexión entre MFT y el receptor de medios se negocia como se muestra a continuación.

1.  La canalización comprueba si MFT es un proxy de hardware; para ello, comprueba el atributo [MFT \_ ENUM \_ HARDWARE URL \_ \_ Attribute](mft-enum-hardware-url-attribute.md) en MFT. Para obtener más información, vea [Hardware MFT](hardware-mfts.md).
2.  La canalización obtiene un puntero a la interfaz [**DESTREAMSTREAMSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) del receptor de flujo en el receptor multimedia.
3.  La canalización usa el puntero [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) para consultar el atributo MF \_ STREAM SINK SUPPORTS HW \_ \_ \_ \_ CONNECTION. Si este atributo está presente y es igual a **TRUE,** el origen de medios admite conexiones de hardware.
4.  La canalización establece el atributo [ \_ MFT CONNECTED \_ STREAM \_ ATTRIBUTE](mft-connected-stream-attribute.md) en el receptor de la secuencia. El valor de este atributo es el puntero [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) del MFT.
5.  La canalización establece el [atributo MFT \_ CONNECTED TO \_ HW \_ \_ STREAM](mft-connected-to-hw-stream.md) en **TRUE** tanto en el receptor de flujo como en el MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




