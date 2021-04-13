---
title: Mensaje de WM_DDE_UNADVISE (DDE. h)
description: Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un \_ \_ mensaje de desaconsejar DDE de WM para informar a una aplicación de servidor DDE de que el elemento especificado o un formato de Portapapeles determinado para el elemento ya no debe actualizarse.
ms.assetid: 9a5f9a86-e6fa-450e-b8bf-f20042c7e6d1
keywords:
- Intercambio de datos de mensajes de WM_DDE_UNADVISE
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492197"
---
# <a name="wm_dde_unadvise-message"></a>Mensaje de no notificación de DDE de WM \_ \_

Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un mensaje de **\_ \_ desaconsejar DDE de WM** para informar a una aplicación de servidor DDE de que el elemento especificado o un formato de Portapapeles determinado para el elemento ya no debe actualizarse. Esto finaliza el vínculo de datos activo o activo para el elemento especificado.

Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_UNADVISE        0x03E3
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana de cliente que envía el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica el formato del Portapapeles del elemento para el que se retira la solicitud de actualización. Si es **null**, todas las conversaciones [**de \_ \_ notificaciones de DDE de WM**](wm-dde-advise.md) activa para el elemento se terminarán.

La palabra de orden superior contiene un átomo global que identifica el elemento para el que se retira la solicitud de actualización. Si es **null**, se terminarán todos los vínculos de [**aviso de WM \_ DDE \_**](wm-dde-advise.md) activos asociados a la conversación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La aplicación cliente asigna la palabra de orden superior de *lParam* mediante una llamada a la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

La aplicación de servidor envía el mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) para responder de forma positiva o negativa. Al publicar **la \_ \_ confirmación de WM DDE**, el servidor puede volver a usar el átomo, o bien puede eliminar el átomo y crear uno nuevo.

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

[**\_aviso de DDE de WM \_**](wm-dde-advise.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md)
</dt> </dl>

 

