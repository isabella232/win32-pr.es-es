---
description: Las constantes siguientes identifican las colas de trabajo de Media Foundation estándar.
ms.assetid: c769f876-83ca-4b04-a054-22fa7146310e
title: Identificadores de cola de trabajo (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecff594bad2a4595862f0bc6457644f86949d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667579"
---
# <a name="work-queue-identifiers"></a>Identificadores de cola de trabajo

Las constantes siguientes identifican las colas de trabajo de Media Foundation estándar.

Las aplicaciones deben usar \_ \_ la cola \_ de devolución de llamada de MFASYNC multiproceso o usar una cola de trabajo obtenida de [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) si desean controlar la prioridad de ejecución. Tenga en cuenta que las prioridades de la cola de trabajo de la plataforma predeterminada pueden cambiar dinámicamente cuando una aplicación llama a [**RegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss). Para obtener más información acerca de las colas de trabajos, consulte [colas de trabajo](work-queues.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_STANDARD"></span><span id="mfasync_callback_queue_standard"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_STANDARD</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">En la mayoría de los casos, las aplicaciones deben utilizar <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br/> Esta cola de trabajo se utiliza para las operaciones sincrónicas. El uso de la cola de trabajo estándar puede correr el riesgo de interbloqueo. Las aplicaciones pueden crear una cola sincrónica privada sobre la cola multiproceso mediante <a href="/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue"><strong>MFAllocateSerialWorkQueue</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_RT"></span><span id="mfasync_callback_queue_rt"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_RT</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">No es para uso general de la aplicación.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_IO"></span><span id="mfasync_callback_queue_io"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_IO</strong></dt> <dt>0x00000003</dt> </dl></td>
<td style="text-align: left;">No es para uso general de la aplicación.<br/> Esta cola de trabajo se usa internamente para operaciones de e/s, como la lectura de archivos y la lectura de la red.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_TIMER"></span><span id="mfasync_callback_queue_timer"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_TIMER</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">No es para uso general de la aplicación.<br/> Esta cola de trabajo se utiliza para las devoluciones de llamada periódicas y los elementos de trabajo programados. Las siguientes funciones colocan los elementos de trabajo en esta cola:<br/>
<ul>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfaddperiodiccallback"><strong>MFAddPeriodicCallback</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitem"><strong>MFScheduleWorkItem</strong></a></li>
<li><a href="/windows/desktop/api/mfapi/nf-mfapi-mfscheduleworkitemex"><strong>MFScheduleWorkItemEx</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_MULTITHREADED"></span><span id="mfasync_callback_queue_multithreaded"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong></dt> <dt>0x00000005</dt> </dl></td>
<td style="text-align: left;">En la mayoría de los casos, se debe usar esta cola de trabajo multiproceso. <br/> Esta cola de trabajo se utiliza para las operaciones asincrónicas en Media Foundation.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION"></span><span id="mfasync_callback_queue_long_function"></span><dl> <dt><strong>MFASYNC_CALLBACK_QUEUE_LONG_FUNCTION</strong></dt> <dt>0x00000007</dt> </dl></td>
<td style="text-align: left;">No es para uso general de la aplicación. En su lugar, las aplicaciones deben usar <strong>MFASYNC_CALLBACK_QUEUE_MULTITHREADED</strong>.<br/></td>
</tr>
</tbody>
</table>



Además, se usan las siguientes constantes en relación con las colas de trabajos.



| Constante o valor                                                                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASYNC_CALLBACK_QUEUE_UNDEFINED"></span><span id="mfasync_callback_queue_undefined"></span><dl> <dt>**MFASYNC \_ Cola de devolución de llamada no \_ \_ definida**</dt> <dt>0x00000000</dt> </dl>           | Cola de trabajo no definida.<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK"></span><span id="mfasync_callback_queue_private_mask"></span><dl> <dt>**MFASYNC \_ \_ \_ \_ Máscara privada de cola de devolución de llamada**</dt> <dt>0xFFFF0000</dt> </dl> | Máscara de bits para distinguir las colas de trabajo de plataforma de las creadas mediante una llamada a [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue).<br/> Para una cola de trabajo creada por [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue), el siguiente valor es distinto de cero:<br/> `(identifier & MFASYNC_CALLBACK_QUEUE_PRIVATE_MASK)`<br/> |
| <span id="MFASYNC_CALLBACK_QUEUE_ALL"></span><span id="mfasync_callback_queue_all"></span><dl> <dt>**MFASYNC \_ Cola de devolución de llamada \_ \_ todos**</dt> <dt>0xFFFFFFFF</dt> </dl>                             | Todas las colas de trabajo de la plataforma.<br/>                                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de Media Foundation](media-foundation-constants.md)
</dt> <dt>

[Colas de trabajo](work-queues.md)
</dt> <dt>

[Mejoras en la cola de trabajo y subprocesos](media-foundation-work-queue-and-threading-improvements.md)
</dt> </dl>

 

 




