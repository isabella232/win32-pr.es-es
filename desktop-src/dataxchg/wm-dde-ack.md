---
title: Mensaje de WM_DDE_ACK (DDE. h)
description: El \_ mensaje de \_ confirmación de DDE de WM notifica a una aplicación intercambio dinámico de datos (DDE) de la recepción y el procesamiento de los siguientes mensajes WM DDE, de WM, de ejecución, de WM DDE o de la \_ \_ \_ \_ solicitud de \_ \_ \_ \_ \_ \_ \_ \_ \_ DDE de WM \_ (en algunos casos). Para enviar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- Intercambio de datos de mensajes de WM_DDE_ACK
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079292"
---
# <a name="wm_dde_ack-message"></a>Mensaje de confirmación de \_ DDE de WM \_

El mensaje de **\_ \_ confirmación de DDE de WM** notifica a una aplicación intercambio dinámico de datos (DDE) de la recepción y el procesamiento de los mensajes siguientes: [**WM \_ DDE \_**](wm-dde-poke.md), error de WM, [**\_ \_ ejecución**](wm-dde-execute.md)de WM DDE, [**datos de WM \_ DDE \_**](wm-dde-data.md), [**\_ \_ aviso de DDE**](wm-dde-advise.md)de WM, [**\_ \_ desaconsejar**](wm-dde-unadvise.md)DDE de WM, [**\_ \_ Inicio de WM DDE**](wm-dde-initiate.md)o [**\_ \_ solicitud de DDE de WM**](wm-dde-request.md) (en algunos casos).

Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Cuando se responde a [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md), este parámetro es un identificador de la ventana del servidor que envía el mensaje.

Cuando se responde a [**WM \_ DDE \_ Execute**](wm-dde-execute.md), este parámetro es un identificador de la ventana del servidor que publica el mensaje.

Al responder a todos los demás mensajes, este parámetro es un identificador de la ventana de cliente o de servidor que publica el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Cuando se responde a [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md), la palabra de orden inferior contiene un átomo que identifica la aplicación de respuesta. La palabra de orden superior contiene un átomo que identifica el tema para el que se está estableciendo una conversación.

Cuando se responde a [**WM \_ DDE \_ Execute**](wm-dde-execute.md), la palabra de orden inferior especifica una estructura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contiene una serie de marcas que indican el estado de la respuesta. La palabra de orden superior es un identificador de un objeto de memoria global que contiene la cadena de comandos que se recibió en el mensaje de **\_ \_ ejecución de WM DDE** .

Al responder a todos los demás mensajes, la palabra de orden inferior especifica una estructura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contiene una serie de marcas que indican el estado de la respuesta. La palabra de orden superior contiene un átomo global que identifica el nombre del elemento de datos para el que se envía la respuesta.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Config

Excepto en respuesta al mensaje [**de \_ \_ Inicio de WM DDE**](wm-dde-initiate.md) , la aplicación envía el mensaje de **confirmación de WM \_ DDE \_** mediante una llamada a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , no mediante una llamada a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) . Al responder a **WM \_ DDE \_ iniciar**, la aplicación envía el mensaje de **\_ \_ confirmación de WM DDE** llamando a **SendMessage**. En este caso, ni el Atom del nombre de la aplicación ni el Atom del nombre del tema deben ser **null** (aunque el mensaje de **Inicio de WM \_ \_ DDE** especifique átomos **null** ).

Al confirmar cualquier mensaje con un átomo que lo acompañe, la confirmación de **la \_ \_ confirmación DDE de WM** de aplicación puede volver a usar el átomo que acompaña al mensaje original, o bien puede eliminarlo y crear uno nuevo.

Cuando se confirma [**la \_ \_ ejecución de WM DDE**](wm-dde-execute.md), la aplicación que envía la **confirmación de WM \_ DDE \_** debe volver a usar el objeto de memoria global identificado en el mensaje de **ejecución de WM \_ \_ DDE** original.

Todos los mensajes de **\_ \_ confirmación DDE de WM** publicados deben crear o volver a usar el parámetro *lParam* llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Si una aplicación ha iniciado la finalización de una conversación mediante la publicación de la terminación de [**WM \_ DDE \_**](wm-dde-terminate.md) y está esperando la confirmación, la aplicación en espera no debe confirmar (positiva o negativamente) los mensajes posteriores enviados por la otra aplicación. La aplicación en espera debe eliminar cualquier átomo o objeto de memoria compartida recibido en estos mensajes que intervienen. Los objetos de memoria no deben liberarse si la marca **fRelease** está establecida en **false** en los mensajes de [**\_ \_ datos DDE**](wm-dde-data.md) de WM y WM [**\_ DDE \_**](wm-dde-poke.md) .

### <a name="receiving"></a>Recepción

La aplicación que recibe un mensaje de **\_ \_ confirmación de WM DDE** debe eliminar todos los átomos que acompañan al mensaje. Si la aplicación recibe una **\_ \_ confirmación de WM DDE** en respuesta a un mensaje con un objeto de memoria global que lo acompaña, y el objeto se envió con las marcas **fRelease** establecidas en **false**, la aplicación es responsable de eliminar el objeto.

Si la aplicación recibe un mensaje **de \_ \_ confirmación DDE de WM** negativo publicado en respuesta a un mensaje de [**\_ \_ notificación de DDE de WM**](wm-dde-advise.md) , la aplicación debe eliminar el objeto de memoria global expuesto con el mensaje de **\_ \_ aviso de DDE de WM** original. Si la aplicación recibe un mensaje **de \_ \_ confirmación de DDE de WM** negativo expuesto en respuesta a un mensaje [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_**](wm-dde-poke.md), o de [**\_ \_ ejecución de WM DDE**](wm-dde-execute.md) , la aplicación debe eliminar el objeto de memoria global que se ha publicado con el mensaje de **\_ \_ ejecución** de **\_ \_ datos DDE** de WM original, de **WM \_ DDE \_** o de WM.

La aplicación que recibe un mensaje **de \_ \_ confirmación de DDE de WM** publicado debe liberar el parámetro *lParam* mediante la función [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .

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

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_aviso de DDE de WM \_**](wm-dde-advise.md)
</dt> <dt>

[**\_datos DDE de WM \_**](wm-dde-data.md)
</dt> <dt>

[**ejecución de WM \_ DDE \_**](wm-dde-execute.md)
</dt> <dt>

[**Inicio de WM \_ DDE \_**](wm-dde-initiate.md)
</dt> <dt>

[**hiperdinámico de WM \_ \_**](wm-dde-poke.md)
</dt> <dt>

[**\_solicitud de DDE de WM \_**](wm-dde-request.md)
</dt> <dt>

[**\_finalización de WM DDE \_**](wm-dde-terminate.md)
</dt> <dt>

[**\_DESaconsejar DDE de WM \_**](wm-dde-unadvise.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md)
</dt> </dl>

 

