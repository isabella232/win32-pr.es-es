---
description: Indica si un origen de medios admite el flujo de datos de hardware.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659672b11cbcaa51f543eec8239f56ba792584a4b1ac44af25ed76016cdeb2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955155"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a>MF \_ SOURCE STREAM ADMITE el atributo HW \_ \_ \_ \_ CONNECTION

Indica si un origen de medios admite el flujo de datos de hardware.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se usa cuando un origen multimedia envía un proxy a un dispositivo de hardware y es capaz de transferir datos de bajada a través de un bus de hardware, sin enviar datos a la CPU. Por ejemplo, una cámara web podría entregar vídeo codificado con H.264 directamente a un descodificador de hardware integrado.

En este escenario, el origen y el descodificador [](media-sources.md) se siguen representando en la Microsoft Media Foundation mediante un objeto de origen multimedia y una [transformación de](media-foundation-transforms.md) Media Foundation datos (MFT). Sin embargo, no hay ningún flujo de datos entre estos dos objetos en la capa de canalización, solo en la capa de hardware, como se muestra en el diagrama siguiente.

![diagrama que muestra un origen de proxy de hardware.](images/proxy-mft3.png)

La conexión entre el origen de medios y el MFT se negocia de la manera siguiente.

1.  La canalización consulta el origen de medios para la [**interfaz IMFMediaSourceEx.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) (Esta interfaz es opcional para que los orígenes multimedia admitan).
2.  La canalización llama [**a IMFMediaSourceEx::GetStreamAttributes para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) obtener un [**puntero DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
3.  Las consultas de canalización para el atributo MF \_ SOURCE \_ STREAM \_ \_ ADMITEN HW \_ CONNECTION. Si el atributo está presente y es igual a **TRUE,** el origen multimedia admite conexiones de hardware.
4.  La canalización comprueba si el MFT también es un proxy de hardware; para ello, comprueba el atributo Atributo de dirección URL de HARDWARE de [MFT \_ ENUM \_ \_ \_ ](mft-enum-hardware-url-attribute.md) en el MFT. Para obtener más información, vea [Hardware MFT](hardware-mfts.md).
5.  La canalización establece el [atributo \_ MFT CONNECTED \_ STREAM \_ ATTRIBUTE](mft-connected-stream-attribute.md) en MFT. El valor de este atributo es el puntero [**DEATTRIBUTEAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) obtenido del origen multimedia en el paso 2.
6.  La canalización establece el [atributo MFT \_ CONNECTED TO \_ HW \_ \_ STREAM](mft-connected-to-hw-stream.md) en **TRUE** tanto en el origen multimedia como en el MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Hardware MFTs](hardware-mfts.md)
</dt> </dl>

 

 




