---
description: Una aplicación envía el mensaje WM WININICHANGE a todas las ventanas de nivel superior después de realizar un cambio en \_ el WIN.INI archivo. La función SystemParametersInfo envía este mensaje después de que una aplicación use la función para cambiar una configuración en WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: WM_WININICHANGE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81cfdfeff65c1580f0bd8373fdc5ef1eec409233a9624934ea67ba835ddf805e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810465"
---
# <a name="wm_wininichange-message"></a>Mensaje \_ WININICHANGE de WM

Una aplicación envía el **mensaje \_ WM WININICHANGE** a todas las ventanas de nivel superior después de realizar un cambio en WIN.INI archivo. La [**función SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) envía este mensaje después de que una aplicación use la función para cambiar una configuración en WIN.INI.

> [!Note]  
> El **mensaje \_ WININICHANGE de WM** solo se proporciona por compatibilidad con versiones anteriores del sistema. Las aplicaciones deben usar el [**mensaje \_ WM SETTINGCHANGE.**](wm-settingchange.md)

 

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena que contiene el nombre del parámetro del sistema que se cambió. Por ejemplo, esta cadena puede ser el nombre de una clave del Registro o el nombre de una sección del Win.ini archivo. Este parámetro no es especialmente útil para determinar qué parámetro del sistema ha cambiado. Por ejemplo, cuando la cadena es un nombre del Registro, normalmente indica solo el nodo hoja en el registro, no toda la ruta de acceso. Además, algunas aplicaciones envían este mensaje con *lParam* establecido en **NULL.** En general, cuando reciba este mensaje, debe comprobar y volver a cargar cualquier configuración de parámetros del sistema que utilice la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si procesa este mensaje, devuelva cero.

## <a name="remarks"></a>Comentarios

Para enviar el **mensaje \_ WM WININICHANGE** a todas las ventanas de nivel superior, use la [**función SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con el parámetro *hWnd* establecido en **HWND \_ BROADCAST**.

Las llamadas a funciones que cambian WIN.INI pueden asignarse al registro en su lugar. Esta asignación se produce cuando WIN.INI y la sección que se va a cambiar se especifican en el Registro con la clave siguiente:

**HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ IniFileMapping**

El cambio en la ubicación de almacenamiento no tiene ningún efecto en el comportamiento de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
