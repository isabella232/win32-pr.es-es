---
description: Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696638"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a>\_ \_ Hora de inicio de la topología MF \_ \_ en el \_ \_ atributo switch de presentación

Especifica la hora de inicio de las presentaciones que se ponen en cola después de la primera presentación.

## <a name="data-type"></a>Tipo de datos

**INT64** almacenado como **UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

Cuando la aplicación pone en cola la primera presentación en la sesión multimedia, la aplicación especifica la hora de inicio en el parámetro *pvarStartPosition* del método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) . En el caso de las presentaciones posteriores, sin embargo, la hora de inicio la proporciona la hora de inicio \_ de la topología MF \_ \_ \_ en \_ \_ el atributo switch de la presentación en la topología. La hora de inicio se especifica en unidades de 100-nanosegundos, con respecto al principio de la presentación. Por ejemplo, si el valor es 50 millones, la reproducción empieza 5 segundos en la presentación. Si no se establece este atributo, la hora de inicio predeterminada es cero.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




