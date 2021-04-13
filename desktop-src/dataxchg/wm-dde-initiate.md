---
title: Mensaje de WM_DDE_INITIATE (DDE. h)
description: Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un \_ mensaje de inicio de WM DDE \_ para iniciar una conversación con una aplicación de servidor que responde a los nombres de tema y aplicación especificados.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- Intercambio de datos de mensajes de WM_DDE_INITIATE
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
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422243"
---
# <a name="wm_dde_initiate-message"></a>Mensaje de inicio de WM \_ DDE \_

Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un mensaje de **\_ \_ Inicio de WM DDE** para iniciar una conversación con una aplicación de servidor que responde a los nombres de tema y aplicación especificados. Al recibir este mensaje, se espera que todas las aplicaciones de servidor con nombres que coincidan con la aplicación especificada y que admitan el tema especificado lo confirmen. (Para obtener más información, vea el mensaje de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) ).


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana de cliente que envía el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior contiene un átomo que identifica la aplicación con la que se solicita una conversación. El nombre de la aplicación no puede contener barras diagonales (/) ni barras diagonales inversas ( \) . Estos caracteres están reservados para las implementaciones de red. Si este parámetro es **null**, se solicita una conversación con todas las aplicaciones.

La palabra de orden superior contiene un átomo que identifica el tema para el que se solicita una conversación. Si el tema es **null**, se solicitan las conversaciones de todos los temas disponibles.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si la palabra de orden inferior de *lParam* es **null**, cualquier aplicación de servidor puede responder. Si la palabra de orden superior de *lParam* es **null**, cualquier tema es válido. Al recibir una solicitud de **\_ \_ Inicio de WM DDE** con la palabra de orden superior del parámetro *lParam* establecida en **null**, un servidor debe enviar un mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para cada uno de los temas que admite.

### <a name="sending"></a>Envío

El cliente difunde el mensaje a todas las ventanas de nivel superior estableciendo el primer parámetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) en la **\_ difusión HWND**.

Si la aplicación cliente ya ha obtenido el identificador de ventana del servidor deseado, puede enviar el **\_ \_ Inicio de WM DDE** directamente a la ventana del servidor pasando el identificador de ventana del servidor como primer parámetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).

La aplicación cliente asigna átomos mediante una llamada a la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Cuando [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) devuelve, la aplicación cliente debe eliminar los átomos.

### <a name="receiving"></a>Recepción

Para completar el inicio de una conversación, la aplicación de servidor debe responder con uno o más mensajes de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) , donde cada mensaje es para un tema independiente. Cuando se envía un mensaje de **\_ \_ confirmación de WM DDE** , el servidor debe crear nuevos átomos; no debe reutilizar los átomos enviados con el **\_ \_ Inicio de WM DDE**.

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

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**\_confirmación de DDE de WM \_**](wm-dde-ack.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md)
</dt> </dl>

 

