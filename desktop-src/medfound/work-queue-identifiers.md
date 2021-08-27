---
description: Las siguientes constantes identifican las colas de trabajo Media Foundation estándar.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Identificadores de cola de trabajo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d454e8b2a199a9c132bf6ea287f31d7d3e5102
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470232"
---
# <a name="work-queue-identifiers"></a>Identificadores de cola de trabajo

Las siguientes constantes identifican las colas de trabajo Media Foundation estándar.

Las aplicaciones deben usar MFASYNC CALLBACK QUEUE MULTITHREADED o usar una cola de trabajo obtenida de \_ \_ \_ [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) si quieren controlar la prioridad de ejecución. Tenga en cuenta que las prioridades predeterminadas de la cola de trabajo de la plataforma pueden cambiar dinámicamente cuando una aplicación llama a [**RegisterPlatformWithMMCSS.**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss) Para obtener más información sobre las colas de trabajo, vea [Colas de trabajo.](work-queues.md)




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt><dt>0x00000001</dt></dl> | En la mayoría de los casos, las aplicaciones <strong>deben MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br /> Esta cola de trabajo se usa para las operaciones sincrónicas. El uso de la cola de trabajo estándar puede ejecutar el riesgo de interbloqueo. Las aplicaciones pueden crear una cola sincrónica privada sobre la cola multiproceso mediante <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt><dt>0x00000002</dt></dl> | No para uso general de la aplicación.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt><dt>0x00000003</dt></dl> | No para uso general de la aplicación.<br /> Esta cola de trabajo se usa internamente para operaciones de E/S como leer archivos y leer desde la red.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt><dt>0x00000004</dt></dl> | No para uso general de la aplicación.<br /> Esta cola de trabajo se usa para devoluciones de llamada periódicas y elementos de trabajo programados. Las siguientes funciones ponen elementos de trabajo en esta cola:<br /><ul><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></li><li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></li></ul> | 
| <span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt><dt>0x00000005</dt></dl> | Esta cola de trabajo multiproceso se debe usar en la mayoría de los casos. <br /> Esta cola de trabajo se usa para las operaciones asincrónicas en Media Foundation.<br /> | 
| <span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl><dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt><dt>0x00000007</dt></dl> | No para uso general de la aplicación. En su lugar, las <strong>aplicaciones MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br /> | 




Además, se usan las siguientes constantes en conexión con las colas de trabajo.



| Constante o valor                                                                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**MFASYNC \_ COLA DE \_ DEVOLUCIÓN \_ DE LLAMADA SIN**</dt> <dt>0X00000000</dt> </dl>           | Cola de trabajo sin definir.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**MFASYNC \_ CALLBACK \_ QUEUE PRIVATE MASK \_ \_ 0xFFFF0000**</dt> <dt></dt> </dl> | Máscara de bits para distinguir las colas de trabajo de la plataforma de las creadas mediante una llamada a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).<br/> Para una cola de trabajo creada [**por MFAllocateWorkQueue,**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue)el valor siguiente es distinto de cero:<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**MFASYNC \_ COLA DE \_ DEVOLUCIÓN \_ DE LLAMADA**</dt> <dt>0XFFFFFFFF</dt> </dl>                             | Todas las colas de trabajo de la plataforma.<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> <dt>

[Colas de trabajo](work-queues.md)
</dt> <dt>

[Mejoras de cola de trabajo y subprocesos](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




