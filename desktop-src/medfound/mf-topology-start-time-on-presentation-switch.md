---
description: Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363914"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a>HORA DE INICIO DE LA TOPOLOGÍA DE MF \_ EN EL atributo PRESENTATION \_ \_ \_ \_ \_ SWITCH

Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.

## <a name="data-type"></a>Tipo de datos

**INT64 almacenado** como **UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

Cuando la aplicación pone en cola la primera presentación en la sesión multimedia, la aplicación especifica la hora de inicio en el *parámetro pvarStartPosition* del [**método IMFMediaSession::Start.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) Sin embargo, para las presentaciones posteriores, la hora de inicio la da el atributo MF \_ TOPOLOGY \_ START TIME ON PRESENTATION SWITCH en la \_ \_ \_ \_ topología. La hora de inicio se especifica en unidades de 100 nanosegundos, con respecto al principio de la presentación. Por ejemplo, si el valor es 50000000, la reproducción comienza en 5 segundos en la presentación. Si no se establece este atributo, la hora de inicio predeterminada es cero.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




