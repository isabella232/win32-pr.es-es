---
description: Un mensaje que se envía a todas las ventanas de nivel superior cuando la función SystemParametersInfo cambia una configuración de todo el sistema o cuando la configuración de Directiva ha cambiado.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: Mensaje de WM_SETTINGCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279017"
---
# <a name="wm_settingchange-message"></a>Mensaje de SETTINGCHANGE de WM \_

Un mensaje que se envía a todas las ventanas de nivel superior cuando la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) cambia una configuración de todo el sistema o cuando la configuración de Directiva ha cambiado.

Las aplicaciones deben enviar **WM \_ SETTINGCHANGE** a todas las ventanas de nivel superior cuando realizan cambios en los parámetros del sistema. (Este mensaje no se puede enviar directamente a una ventana). Para enviar el mensaje de **\_ SETTINGCHANGE de WM** a todas las ventanas de nivel superior, use la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) con el parámetro *hWnd* establecido en la **\_ difusión HWND**.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Cuando el sistema envía este mensaje como resultado de una llamada [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , el parámetro *wParam* es el valor del parámetro *uiAction* que se pasa a la función **SystemParametersInfo** . Para obtener una lista de valores, vea **SystemParametersInfo**.

Cuando el sistema envía este mensaje como resultado de un cambio en la configuración de la Directiva, este parámetro indica el tipo de directiva que se ha aplicado. Este valor es 1 si se ha aplicado la Directiva de equipo o cero si se ha aplicado la Directiva de usuario.

Cuando el sistema envía este mensaje como resultado de un cambio en la configuración regional, este parámetro es cero.

Cuando una aplicación envía este mensaje, este parámetro debe ser **null**.

</dd> <dt>

*lParam* 
</dt> <dd>

Cuando el sistema envía este mensaje como resultado de una llamada [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , *lParam* es un puntero a una cadena que indica el área que contiene el parámetro del sistema que se ha cambiado. Normalmente, este parámetro no indica qué parámetro del sistema concreto cambió. (Tenga en cuenta que algunas aplicaciones envían este mensaje con *lParam* establecido en **null**). En general, cuando reciba este mensaje, debe comprobar y volver a cargar cualquier configuración de parámetros del sistema utilizada por la aplicación.

Esta cadena puede ser el nombre de una clave del registro o el nombre de una sección del archivo de Win.ini. Cuando la cadena es un nombre de registro, normalmente solo indica el nodo hoja del registro, no la ruta de acceso completa.

Cuando el sistema envía este mensaje como resultado de un cambio en la configuración de la Directiva, este parámetro señala a la cadena "Policy".

Cuando el sistema envía este mensaje como resultado de un cambio en la configuración regional, este parámetro señala a la cadena "intl".

Para aplicar un cambio en las variables de entorno del sistema o del usuario, difunda este mensaje con *lParam* establecido en la cadena "Environment".

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si procesa este mensaje, devuelve cero.

## <a name="remarks"></a>Observaciones

El parámetro *lParam* indica qué métrica del sistema ha cambiado, por ejemplo, "ConvertibleSlateMode" si el indicador ConvertibleSlateMode se ha modificado o "SystemDockMode" si el indicador acoplado está activado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Directiva](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
