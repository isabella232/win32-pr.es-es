---
description: Contiene un puntero a un almacén de propiedades con propiedades de codificación.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: MF_SINK_WRITER_ENCODER_CONFIG atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb68348987ac406643cbe709dc6052d1add3c04e63b4e1f38d7c681a95c3ae7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059089"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>Atributo MF \_ SINK \_ WRITER ENCODER \_ \_ CONFIG

Contiene un puntero a un almacén de propiedades con propiedades de codificación.

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Comentarios

El valor de este atributo es un [**puntero IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

Este atributo permite a una aplicación establecer propiedades de codificación cuando se usa [sink writer](sink-writer.md). Para establecer este atributo, realice los pasos siguientes:

1.  Llame [**a PSCreateMemoryPropertyStore para**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) crear un nuevo almacén de propiedades.
2.  Establezca las propiedades del codificador en el almacén de propiedades. Las propiedades disponibles dependen del codificador. Para obtener más información, vea [Objetos de códec](codecobjects.md).
3.  Llame [**a MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos.
4.  Llame [**aATTRIBUTEAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) para establecer el [**puntero IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) en el almacén de atributos.
5.  Cree una nueva instancia del escritor receptor. Pase el [**punteroATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) a la función de creación. Para obtener más información, vea [Sink Writer Attributes](sink-writer-attributes.md).

Sink Writer establece las propiedades en el codificador antes de establecer los tipos de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Atributos de escritor de receptores](sink-writer-attributes.md)
</dt> </dl>

 

 
