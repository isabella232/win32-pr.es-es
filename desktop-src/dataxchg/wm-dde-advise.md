---
title: WM_DDE_ADVISE mensaje (Dde.h)
description: Una datos dinámicos Exchange cliente de datos dinámicos Exchange (DDE) envía el mensaje WM DDE ADVISE a una aplicación de servidor DDE para solicitar al servidor que proporcione una actualización para un elemento de datos cada vez que cambia \_ \_ el elemento.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- WM_DDE_ADVISE mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_DDE_ADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832c6991169b71955c0ab21b59d2b55b0b54fc9a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160488"
---
# <a name="wm_dde_advise-message"></a>Mensaje \_ DDE ADVISE de WM \_

Una datos dinámicos Exchange cliente de datos dinámicos Exchange (DDE) envía el mensaje **WM \_ DDE \_ ADVISE** a una aplicación de servidor DDE para solicitar al servidor que proporcione una actualización para un elemento de datos cada vez que cambia el elemento.

Para publicar este mensaje, llame a la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_ADVISE      0x03E2
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana de cliente que publica el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo es un identificador para un objeto de memoria global que contiene una estructura [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) que especifica cómo se enviarán los datos.

La palabra de orden superior contiene un átomo que identifica el elemento de datos solicitado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si una aplicación cliente admite más de un formato de Portapapeles para un único tema y elemento, puede publicar varios mensajes **DE WM \_ DDE \_ ADVISE** para el tema y el elemento, especificando un formato de Portapapeles diferente con cada mensaje. Tenga en cuenta que un servidor solo puede admitir varios formatos para vínculos de datos de acceso rápido, no vínculos de datos de acceso directo.

### <a name="posting"></a>Publicar

La aplicación cliente publica el **mensaje WM \_ DDE \_ ADVISE** llamando a la [**función PostMessage,**](/windows/desktop/api/winuser/nf-winuser-postmessagea) no a [**la función SendMessage.**](/windows/desktop/api/winuser/nf-winuser-sendmessage)

La aplicación cliente asigna el objeto de memoria global mediante la [**función GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc) Asigna el átomo mediante la [**función GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

La aplicación cliente debe crear o reutilizar el parámetro *lParam* **WM \_ DDE \_ ADVISE** llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la [**función ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Si la aplicación receptora (servidor) responde con un mensaje [**\_ DDE \_ ACK**](wm-dde-ack.md) de WM negativo, la aplicación de publicación debe eliminar el objeto .

La **marca fRelease** no se usa en los mensajes **DE \_ DDE \_ ADVISE** de WM, pero su comportamiento de liberar datos es similar al de los mensajes WM [**\_ DDE \_ DATA**](wm-dde-data.md) y [**WM \_ DDE \_ SOAPE,**](wm-dde-poke.md) donde **fRelease** es **TRUE.**

### <a name="receiving"></a>Recepción

La aplicación de servidor publica el [**mensaje \_ WM DDE \_ ACK**](wm-dde-ack.md) para responder de forma positiva o negativa. Al publicar **WM \_ DDE \_ ACK,** la aplicación puede reutilizar el átomo o eliminarlo y crear uno nuevo. Si el **mensaje \_ wm DDE \_ ACK** es positivo, la aplicación debe eliminar el objeto de memoria global; de lo contrario, la aplicación no debe eliminar el objeto.

El servidor debe crear o reutilizar el parámetro *lParam* [**wm \_ DDE \_ ACK**](wm-dde-ack.md) llamando a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la [**función ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

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

[**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise)
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

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**SOLICITUD \_ DDE de WM \_**](wm-dde-request.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

