---
title: WM_DDE_UNADVISE mensaje (Dde.h)
description: Una datos dinámicos Exchange cliente de datos dinámicos Exchange (DDE) envía un mensaje \_ WM DDE UNADVISE para informar a una aplicación de servidor DDE de que el elemento especificado o un formato de Portapapeles determinado para el elemento ya no se deben \_ actualizar.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- WM_DDE_UNADVISE mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_DDE_UNADVISE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dba83badcb689789d2654d99780bcb8cc503511d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242883"
---
# <a name="wm_dde_unadvise-message"></a>Mensaje \_ WM DDE \_ UNADVISE

Una aplicación cliente datos dinámicos Exchange (DDE) envía un mensaje WM **\_ DDE \_ UNADVISE** para informar a una aplicación de servidor DDE de que el elemento especificado o un formato de Portapapeles determinado para el elemento ya no se deben actualizar. Esto finaliza el vínculo de datos en caliente o en caliente para el elemento especificado.

Para publicar este mensaje, llame a la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador a la ventana del cliente que envía el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo especifica el formato del Portapapeles del elemento para el que se va a retirar la solicitud de actualización. Si es **NULL, se** van a finalizar todas las conversaciones activas de [**\_ DDE \_ ADVISE**](wm-dde-advise.md) de WM para el elemento.

La palabra de orden superior contiene un átomo global que identifica el elemento para el que se va a retirar la solicitud de actualización. Si es **NULL, se** finalizarán todos los vínculos [**\_ DDE \_ ADVISE**](wm-dde-advise.md) de WM activos asociados a la conversación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La aplicación cliente asigna la palabra de orden superior *de lParam* mediante una llamada a la [**función GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

La aplicación de servidor publica el [**mensaje \_ WM DDE \_ ACK**](wm-dde-ack.md) para responder de forma positiva o negativa. Al publicar **WM \_ DDE \_ ACK**, el servidor puede reutilizar el átomo o puede eliminar el átomo y crear uno nuevo.

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

**Conceptual**
</dt> <dt>

[Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

