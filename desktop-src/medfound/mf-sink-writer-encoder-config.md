---
description: Contiene un puntero a un almacén de propiedades con propiedades de codificación.
ms.assetid: 28AC864C-C63C-4BD4-9770-B7B48A2815C6
title: MF_SINK_WRITER_ENCODER_CONFIG atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1703eaa93254c5703f544641edd0063e2190a342
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814891"
---
# <a name="mf_sink_writer_encoder_config-attribute"></a>\_Atributo de \_ \_ configuración del codificador del escritor de receptor MF \_

Contiene un puntero a un almacén de propiedades con propiedades de codificación.

## <a name="data-type"></a>Tipo de datos

**IUnknown \** _

## <a name="remarks"></a>Observaciones

El valor de este atributo es [_ *IPropertyStore* *](/windows/win32/api/propsys/nn-propsys-ipropertystore) .

Este atributo permite que una aplicación establezca las propiedades de codificación al utilizar el [escritor del receptor](sink-writer.md). Para establecer este atributo, realice los pasos siguientes:

1.  Llame a [**PSCreateMemoryPropertyStore**](/windows/win32/api/propsys/nf-propsys-pscreatememorypropertystore) para crear un nuevo almacén de propiedades.
2.  Establezca las propiedades del codificador en el almacén de propiedades. Las propiedades disponibles dependen del codificador. Para obtener más información, consulte [objetos codec](codecobjects.md).
3.  Llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos.
4.  Llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown) para establecer el puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) en el almacén de atributos.
5.  Cree una nueva instancia del escritor del receptor. Pase el puntero [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) a la función de creación. Para obtener más información, vea [atributos del escritor de receptor](sink-writer-attributes.md).

El escritor del receptor establece las propiedades en el codificador antes de establecer los tipos de medios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                              |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Atributos del escritor de receptor](sink-writer-attributes.md)
</dt> </dl>

 

 
