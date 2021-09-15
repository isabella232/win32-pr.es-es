---
title: WM_DDE_REQUEST (Dde.h)
description: Una datos dinámicos Exchange cliente de datos dinámicos Exchange (DDE) envía un mensaje DE SOLICITUD de DDE de WM a una aplicación de servidor DDE para solicitar \_ el valor de un elemento de \_ datos. Para publicar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- WM_DDE_REQUEST mensaje Datos Exchange
topic_type:
- apiref
api_name:
- WM_DDE_REQUEST
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7d5eab75d3b7298d78547b17fccfb164a47ae4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570009"
---
# <a name="wm_dde_request-message"></a>Mensaje \_ DE SOLICITUD de DDE de WM \_

Una datos dinámicos Exchange cliente (DDE) envía un mensaje **WM \_ DDE \_ REQUEST** a una aplicación de servidor DDE para solicitar el valor de un elemento de datos.

Para publicar este mensaje, llame a la [**función PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador a la ventana de cliente que envía el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo especifica un formato de Portapapeles estándar o registrado.

La palabra de orden superior contiene un atom que identifica el elemento de datos solicitado al servidor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Publicar

La aplicación cliente asigna el atom mediante una llamada a la [**función GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

### <a name="receiving"></a>Recepción

Si la aplicación receptora (servidor) puede satisfacer la solicitud, responde con un mensaje [**WM \_ DDE \_ DATA**](wm-dde-data.md) que contiene los datos solicitados. De lo contrario, responde con un mensaje [**\_ DDE \_ ACK**](wm-dde-ack.md) de WM negativo.

Al responder con un mensaje [**WM \_ DDE \_ DATA**](wm-dde-data.md) o [**WM \_ DDE \_ ACK,**](wm-dde-ack.md) la aplicación de servidor puede reutilizar el atom o puede eliminar el atom y crear uno nuevo.

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

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

