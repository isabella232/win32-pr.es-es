---
title: WM_DDE_ACK mensaje (Dde.h)
description: El mensaje WM DDE ACK notifica a una aplicación datos dinámicos Exchange (DDE) la recepción y el procesamiento de los siguientes mensajes \_ \_ WM \_ DDE WM \_ WM, WM \_ DDE \_ EXECUTE, WM \_ DDE \_ DATA, WM \_ \_ DDE ADVISE, WM \_ DDE \_ UNADVISE, WM DDE INITIATE o \_ WM \_ \_ DDE REQUEST (en algunos \_ casos). Para publicar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK mensaje Datos Exchange
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a407fc6cad7077586539f119dd65be59a507cacd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160491"
---
# <a name="wm_dde_ack-message"></a>Mensaje \_ DDE \_ ACK de WM

El mensaje **\_ DDE \_ ACK** de WM notifica a una aplicación datos dinámicos Exchange (DDE) la recepción y el procesamiento de los mensajes siguientes: [**WM \_ DDE \_ WM WM,**](wm-dde-poke.md) [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md) [**WM \_ DDE \_ DATA,**](wm-dde-data.md) [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) [**WM \_ DDE \_ UNADVISE,**](wm-dde-unadvise.md) [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)o [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) (en algunos casos).

Para publicar este mensaje, llame a la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Al responder a [**WM \_ DDE \_ INITIATE,**](wm-dde-initiate.md)este parámetro es un identificador para la ventana del servidor que envía el mensaje.

Al responder a [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md)este parámetro es un identificador de la ventana del servidor que publica el mensaje.

Al responder a todos los demás mensajes, este parámetro es un identificador para la ventana cliente o servidor que publica el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Al responder a [**WM \_ DDE \_ INITIATE,**](wm-dde-initiate.md)la palabra de orden bajo contiene un atom que identifica la aplicación de respuesta. La palabra de orden superior contiene un atom que identifica el tema para el que se establece una conversación.

Al responder a [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md)la palabra de orden bajo especifica una estructura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contiene una serie de marcas que indican el estado de la respuesta. La palabra de orden superior es un identificador de un objeto de memoria global que contiene la cadena de comando que se recibió en el mensaje **\_ \_ EXECUTE de WM DDE.**

Al responder a todos los demás mensajes, la palabra de orden bajo especifica una estructura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contiene una serie de marcas que indican el estado de la respuesta. La palabra de orden superior contiene un atom global que identifica el nombre del elemento de datos para el que se envía la respuesta.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Publicar

Excepto en respuesta al mensaje [**WM \_ DDE \_ INITIATE,**](wm-dde-initiate.md) la aplicación publica el mensaje **WM \_ DDE \_ ACK** llamando a la [**función PostMessage,**](/windows/desktop/api/winuser/nf-winuser-postmessagea) no llamando a [**la función SendMessage.**](/windows/desktop/api/winuser/nf-winuser-sendmessage) Al responder a **WM \_ DDE \_ INITIATE,** la aplicación envía el mensaje **\_ DDE \_ ACK** de WM mediante una **llamada a SendMessage**. En este caso, ni el atom de nombre de aplicación ni el atom de nombre de tema deben ser **NULL** (incluso si el mensaje **WM \_ DDE \_ INITIATE** especificó atoms **NULL).**

Al confirmar cualquier mensaje con un atom adjunto, la aplicación que publica **WM \_ DDE \_ ACK** puede reutilizar el atom que acompañaba al mensaje original, o bien puede eliminarlo y crear uno nuevo.

Al confirmar [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md), la aplicación que publica **WM \_ DDE \_ ACK** debe reutilizar el objeto de memoria global identificado en el mensaje **EXECUTE de WM \_ DDE \_** original.

Todos los **mensajes de WM \_ DDE \_ ACK** publicados deben crear o reutilizar el parámetro *lParam* llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la [**función ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Si una aplicación ha iniciado la finalización de una conversación mediante la publicación de [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) y está esperando confirmación, la aplicación en espera no debe confirmar (de forma positiva o negativa) los mensajes subsiguientes enviados por la otra aplicación. La aplicación en espera debe eliminar los atoms u objetos de memoria compartida recibidos en estos mensajes que intervienen. Los objetos de memoria no deben liberarse si la marca **fRelease** está establecida en **FALSE** en los mensajes [**WM \_ DDE WM \_ DDE**](wm-dde-poke.md) [**\_ \_ DATA.**](wm-dde-data.md)

### <a name="receiving"></a>Recepción

La aplicación que recibe un **mensaje \_ wm DDE \_ ACK** debe eliminar todos los átomos que acompañan al mensaje. Si la aplicación recibe un **\_ DDE \_ ACK** de WM en respuesta a un mensaje con un objeto de memoria global adjunto y el objeto se envió con las marcas **fRelease** establecidas en **FALSE,** la aplicación es responsable de eliminar el objeto.

Si la aplicación recibe un mensaje **\_ DDE \_ ACK** de WM negativo publicado en respuesta a un mensaje [**DE WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) la aplicación debe eliminar el objeto de memoria global publicado con el mensaje **WM \_ DDE \_ ADVISE** original. Si la aplicación recibe un mensaje **\_ DDE \_ ACK** de WM negativo publicado en respuesta a un mensaje WM [**\_ DDE \_ DATA**](wm-dde-data.md), WM DDE WM WM O [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md) la aplicación debe eliminar el objeto de memoria global publicado con el mensaje **ORIGINAL WM \_ DDE \_ DATA**, **WM \_ DDE WM \_** [**\_ \_ WME**](wm-dde-poke.md)o **WM \_ DDE \_ EXECUTE.**

La aplicación que recibe un mensaje **wm \_ DDE \_ ACK** publicado debe liberar el parámetro *lParam* mediante la [**función FreeDDElParam.**](/windows/desktop/api/Dde/nf-dde-freeddelparam)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Dde.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**DesempaquetarDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)
</dt> <dt>

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md)
</dt> <dt>

[**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**SOLICITUD \_ DE DDE DE \_ WM**](wm-dde-request.md)
</dt> <dt>

[**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md)
</dt> <dt>

[**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

