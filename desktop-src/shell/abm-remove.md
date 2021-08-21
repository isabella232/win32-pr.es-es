---
description: Anula el registro de una barra de aplicaciones quitándosela de la lista interna del sistema. El sistema ya no envía mensajes de notificación a la barra de aplicaciones ni impide que otras aplicaciones utilicen el área de pantalla que usa la barra de aplicaciones.
title: ABM_REMOVE mensaje (Shellapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c32fd2c7a12fc8146a01d3722b31b46bad01f61b526397806a5121b7381b069e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861712"
---
# <a name="abm_remove-message"></a>Mensaje REMOVE de ABM \_

Anula el registro de una barra de aplicaciones quitándosela de la lista interna del sistema. El sistema ya no envía mensajes de notificación a la barra de aplicaciones ni impide que otras aplicaciones utilicen el área de pantalla que usa la barra de aplicaciones.


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una [**estructura APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contiene el identificador de la barra de aplicaciones para anular el registro. Debe especificar los **miembros cbSize** y **hWnd** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

Este mensaje hace que el sistema envíe el mensaje de [**notificación \_ ABN POSCHANGED**](abn-poschanged.md) a todas las barras de aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




