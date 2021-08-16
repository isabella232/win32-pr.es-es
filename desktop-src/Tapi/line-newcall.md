---
description: El mensaje NEWCALL de TSPI LINE se envía a la función de devolución de llamada LINEEVENT cada vez que llega una nueva llamada que TAPI no ha originado en una línea que \_ TAPI ha abierto.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: LINE_NEWCALL mensaje (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f541f7535e9b41dc66a83b8d033d3ff7adf4d51f6e78f275d2695cb5ae7a35b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761911"
---
# <a name="line_newcall-message"></a>MENSAJE \_ LINE NEWCALL

El mensaje **\_ NEWCALL** de TSPI LINE se envía a la función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) cada vez que llega una nueva llamada que TAPI no ha originado en una línea que TAPI ha abierto. Este debe ser el primer mensaje enviado con respecto a esa llamada. TAPI escribe el identificador *opaco htCall* en la ubicación pasada por el proveedor de servicios como *dwParam2*. Esto proporciona al proveedor de servicios el *valor htCall* que se usará en los mensajes posteriores.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htLine* 
</dt> <dd>

Identificador de objeto opaco TAPI para el dispositivo de línea.

</dd> <dt>

*htCall* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwMsg* 
</dt> <dd>

Valor LINE \_ NEWCALL.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificador opaco del proveedor de servicios para la llamada, de tipo [**HDRVCALL**](hdrvline.md). TAPI pasa este valor como el parámetro *hdCall* para identificar la llamada en procedimientos posteriores que invoca para operar en la llamada.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Puntero de tipo LPHTAPICALL que apunta a [**htapicall.**](htapicall.md) TAPI escribe el identificador opaco TAPI para la llamada a la ubicación indicada. El proveedor de servicios debe guardar este valor y pasarlo como el parámetro *htCall* para identificar la llamada en eventos posteriores que notifica para la llamada.

Este parámetro también puede adquirir un valor **NULL** (consulte la sección Comentarios siguiente).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El proveedor de servicios debe enviar el [**mensaje LINE \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) como el siguiente mensaje para esta llamada. El **evento LINE \_ NEWCALL** es inusual en que también pasa un valor al proveedor de servicios.

Esta función notifica las nuevas llamadas que se originan en el proveedor de servicios (entrantes, salientes, iniciadas en el teléfono, entre otras) para las que TAPI y el proveedor de servicios aún no han intercambiado identificadores opacos. Los identificadores se intercambian para que TAPI y el proveedor de servicios puedan realizar posteriormente solicitudes e informar de eventos que implican la llamada. Dado que estas nuevas llamadas no son necesariamente entrantes, las llamadas pueden estar inicialmente en cualquier estado, no necesariamente en el *estado de la* oferta. Si el proveedor de servicios se inicia y detecta que una o varias llamadas ya están activas en la línea, informa a TAPI de ellas con mensajes **\_ LINE NEWCALL** seguidos de mensajes [**LINE \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) que indican el estado actual. Una nueva llamada saliente, iniciada por el usuario en el teléfono, se notifica con un mensaje **LINE \_ NEWCALL** y el mensaje **LINE \_ CALLSTATE** inicial indicaría que la llamada estaba en estado **DIALTONE** (y, a continuación, continuar desde allí).

Si el proveedor de servicios pasa un gran número de llamadas a TAPI en un período muy corto de tiempo (durante el mismo ciclo de interrupción), TAPI puede quedar atrás en el procesamiento de esas llamadas. Cuando esto sucede, TAPI indica al proveedor de servicios que espere un breve tiempo antes de enviar más llamadas. Lo señala escribiendo un valor **NULL,** en lugar de un [**HTAPICALL**](htapicall.md)válido, en la ubicación a la que apunta el parámetro *dwParam2* **de LINE \_ NEWCALL.** Esto indica que el intento de procesar el identificador de llamada recién ofrecido no se ha realizado correctamente, probablemente debido a una incapacidad temporal para asignar memoria. El proveedor de servicios puede responder quitando la llamada o reenviendo el mensaje **\_ LINE NEWCALL** después de un retraso de programación (durante el cual el proveedor de servicios debe producir el procesador para permitir que TAPI procese otras acciones pendientes). En cualquier caso, no se pueden pasar más mensajes relacionados con la nueva llamada a TAPI hasta que el intercambio del identificador se realiza correctamente. Cuando la ubicación a la que *apunta dwParam2* adquiere un valor distinto de **NULL,** el proveedor de servicios sabe que este valor es un identificador [**HTAPICALL**](htapicall.md) válido para la llamada.

No hay ningún mensaje directamente correspondiente en el nivel de TAPI. Este mensaje se usa en el nivel de TSPI para introducir de forma única e inequívoca una nueva llamada entrante a TAPI y recuperar el identificador opaco TAPI de la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**LINE \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

