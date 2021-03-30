---
title: Mensaje de WM_DDE_REQUEST (DDE. h)
description: Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un \_ \_ mensaje de solicitud de WM DDE a una aplicación de servidor DDE para solicitar el valor de un elemento de datos. Para enviar este mensaje, llame a la función PostMessage con los parámetros siguientes.
ms.assetid: 922452d2-455c-43e1-a8a8-e3c52b0fab51
keywords:
- Intercambio de datos de mensajes de WM_DDE_REQUEST
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801964"
---
# <a name="wm_dde_request-message"></a>Mensaje de solicitud de \_ DDE de WM \_

Una aplicación cliente de Intercambio dinámico de datos (DDE) envía un mensaje de **\_ \_ solicitud de WM DDE** a una aplicación de servidor DDE para solicitar el valor de un elemento de datos.

Para enviar este mensaje, llame a la función [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con los parámetros siguientes.


```C++
#define WM_DDE_REQUEST     0x03E6
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana de cliente que envía el mensaje.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica un formato de Portapapeles estándar o registrado.

La palabra de orden superior contiene un átomo que identifica el elemento de datos solicitado desde el servidor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

### <a name="posting"></a>Config

La aplicación cliente asigna el átomo llamando a la función [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

### <a name="receiving"></a>Recepción

Si la aplicación receptora (servidor) puede satisfacer la solicitud, responde con un mensaje [**de \_ \_ datos de WM DDE**](wm-dde-data.md) que contiene los datos solicitados. De lo contrario, responde con un mensaje [**de \_ \_ confirmación DDE de WM**](wm-dde-ack.md) negativo.

Cuando responde con un mensaje [**de \_ \_ datos DDE de WM**](wm-dde-data.md) o de [**\_ \_ confirmación DDE de WM**](wm-dde-ack.md) , la aplicación de servidor puede reutilizar el átomo o eliminar el átomo y crear uno nuevo.

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

[**\_datos DDE de WM \_**](wm-dde-data.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md)
</dt> </dl>

 

