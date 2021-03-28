---
description: Anula el registro de una Appbar quitando la lista interna del sistema. El sistema ya no envía mensajes de notificación al Appbar o impide que otras aplicaciones utilicen el área de pantalla utilizada por el Appbar.
title: Mensaje de ABM_REMOVE (ShellAPI. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907735"
---
# <a name="abm_remove-message"></a>ABN \_ quitar mensaje

Anula el registro de una Appbar quitando la lista interna del sistema. El sistema ya no envía mensajes de notificación al Appbar o impide que otras aplicaciones utilicen el área de pantalla utilizada por el Appbar.


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pabd* 
</dt> <dd>

Puntero a una estructura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contiene el identificador de la Appbar cuyo registro se va a anular. Debe especificar los miembros **cbSize** y **hWnd** al enviar este mensaje; se omiten todos los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **true**.

## <a name="remarks"></a>Observaciones

Este mensaje hace que el sistema envíe el mensaje de notificación [**ABN \_ POSCHANGED**](abn-poschanged.md) a todos los appbars.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



 

 




