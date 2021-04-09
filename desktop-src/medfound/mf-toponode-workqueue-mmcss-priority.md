---
description: Especifica la prioridad relativa de subprocesos para una bifurcación de la topología.
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154981"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ prioridad atributo

Especifica la prioridad relativa de subprocesos para una bifurcación de la topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**). El atributo es opcional.

Este atributo requiere los atributos de clase [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) y [MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) en el mismo nodo.

El valor del atributo es la prioridad de subproceso relativa de la cola de trabajo para esta rama de la topología. El [servicio Programador de clases multimedia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) utiliza la prioridad relativa cuando establece la prioridad del subproceso. Para obtener más información, vea [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[Mejoras en la cola de trabajo y subprocesos](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**identificador de WORKQUEUE de MF \_ TOPONODE \_ \_**](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
