---
description: Mensaje que se envía a todas las ventanas de nivel superior cuando la función SystemParametersInfo cambia una configuración de todo el sistema o cuando la configuración de directiva ha cambiado.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: WM_SETTINGCHANGE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302f156da905263ed7f3d1d331d4dbb25af5b3e81d9df6136281c7dbc7b3914c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710045"
---
# <a name="wm_settingchange-message"></a>Mensaje \_ WM SETTINGCHANGE

Mensaje que se envía a todas las ventanas de nivel superior cuando la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) cambia una configuración de todo el sistema o cuando la configuración de directiva ha cambiado.

Las aplicaciones deben **enviar WM \_ SETTINGCHANGE** a todas las ventanas de nivel superior cuando realicen cambios en los parámetros del sistema. (Este mensaje no se puede enviar directamente a una ventana). Para enviar el **mensaje WM \_ SETTINGCHANGE** a todas las ventanas de nivel superior, use la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con el *parámetro hwnd* establecido en **HWND \_ BROADCAST**.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Cuando el sistema envía este mensaje como resultado de una llamada a [**SystemParametersInfo,**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) el parámetro *wParam* es el valor del parámetro *uiAction* pasado a la **función SystemParametersInfo.** Para obtener una lista de valores, **vea SystemParametersInfo**.

Cuando el sistema envía este mensaje como resultado de un cambio en la configuración de directiva, este parámetro indica el tipo de directiva que se aplicó. Este valor es 1 si se aplicó la directiva de equipo o cero si se aplicó la directiva de usuario.

Cuando el sistema envía este mensaje como resultado de un cambio en la configuración regional, este parámetro es cero.

Cuando una aplicación envía este mensaje, este parámetro debe ser **NULL.**

</dd> <dt>

*lParam* 
</dt> <dd>

Cuando el sistema envía este mensaje como resultado de una llamada a [**SystemParametersInfo,**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) *lParam* es un puntero a una cadena que indica el área que contiene el parámetro del sistema que se cambió. Este parámetro no suele indicar qué parámetro específico del sistema ha cambiado. (Tenga en cuenta que algunas aplicaciones envían este mensaje con *lParam* establecido en **NULL).** En general, cuando reciba este mensaje, debe comprobar y volver a cargar cualquier configuración de parámetros del sistema que utilice la aplicación.

Esta cadena puede ser el nombre de una clave del Registro o el nombre de una sección del Win.ini archivo. Cuando la cadena es un nombre del Registro, normalmente indica solo el nodo hoja del registro, no la ruta de acceso completa.

Cuando el sistema envía este mensaje como resultado de un cambio en la configuración de la directiva, este parámetro apunta a la cadena "Policy".

Cuando el sistema envía este mensaje como resultado de un cambio en la configuración regional, este parámetro apunta a la cadena "intl".

Para efectuar un cambio en las variables de entorno para el sistema o el usuario, difusione este mensaje con *lParam* establecido en la cadena "Environment".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si procesa este mensaje, devuelva cero.

## <a name="remarks"></a>Comentarios

El parámetro *lParam* indica qué métrica del sistema ha cambiado, por ejemplo, "ConvertibleSlateMode" si se alternó el indicador CONVERTIBLESLATEMODE o "SystemDockMode" si se alternó el indicador DOCKED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de directiva](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
