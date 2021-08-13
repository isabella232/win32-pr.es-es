---
description: Especifica una tarea del Servicio programador de clases multimedia (MMCSS) para una rama de topología.
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: MF_TOPONODE_WORKQUEUE_MMCSS_CLASS atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6630cf22d3afe270b2a032304fd9de3118e73e75e28da4116418894271237a71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739849"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a>Atributo \_ \_ \_ MMCSS CLASS MF TOPONODE WORKQUEUE \_

Especifica una tarea [del Servicio programador de](../procthread/multimedia-class-scheduler-service.md) clases multimedia (MMCSS) para una rama de topología.

## <a name="data-type"></a>Tipo de datos

Cadena de caracteres anchos

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de origen **(MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE**). Este atributo es opcional.

Este atributo requiere el atributo [MF \_ TOPONODE \_ WORKQUEUE \_ ID.](mf-toponode-workqueue-id-attribute.md) Si establece este atributo, establezca también el atributo **MF \_ TOPONODE \_ WORKQUEUE \_ ID** en el mismo nodo.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**ATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ ID**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[Colas de trabajo](work-queues.md)
</dt> </dl>

 

 
