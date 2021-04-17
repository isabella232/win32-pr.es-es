---
title: Mensaje de WM_DDE_DATA (DDE. h)
description: Una aplicación de servidor Intercambio dinámico de datos (DDE) envía un \_ mensaje de datos de WM DDE \_ a una aplicación cliente DDE para pasar un elemento de datos al cliente o para notificar al cliente la disponibilidad de un elemento de datos.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- Intercambio de datos de mensajes de WM_DDE_DATA
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f045ff07e01023e6535eb00dcb78400e4c9519a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714580"
---
# <a name="wm_dde_data-message"></a>\_Mensaje de datos DDE de WM \_

Una aplicación de servidor Intercambio dinámico de datos (DDE) envía un mensaje de **\_ \_ datos de WM DDE** a una aplicación cliente DDE para pasar un elemento de datos al cliente o para notificar al cliente la disponibilidad de un elemento de datos.

Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana del servidor que publica el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior es un identificador de un objeto de memoria global que contiene una estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) con los datos e información adicional. El identificador se debe establecer en **null** si el servidor notifica al cliente que el valor del elemento de datos ha cambiado durante un vínculo de datos semiactivos. El cliente establece un vínculo en caliente mediante el envío de un mensaje de [**\_ \_ notificación de WM DDE**](wm-dde-advise.md) con el conjunto de bits **fDeferUpd** .

La palabra de orden superior contiene un átomo que identifica el elemento de datos para el que se envían los datos o la notificación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Config

La aplicación de servidor asigna el objeto de memoria global mediante la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Asigna el átomo mediante la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

El servidor debe crear o reutilizar el parámetro *lParam* de **\_ \_ datos DDE de WM** llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Si la aplicación receptora (cliente) responde con un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo, la aplicación de posting (servidor) debe eliminar el objeto de memoria global; de lo contrario, el cliente debe eliminar el objeto después de extraer su contenido mediante una llamada a la función [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .

Si la aplicación de servidor establece el miembro **fRelease** de la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) en **false**, el servidor es responsable de eliminar el objeto al recibir una confirmación positiva o negativa.

La aplicación de servidor no debe establecer los miembros **fAckReq** y **fRelease** de la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) en **false**. Si ambos miembros están establecidos en **false**, no es posible que el servidor determine Cuándo se debe eliminar el objeto.

### <a name="receiving"></a>Recepción

Si **fAckReq** es **true**, la aplicación cliente debe exponer el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder positiva o negativamente. Al publicar **la \_ \_ confirmación de WM DDE**, el cliente puede volver a usar el átomo, o bien puede eliminarlo y crear uno nuevo.

El cliente debe crear o volver a usar el parámetro *lParam* de la [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) mediante una llamada a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Si **fAckReq** es **false**, la aplicación cliente debe eliminar el átomo.

Si la aplicación de publicación especifica el objeto de memoria global como **null**, la aplicación receptora puede solicitar al servidor que envíe los datos mediante la publicación de un mensaje de [**solicitud de \_ DDE \_ de WM**](wm-dde-request.md) .

Después de procesar un mensaje de **\_ \_ datos de DDE de WM** en el que el objeto de memoria global no es **null**, el cliente debe liberar el objeto, a menos que se cumpla una de las condiciones siguientes:

-   El miembro **fRelease** es **false**.
-   El miembro **fRelease** es **true**, pero la aplicación cliente responde con un mensaje de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>DDE. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_confirmación de DDE de WM \_**](wm-dde-ack.md)
</dt> <dt>

[**\_aviso de DDE de WM \_**](wm-dde-advise.md)
</dt> <dt>

[**hiperdinámico de WM \_ \_**](wm-dde-poke.md)
</dt> <dt>

[**\_solicitud de DDE de WM \_**](wm-dde-request.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md)
</dt> </dl>

 

