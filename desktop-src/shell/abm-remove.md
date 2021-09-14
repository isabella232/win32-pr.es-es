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
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361067"
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

## <a name="remarks"></a>Observaciones

Este mensaje hace que el sistema envíe el mensaje de [**notificación \_ ABN POSCHANGED**](abn-poschanged.md) a todas las barras de aplicaciones.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



 

 




