---
description: Indica si un origen multimedia admite el flujo de datos de hardware.
ms.assetid: 32FEBC99-0AE0-4FE9-90AB-5FB204BD4C83
title: MF_SOURCE_STREAM_SUPPORTS_HW_CONNECTION atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 751d672e664ab1849376d839285393075ddf6af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716670"
---
# <a name="mf_source_stream_supports_hw_connection-attribute"></a>El \_ flujo de origen MF \_ admite el atributo de \_ \_ conexión de HW \_

Indica si un origen multimedia admite el flujo de datos de hardware.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se usa cuando un origen de medios sirve como proxy para un dispositivo de hardware y puede transferir datos de nivel inferior a través de un bus de hardware, sin enviar datos a la CPU. Por ejemplo, una cámara web puede proporcionar vídeo codificado en H. 264 directamente a un descodificador de hardware integrado.

En este escenario, el origen y el descodificador todavía se representan en el Microsoft Media Foundation por un objeto de [origen de medios](media-sources.md) y una [transformación de Media Foundation](media-foundation-transforms.md) (MFT). Sin embargo, los datos no fluyen entre estos dos objetos en la capa de canalización, solo en el nivel de hardware, como se muestra en el diagrama siguiente.

![diagrama que muestra un origen de proxy de hardware.](images/proxy-mft3.png)

La conexión entre el origen del medio y el MFT se negocia como se indica a continuación.

1.  La canalización consulta el origen de los medios para la interfaz [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) . (Esta interfaz es opcional para admitir los orígenes multimedia).
2.  La canalización llama a [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obtener un puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
3.  Las consultas de canalización para el \_ flujo de origen MF \_ \_ admiten el atributo de \_ \_ conexión HW. Si el atributo está presente y es igual a **true**, el origen de medios admite conexiones de hardware.
4.  La canalización comprueba si la MFT es también un proxy de hardware, comprobando el atributo de [ \_ \_ \_ \_ atributo de dirección URL de hardware de enumeración MFT](mft-enum-hardware-url-attribute.md) en la MFT. Para obtener más información, consulte [hardware MFTs](hardware-mfts.md).
5.  La canalización establece el atributo de [ \_ \_ \_ atributo Stream conectado de MFT](mft-connected-stream-attribute.md) en MFT. El valor de este atributo es el puntero [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) obtenido del origen multimedia en el paso 2.
6.  La canalización establece el atributo [MFT \_ conectado \_ a \_ HW \_ Stream](mft-connected-to-hw-stream.md) en **true** tanto en el origen multimedia como en el MFT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs de hardware](hardware-mfts.md)
</dt> </dl>

 

 




