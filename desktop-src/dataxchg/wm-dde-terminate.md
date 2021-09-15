---
title: WM_DDE_TERMINATE mensaje (Dde.h)
description: Una datos dinámicos Exchange (DDE) (cliente o servidor) publica un mensaje WM \_ DDE \_ TERMINATE para finalizar una conversación. Para publicar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- WM_DDE_TERMINATE mensaje De datos Exchange
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
ms.openlocfilehash: 105b4a7daab87b1311a58a7b5e5805bbd81e73ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466103"
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

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Publicar

Mientras espera la confirmación de la finalización, la aplicación de publicación no debe publicar ningún otro mensaje en la aplicación receptora. Si la aplicación de envío recibe mensajes (distintos de **WM \_ DDE \_ TERMINATE)** de la aplicación receptora, debe eliminar los atoms u objetos de memoria compartida que acompañan a los mensajes, excepto los objetos de memoria global asociados a los mensajes [**WM \_ DDE WM \_ DDE**](wm-dde-poke.md) [**\_ \_ DATA**](wm-dde-data.md) que no tienen el miembro **fRelease** establecido.

### <a name="receiving"></a>Recepción

La aplicación cliente o servidor debe responder mediante la publicación de un **mensaje \_ WM DDE \_ TERMINATE.**

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

 

