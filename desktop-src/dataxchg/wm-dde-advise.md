---
title: Mensaje de WM_DDE_ADVISE (DDE. h)
description: Una aplicación cliente de Intercambio dinámico de datos (DDE) envía el \_ mensaje de notificación de DDE de WM \_ a una aplicación de servidor DDE para solicitar al servidor que proporcione una actualización para un elemento de datos cada vez que cambie el elemento.
ms.assetid: b00db740-36a7-4487-abbf-d74b12f5212a
keywords:
- Intercambio de datos de mensajes de WM_DDE_ADVISE
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150212"
---
# <a name="wm_dde_advise-message"></a>Mensaje de aviso de \_ DDE de WM \_

Una aplicación cliente de Intercambio dinámico de datos (DDE) envía el mensaje de **\_ \_ notificación de DDE de WM** a una aplicación de servidor DDE para solicitar al servidor que proporcione una actualización para un elemento de datos cada vez que cambie el elemento.

Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


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

La palabra de orden inferior es un identificador de un objeto de memoria global que contiene una estructura [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) que especifica cómo se van a enviar los datos.

La palabra de orden superior contiene un átomo que identifica el elemento de datos solicitado.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si una aplicación cliente admite más de un formato de Portapapeles para un solo tema y elemento, puede enviar varios mensajes de **\_ \_ notificación de DDE de WM** para el tema y el elemento, especificando un formato de Portapapeles diferente con cada mensaje. Tenga en cuenta que un servidor solo puede admitir varios formatos para vínculos de datos activos, no vínculos de datos semiactivos.

### <a name="posting"></a>Config

La aplicación cliente envía el mensaje de **\_ \_ aviso de DDE de WM** mediante una llamada a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) , no a la función [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) .

La aplicación cliente asigna el objeto de memoria global mediante la función [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Asigna el átomo mediante la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

La aplicación cliente debe crear o volver a usar el parámetro del método *lParam* de **WM \_ DDE \_** para llamar a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Si la aplicación receptora (servidor) responde con un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo, la aplicación de publicación debe eliminar el objeto.

La **marca fRelease** no se utiliza en los mensajes de **\_ \_ notificación de DDE de WM** , pero su comportamiento de liberación de datos es similar al de los mensajes de WM y de [**\_ \_ datos DDE**](wm-dde-data.md) [**de WM donde \_ \_**](wm-dde-poke.md) **fRelease** es **true**.

### <a name="receiving"></a>Recepción

La aplicación de servidor envía el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder de forma positiva o negativa. Al publicar **la \_ \_ confirmación de WM DDE**, la aplicación puede reutilizar el átomo o eliminarlo y crear uno nuevo. Si el mensaje de **\_ \_ confirmación de DDE de WM** es positivo, la aplicación debe eliminar el objeto de memoria global; de lo contrario, la aplicación no debe eliminar el objeto.

El servidor debe crear o volver a usar el parámetro *lParam* de la [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) mediante una llamada a la función [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) o a la función [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

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

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_confirmación de DDE de WM \_**](wm-dde-ack.md)
</dt> <dt>

[**\_datos DDE de WM \_**](wm-dde-data.md)
</dt> <dt>

[**hiperdinámico de WM \_ \_**](wm-dde-poke.md)
</dt> <dt>

[**\_solicitud de DDE de WM \_**](wm-dde-request.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md)
</dt> </dl>

 

