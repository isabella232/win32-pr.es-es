---
description: Especifica un identificador de tarea del Servicio programador de clases multimedia (MMCSS) para una rama de topología.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: MF_TOPONODE_WORKQUEUE_MMCSS_TASKID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579845"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>Atributo \_ TASKID DE MMCSS MF TOPONODE \_ \_ \_ WORKQUEUE

Especifica un identificador de tarea del Servicio programador de clases multimedia (MMCSS) para una rama de topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de origen **(MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE).** Este atributo es opcional.

Este atributo se omite a menos que también se establezcan los siguientes atributos:

-   [**ID. \_ DE \_ WORKQUEUE DE MF TOPONODE \_**](mf-toponode-workqueue-id-attribute.md)
-   [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ (CLASE)**](mf-toponode-workqueue-mmcss-class-attribute.md)

Si la aplicación registra uno de sus propios subprocesos con MMCSS, puede usar este atributo para asociar la cola de trabajo de topología con el grupo MMCSS de la aplicación. Establezca el valor del atributo igual al identificador de tarea que la aplicación recibió cuando se registró con MMCSS. (El identificador de tarea se devuelve en el *parámetro TaskIndex* de la [**función AvSetMmThreadCharacteristics.**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) Para obtener más información, vea el tema [Funciones de proceso y subproceso).](../procthread/process-and-thread-functions.md)

Si desea que MMCSS asigne un nuevo identificador de tarea para la topología, establezca el atributo [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS,**](mf-toponode-workqueue-mmcss-class-attribute.md) pero no establezca el atributo **\_ \_ \_ \_ TASKID MMCSS DE MF TOPONODE WORKQUEUE.**

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[Colas de trabajo](work-queues.md)
</dt> </dl>

 

 
