---
description: Se envía cuando un usuario realiza un gesto de lápiz. Una ventana recibe este mensaje a través de su función WindowProc.
ms.assetid: 9433aadf-3440-4249-8f2c-3e22ebc949fb
title: Mensaje de WM_TABLET_FLICK (Tpcshrd. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98c95598ac23f37918c67eec70c2ed205f8a4fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275358"
---
# <a name="wm_tablet_flick-message"></a>\_Mensaje de gesto de Tablet PC de WM \_

Se envía cuando un usuario realiza un gesto de lápiz. Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_FLICK    (WM_TABLET_DEFBASE + 11)     
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Una [**\_ estructura de datos de gestos**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data) que contiene información sobre el gesto de lápiz que se ha producido.

</dd> <dt>

*lParam* 
</dt> <dd>

La [**\_ estructura de punto de gesto**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_point) que especifica dónde se produjo el gesto de lápiz.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Un gesto de lápiz es un gesto de lápiz unidireccional que requiere que el usuario se ponga en contacto con el digitalizador en un movimiento de gesto rápido y sencillo. Un gesto se caracteriza por alta velocidad y un alto grado de recta. Un gesto se identifica por su dirección. Los gestos se pueden realizar en ocho direcciones correspondientes a las direcciones de brújula cardinal y secundaria.

Cuando se produce un gesto de lápiz, Windows notifica primero a una aplicación mediante el envío de un mensaje de **\_ \_ gesto de Tablet PC de WM** , que una ventana recibe a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Devuelva la constante de **\_ \_ \_ máscara controlada** por el gesto de WM, descrita en el apartado de [constantes de gestos](flicks-constants.md), para indicar que la aplicación respondió al mensaje de **\_ \_ gesto de Tablet PC de WM** . Si la aplicación no devuelve el **gesto de la \_ \_ \_ máscara controlada de WM**, Windows realiza la acción predeterminada especificada en el panel de control de gestos mediante el envío de una notificación de seguimiento, como [**WM \_ APPCOMMAND**](../inputdev/wm-appcommand.md), [**WM \_ VSCROLL**](../controls/wm-vscroll.md)o [**WM \_ KEYDOWN**](../inputdev/wm-keydown.md), en función de la acción asociada con el gesto de lápiz.

Tenga precaución al controlar el mensaje de **\_ \_ gestos de Tablet PC de WM** . **WM \_ El \_ gesto de TABLET PC** se pasa a través de la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) . Si llama a métodos en una interfaz COM, ese objeto debe estar dentro del mismo proceso. De lo contrario, COM produce una excepción.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Tpcshrd. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**estructura de los datos de gestos \_**](/windows/desktop/api/tabflicks/ns-tabflicks-flick_data)
</dt> <dt>

[**\_mensaje de gesto de Tablet PC de WM \_**](wm-tablet-flick-message.md)
</dt> <dt>

[gestos de gestos](flicks-gestures.md)
</dt> <dt>

[responder a gestos de lápiz](/previous-versions/windows/desktop/ms703447(v=vs.85))
</dt> </dl>

 

 
