---
title: WM_DDE_DATA mensaje (Dde.h)
description: Una aplicación de servidor datos dinámicos Exchange (DDE) envía un mensaje WM DDE DATA a una aplicación cliente DDE para pasar un elemento de datos al cliente o para notificar al cliente la disponibilidad de un elemento de \_ \_ datos.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA mensaje De datos Exchange
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568460"
---
# <a name="wm_dde_data-message"></a>Mensaje \_ DE DATOS de DDE de WM \_

Una aplicación de servidor datos dinámicos Exchange (DDE) envía un mensaje **WM \_ DDE \_ DATA** a una aplicación cliente de DDE para pasar un elemento de datos al cliente o para notificar al cliente la disponibilidad de un elemento de datos.

Para publicar este mensaje, llame a la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


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

La palabra de orden bajo es un identificador de un objeto de memoria global que contiene una estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) con los datos y la información adicional. El identificador debe establecerse en **NULL** si el servidor notifica al cliente que el valor del elemento de datos ha cambiado durante un vínculo de datos en caliente. El cliente que envía un mensaje [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md) con el conjunto de bits **fDeferUpd** establece un vínculo en caliente.

La palabra de orden superior contiene un atom que identifica el elemento de datos para el que se envían los datos o la notificación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Publicar

La aplicación de servidor asigna el objeto de memoria global mediante la [**función GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc) Asigna el atom mediante la [**función GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

El servidor debe crear o reutilizar el parámetro **wm \_ DDE \_ DATA** *lParam* llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la [**función ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Si la aplicación receptora (cliente) responde con un mensaje [**\_ DDE \_ ACK**](wm-dde-ack.md) de WM negativo, la aplicación de publicación (servidor) debe eliminar el objeto de memoria global; de lo contrario, el cliente debe eliminar el objeto después de extraer su contenido llamando a la función [**UnpackDDElParam.**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)

Si la aplicación de servidor establece el miembro **fRelease** de la estructura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) en **FALSE,** el servidor es responsable de eliminar el objeto al recibir una confirmación positiva o negativa.

La aplicación de servidor no debe establecer los miembros **fAckReq** y **fRelease** de la [**estructura DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) en **FALSE.** Si ambos miembros se establecen en **FALSE,** es imposible que el servidor determine cuándo eliminar el objeto.

### <a name="receiving"></a>Recepción

Si **fAckReq** es **TRUE,** la aplicación cliente debe publicar el mensaje [**wm \_ DDE \_ ACK**](wm-dde-ack.md) para responder de forma positiva o negativa. Al publicar **WM \_ DDE \_ ACK,** el cliente puede reutilizar el atom o puede eliminarlo y crear uno nuevo.

El cliente debe crear o reutilizar el parámetro *LParam* [**de \_ \_ DDE ACK**](wm-dde-ack.md) de WM llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la [**función ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Si **fAckReq** es **FALSE,** la aplicación cliente debe eliminar el atom.

Si la aplicación de publicación especificó el objeto de memoria global como **NULL,** la aplicación receptora puede solicitar al servidor que envíe los datos mediante la publicación de un mensaje [**WM \_ DDE \_ REQUEST.**](wm-dde-request.md)

Después de procesar un **mensaje WM \_ DDE \_ DATA** en el que el objeto de memoria global no es **NULL,** el cliente debe liberar el objeto, a menos que se cumple una de las condiciones siguientes:

-   El **miembro fRelease** es **FALSE.**
-   El **miembro fRelease** es **TRUE,** pero la aplicación cliente responde con un mensaje [**wm \_ DDE \_ ACK**](wm-dde-ack.md) negativo.

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

[**DesempaquetarDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

[**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**SOLICITUD \_ DE DDE DE \_ WM**](wm-dde-request.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

