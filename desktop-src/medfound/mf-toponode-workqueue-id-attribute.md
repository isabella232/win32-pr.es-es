---
description: Especifica una cola de trabajo para una rama de topología.
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: MF_TOPONODE_WORKQUEUE_ID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ba4ab55d2a70b4b0c081544ab43a78719fab537fbf478519bde1e65dfc9e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955095"
---
# <a name="mf_toponode_workqueue_id-attribute"></a>Atributo MF \_ TOPONODE \_ WORKQUEUE \_ ID

Especifica una cola de trabajo para una rama de topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica a los nodos de origen **(MF \_ TOPOLOGY \_ SOURCESTREAM \_ NODE).** El atributo es opcional.

El valor del atributo es un identificador definido por la aplicación para la cola de trabajo.

Las aplicaciones pueden usar este atributo para asignar colas de trabajo a ramas de la topología. Cada nodo de origen de la topología define una rama. La rama incluye todos los nodos de topología que reciben datos de ese nodo.

Si establece este atributo, llame al método [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) en la topología resuelta. Varias ramas de la topología pueden compartir la misma cola de trabajo y las colas de trabajo se pueden volver a usar entre topologías.

> [!Note]  
> El valor de este atributo no es el mismo que el identificador devuelto por la [**función MFAllocateWorkQueue.**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) El valor del atributo es un identificador definido por la aplicación y se usa para asociar ramas de topología con colas de trabajo. Cuando la sesión multimedia asigna una nueva cola de trabajo, almacena internamente el identificador real de cola de trabajo.

 

Si establece este atributo, la aplicación también puede asignar la rama a una tarea del Servicio programador de clases multimedia (MMCSS), estableciendo el atributo [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ CLASS.**](mf-toponode-workqueue-mmcss-class-attribute.md)

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**NODETopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ (CLASE)**](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[Atributos de nodo de topología](topology-node-attributes.md)
</dt> <dt>

[Colas de trabajo](work-queues.md)
</dt> </dl>

 

 




