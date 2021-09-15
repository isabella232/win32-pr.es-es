---
description: Habilita el procesamiento de baja latencia en la canalización Microsoft Media Foundation datos.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: MF_LOW_LATENCY atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360461"
---
# <a name="mf_low_latency-attribute"></a>Atributo \_ MF LOW \_ LATENCY

Habilita el procesamiento de baja latencia en la canalización Microsoft Media Foundation datos.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

La latencia baja se define como el menor retraso posible desde el momento en que se generan (o reciben) los datos multimedia hasta el momento en que se representan. La latencia baja es deseable para escenarios de comunicación en tiempo real. En otros escenarios, como la reproducción local o la transcodificación, normalmente no debe habilitar el modo de baja latencia, ya que puede afectar a la calidad.

> [!Note]  
> El valor GUID de este atributo es idéntico a la propiedad [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) definida para la [**interfaz ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)

 

Establezca este atributo en los componentes de canalización como se muestra a continuación:

-   Origen multimedia: use el [**método IMFMediaSourceEx::GetSourceAttributes.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes)
-   Media Foundation transformación (MFT): use el [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) En el caso de los codificadores, el codificador puede admitir una latencia baja a través de la [**interfaz ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   Receptor multimedia: consulte el receptor multimedia para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Normalmente, las aplicaciones no establecen este atributo directamente en los componentes de canalización, sino que establecen el atributo en uno de los objetos siguientes:

-   [Sesión multimedia:](media-session.md)use el *parámetro pConfiguation* de las funciones [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) o bien establezca el atributo en la topología.
-   [Lector de origen:](source-reader.md)establezca el atributo con las propiedades de configuración al crear el Lector de origen. Para obtener más información, vea [Atributos del lector de origen.](source-reader-attributes.md)
-   [Escritor de receptores:](sink-writer.md)establezca el atributo con las propiedades de configuración al crear el escritor de receptores. Para obtener más información, vea [Sink Writer Attributes](sink-writer-attributes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del escritor de receptores](sink-writer-attributes.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 
