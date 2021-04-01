---
title: Mensaje de WM_DDE_TERMINATE (DDE. h)
description: Una aplicación Intercambio dinámico de datos (DDE) (cliente o servidor) envía un \_ mensaje de finalización de WM DDE \_ para finalizar una conversación. Para enviar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: 4fc162c0-ccc2-44e3-9c07-d49d7426af8b
keywords:
- Intercambio de datos de mensajes de WM_DDE_TERMINATE
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150160"
---
# <a name="wm_dde_terminate-message"></a>Mensaje de terminación de WM \_ DDE \_

Una aplicación Intercambio dinámico de datos (DDE) (cliente o servidor) envía un mensaje de **\_ \_ finalización de WM DDE** para finalizar una conversación.

Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_TERMINATE       0x03E1
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana de cliente o de servidor que publica el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Config

Mientras se espera la confirmación de la finalización, la aplicación de publicación no debe publicar ningún otro mensaje en la aplicación receptora. Si la aplicación emisora recibe mensajes (distintos de la **\_ \_ terminación de WM DDE**) de la aplicación receptora, debe eliminar todos los subconjuntos o objetos de memoria compartida que acompañan a los mensajes, excepto los objetos de memoria global asociados a los mensajes de [**\_ \_ datos dinámicos**](wm-dde-data.md) de WM o WM que no tienen el conjunto de miembros **fRelease** . [**\_ \_**](wm-dde-poke.md)

### <a name="receiving"></a>Recepción

La aplicación de cliente o de servidor debe responder mediante la publicación de un mensaje de **\_ \_ finalización de WM DDE** .

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

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**\_datos DDE de WM \_**](wm-dde-data.md)
</dt> <dt>

[**hiperdinámico de WM \_ \_**](wm-dde-poke.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md)
</dt> </dl>

 

