---
description: Habilita el procesamiento de baja latencia en la canalización de Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: MF_LOW_LATENCY atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815510"
---
# <a name="mf_low_latency-attribute"></a>\_Atributo de baja \_ latencia MF

Habilita el procesamiento de baja latencia en la canalización de Microsoft Media Foundation.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

La baja latencia se define como el menor retraso posible desde el momento en que se generan (o reciben) los datos multimedia cuando se representan. La latencia baja es conveniente para escenarios de comunicación en tiempo real. En otros escenarios, como la reproducción local o la transcodificación, normalmente no debe habilitar el modo de baja latencia, ya que puede afectar a la calidad.

> [!Note]  
> El valor GUID de este atributo es idéntico a la [propiedad \_ AVLowLatencyMode de CODECAPI](codecapi-avlowlatencymode.md) definida para la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .

 

Establezca este atributo en los componentes de canalización de la siguiente manera:

-   Origen de medios: Use el método [**IMFMediaSourceEx:: GetSourceAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .
-   Media Foundation Transform (MFT): Use el método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . En el caso de los codificadores, el codificador podría admitir latencia baja a través de la interfaz [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .
-   Receptor de medios: Consulte el receptor de medios para la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Normalmente, las aplicaciones no establecen este atributo directamente en los componentes de canalización, sino que establecen el atributo en uno de los siguientes objetos:

-   [Sesión de medios](media-session.md): Use el parámetro *pConfiguation* de la función [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) o [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) , o bien establezca el atributo en la topología.
-   [Lector de origen](source-reader.md): establezca el atributo con las propiedades de configuración al crear el lector de origen. Para obtener más información, vea [atributos del lector de código fuente](source-reader-attributes.md).
-   [Escritor de receptor](sink-writer.md): establezca el atributo con las propiedades de configuración al crear el escritor del receptor. Para obtener más información, vea [atributos del escritor de receptor](sink-writer-attributes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del escritor de receptor](sink-writer-attributes.md)
</dt> <dt>

[Atributos del lector de código fuente](source-reader-attributes.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 
