---
description: Especifica un identificador de tarea del servicio Programador de clases multimedia (MMCSS) para una bifurcación de topología.
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: MF_TOPONODE_WORKQUEUE_MMCSS_TASKID atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543238"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ atributo TASKID

Especifica un identificador de tarea del servicio Programador de clases multimedia (MMCSS) para una bifurcación de topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**). Este atributo es opcional.

Este atributo se omite a menos que también se establezcan los siguientes atributos:

-   [**identificador de WORKQUEUE de MF \_ TOPONODE \_ \_**](mf-toponode-workqueue-id-attribute.md)
-   [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS ( \_ clase)**](mf-toponode-workqueue-mmcss-class-attribute.md)

Si la aplicación registra uno de sus propios subprocesos con MMCSS, puede usar este atributo para asociar la cola de trabajo de topología al grupo MMCSS de la aplicación. Establezca el valor de atributo igual al identificador de tarea que recibió la aplicación cuando se registró con MMCSS. (El identificador de tarea se devuelve en el parámetro *TaskIndex* de la función [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) . Para obtener más información, vea el tema [Process and Thread Functions](../procthread/process-and-thread-functions.md)).

Si desea que MMCSS asigne un nuevo identificador de tarea para la topología, establezca el atributo de [**\_ clase MF TOPONODE \_ WORKQUEUE \_ MMCSS \_**](mf-toponode-workqueue-mmcss-class-attribute.md) , pero no establezca el atributo **MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID** .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[Colas de trabajo](work-queues.md)
</dt> </dl>

 

 
