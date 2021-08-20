---
title: WM_DDE_INITIATE mensaje (Dde.h)
description: Una datos dinámicos Exchange cliente de datos dinámicos Exchange (DDE) envía un mensaje WM DDE INITIATE para iniciar una conversación con una aplicación de servidor que responda a los nombres de aplicación y \_ \_ tema especificados.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d2d5cf46221e268cf27f7557349185b32aafff65bdd20b0ac20063fde151a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915153"
---
# <a name="wm_dde_initiate-message"></a>Mensaje \_ WM DDE \_ INITIATE

Una datos dinámicos Exchange cliente (DDE) envía un mensaje **WM \_ DDE \_ INITIATE** para iniciar una conversación con una aplicación de servidor que responda a los nombres de aplicación y tema especificados. Tras recibir este mensaje, se espera que todas las aplicaciones de servidor con nombres que coincidan con la aplicación especificada y que admitan el tema especificado la confirmen. (Para obtener más información, vea el mensaje [**\_ WM DDE \_ ACK).**](wm-dde-ack.md)


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador a la ventana del cliente que envía el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo contiene un átomo que identifica la aplicación con la que se solicita una conversación. El nombre de la aplicación no puede contener barras diagonales (/) ni barras diagonales inversas ( \\ ). Estos caracteres están reservados para implementaciones de red. Si este parámetro es **NULL,** se solicita una conversación con todas las aplicaciones.

La palabra de orden superior contiene un átomo que identifica el tema para el que se solicita una conversación. Si el tema es **NULL, se** solicitan conversaciones para todos los temas disponibles.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Si la palabra de orden bajo de *lParam* **es NULL,** cualquier aplicación de servidor puede responder. Si la palabra de orden superior de *lParam* **es NULL,** cualquier tema es válido. Al recibir una solicitud **WM \_ DDE \_ INITIATE** con la palabra de orden superior del parámetro *lParam* establecida en **NULL,** un servidor debe enviar un mensaje [**WM \_ DDE \_ ACK**](wm-dde-ack.md) para cada uno de los temas que admite.

### <a name="sending"></a>Envío

El cliente difunde el mensaje a todas las ventanas de nivel superior estableciendo el primer parámetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) en **HWND \_ BROADCAST.**

Si la aplicación cliente ya ha obtenido el identificador de ventana del servidor deseado, puede enviar **WM \_ DDE \_ INITIATE** directamente a la ventana del servidor pasando el identificador de ventana del servidor como primer parámetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).

La aplicación cliente asigna átomos mediante una llamada a la [**función GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

Cuando [**se devuelve SendMessage,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) la aplicación cliente debe eliminar los átomos.

### <a name="receiving"></a>Recepción

Para completar el inicio de una conversación, la aplicación de servidor debe responder con uno o varios mensajes [**\_ wm DDE \_ ACK,**](wm-dde-ack.md) donde cada mensaje es para un tema independiente. Al enviar **el \_ mensaje WM DDE \_ ACK,** el servidor debe crear nuevos átomos; no debe reutilizar los átomos enviados con **WM \_ DDE \_ INITIATE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>Dde.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

