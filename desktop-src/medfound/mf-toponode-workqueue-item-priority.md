---
description: Especifica la prioridad del elemento de trabajo para una bifurcación de la topología.
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275688"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a>MF \_ TOPONODE \_ WORKQUEUE \_ atributo de prioridad de elemento \_

Especifica la prioridad del elemento de trabajo para una bifurcación de la topología.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo se aplica a los nodos de origen (**\_ \_ \_ nodo SOURCESTREAM de topología MF**). El atributo es opcional.

Este atributo requiere el atributo [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) en el mismo nodo.

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
</dt> </dl>

 

 




