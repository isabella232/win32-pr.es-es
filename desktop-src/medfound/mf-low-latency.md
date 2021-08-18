---
description: Habilita el procesamiento de baja latencia en la Microsoft Media Foundation ejecución.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: MF_LOW_LATENCY atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51421b68e23ab3f29c15b0b360a7d189befb45cd9046176e6dcb99f1b0748f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956455"
---
# <a name="mf_low_latency-attribute"></a>Atributo \_ MF LOW \_ LATENCY

Habilita el procesamiento de baja latencia en la Microsoft Media Foundation ejecución.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

La latencia baja se define como el menor retraso posible desde el momento en que se generan (o reciben) los datos multimedia hasta el momento en que se representan. La baja latencia es deseable para escenarios de comunicación en tiempo real. En otros escenarios, como la reproducción local o la transcodificación, normalmente no debe habilitar el modo de baja latencia, ya que puede afectar a la calidad.

> [!Note]  
> El valor GUID de este atributo es idéntico a la propiedad [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) definida para la [**interfaz ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)

 

Establezca este atributo en los componentes de canalización de la siguiente manera:

-   Origen multimedia: use el [**método IMFMediaSourceEx::GetSourceAttributes.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes)
-   Media Foundation transformación (MFT): use el [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) En el caso de los codificadores, el codificador puede admitir una latencia baja a través de la [**interfaz ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   Receptor de medios: consulte el receptor de medios para la [**interfazATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Normalmente, las aplicaciones no establecen este atributo directamente en los componentes de canalización, sino que establecen el atributo en uno de los objetos siguientes:

-   [Sesión multimedia:](media-session.md)use el *parámetro pConfiguation* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) o bien establezca el atributo en la topología.
-   [Lector de origen:](source-reader.md)establezca el atributo con las propiedades de configuración al crear el Lector de origen. Para obtener más información, vea [Atributos del lector de origen.](source-reader-attributes.md)
-   [Escritor de](sink-writer.md)receptores: establezca el atributo con las propiedades de configuración al crear el escritor de receptores. Para obtener más información, vea [Sink Writer Attributes](sink-writer-attributes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de escritor de receptores](sink-writer-attributes.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 
