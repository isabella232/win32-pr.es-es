---
title: WM_DDE_TERMINATE mensaje (Dde.h)
description: Una datos dinámicos Exchange (DDE) (cliente o servidor) publica un mensaje WM \_ DDE \_ TERMINATE para finalizar una conversación. Para publicar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_DDE_TERMINATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98d9b4bf2120cb6daa08b6088a8dd39f8a17b8e28c37a3917936a9c49230487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736272"
---
# <a name="wm_dde_terminate-message"></a>Mensaje \_ WM DDE \_ TERMINATE

Una datos dinámicos Exchange (DDE) (cliente o servidor) publica un mensaje **WM \_ DDE \_ TERMINATE** para finalizar una conversación.

Para publicar este mensaje, llame a la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana cliente o servidor que publica el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

### <a name="posting"></a>Publicar

Mientras espera la confirmación de la finalización, la aplicación de publicación no debe publicar ningún otro mensaje en la aplicación receptora. Si la aplicación de envío recibe mensajes (distintos de **WM \_ DDE \_ TERMINATE)** de la aplicación receptora, debe eliminar los átomos u objetos de memoria compartidos que acompañan a los mensajes, excepto los objetos de memoria global asociados a [**mensajes WM \_ DDE \_ SOAPE**](wm-dde-poke.md) o [**WM \_ DDE \_ DATA**](wm-dde-data.md) que no tengan establecido el miembro **fRelease.**

### <a name="receiving"></a>Recepción

La aplicación cliente o servidor debe responder mediante la publicación de un **mensaje WM \_ DDE \_ TERMINATE.**

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

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

