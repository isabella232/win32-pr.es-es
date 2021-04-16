---
description: El mensaje NEWCALL de la línea de TSPI \_ se envía a la función de devolución de llamada LINEEVENT cada vez que se recibe una nueva llamada que TAPI no ha originado en una línea abierta por TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: Mensaje de LINE_NEWCALL (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690387"
---
# <a name="line_newcall-message"></a>Mensaje de línea \_ NEWCALL

El mensaje **\_ NEWCALL** de la línea de TSPI se envía a la función de devolución de llamada [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) cada vez que se recibe una nueva llamada que TAPI no ha originado en una línea abierta por TAPI. Este debe ser el primer mensaje enviado con respecto a esa llamada. TAPI escribe el identificador opaco *htCall* en la ubicación pasada por el proveedor de servicios como *dwParam2*. Esto proporciona al proveedor de servicios el valor *htCall* que se va a usar en los mensajes posteriores.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htLine* 
</dt> <dd>

El identificador de objeto opaco TAPI para el dispositivo de línea.

</dd> <dt>

*htCall* 
</dt> <dd>

Sin usar.

</dd> <dt>

*dwMsg* 
</dt> <dd>

La línea de valor \_ NEWCALL.

</dd> <dt>

*dwParam1* 
</dt> <dd>

El identificador opaco del proveedor de servicios para la llamada, de tipo [**HDRVCALL**](hdrvline.md). TAPI pasa este valor como el parámetro *hdCall* para identificar la llamada en los procedimientos subsiguientes que invoca para operar en la llamada.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Puntero de tipo LPHTAPICALL que señala a un [**HTAPICALL**](htapicall.md). TAPI escribe el identificador opaco de TAPI para la llamada a la ubicación indicada. El proveedor de servicios debe guardar este valor y pasarlo como el parámetro *htCall* para identificar la llamada en los eventos posteriores que notifica a la llamada.

Este parámetro también puede adquirir un valor **null** (vea la sección Comentarios siguiente).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Sin usar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El proveedor de servicios debe enviar el mensaje [**line \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) como el siguiente mensaje para esta llamada. El evento **line \_ NEWCALL** es inusual en que también devuelve un valor al proveedor de servicios.

Esta función informa de todas las llamadas nuevas que se originan en el proveedor de servicios (entrante, saliente, iniciada en el teléfono, etc.) para las que TAPI y el proveedor de servicios aún no han intercambiado los identificadores opacos. Los identificadores se intercambian para que TAPI y el proveedor de servicios puedan crear solicitudes y eventos de informe que impliquen la llamada. Dado que estas nuevas llamadas no están necesariamente entrantes, las llamadas pueden estar inicialmente en cualquier Estado, no necesariamente en el estado de la *oferta* . Si el proveedor de servicios se inicia y detecta que una o más llamadas ya están activas en la línea, informa a TAPI de ellas con mensajes de **línea \_ NEWCALL** seguidos de los mensajes de [**línea \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) que indican el estado actual. Una nueva llamada de salida, iniciada en el teléfono por el usuario, se notificará con un mensaje **line \_ NEWCALL** y el **mensaje \_ CALLSTATE** de la línea inicial indicaría que la llamada se encontraba en el estado **ditono** (y continuaría desde allí).

Si el proveedor de servicios pasa un gran número de llamadas a TAPI en un período de tiempo muy breve (durante el mismo ciclo de interrupción), TAPI puede volver a iniciar sesión en el procesamiento de esas llamadas. Cuando esto sucede, TAPI indica al proveedor de servicios que espere un poco de tiempo antes de enviar más llamadas. Indica esto escribiendo un valor **null**, en lugar de un [**HTAPICALL**](htapicall.md)válido, en la ubicación a la que señala el parámetro *dwParam2* de la **línea \_ NEWCALL**. Esto indica que el intento de procesar el identificador de llamada recién ofrecido no se realizó correctamente, probablemente debido a una imposibilidad temporal de asignar memoria. El proveedor de servicios puede responder quitando la llamada o reenviando el mensaje **de \_ NEWCALL de línea** después de un retraso de programación (durante el cual el proveedor de servicios debe proporcionar el procesador para permitir que TAPI procese otras acciones pendientes). En cualquier caso, no se pueden pasar más mensajes con respecto a la nueva llamada a TAPI hasta que el intercambio de identificadores se realice correctamente. Cuando la ubicación a la que apunta *dwParam2* adquiere un valor distinto de **null** , el proveedor de servicios sabe que este valor es un identificador [**HTAPICALL**](htapicall.md) válido para la llamada.

No hay ningún mensaje directamente correspondiente en el nivel de TAPI. Este mensaje se usa en el nivel TSPI para introducir de forma única y sin ambigüedad una nueva llamada entrante a TAPI y recuperar el identificador opaco de TAPI para la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LÍNEA \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))
</dt> <dt>

[**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

