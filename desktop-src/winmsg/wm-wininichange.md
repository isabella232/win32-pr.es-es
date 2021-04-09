---
description: Una aplicación envía el mensaje de WININICHANGE de WM \_ a todas las ventanas de nivel superior después de hacer un cambio en el archivo de WIN.INI. La función SystemParametersInfo envía este mensaje después de que una aplicación utilice la función para cambiar una configuración en WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: Mensaje de WM_WININICHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001107"
---
# <a name="wm_wininichange-message"></a>Mensaje de WININICHANGE de WM \_

Una aplicación envía el mensaje de **\_ WININICHANGE de WM** a todas las ventanas de nivel superior después de hacer un cambio en el archivo de WIN.INI. La función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) envía este mensaje después de que una aplicación utilice la función para cambiar una configuración en WIN.INI.

> [!Note]  
> El mensaje de **\_ WININICHANGE de WM** solo se proporciona para ofrecer compatibilidad con versiones anteriores del sistema. Las aplicaciones deben usar el mensaje de [**\_ SETTINGCHANGE de WM**](wm-settingchange.md) .

 

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Un puntero a una cadena que contiene el nombre del parámetro del sistema que se cambió. Por ejemplo, esta cadena puede ser el nombre de una clave del registro o el nombre de una sección del archivo de Win.ini. Este parámetro no es especialmente útil para determinar qué parámetro del sistema ha cambiado. Por ejemplo, cuando la cadena es un nombre de registro, normalmente solo indica el nodo hoja del registro, no la ruta de acceso completa. Además, algunas aplicaciones envían este mensaje con *lParam* establecido en **null**. En general, cuando reciba este mensaje, debe comprobar y volver a cargar cualquier configuración de parámetros del sistema utilizada por la aplicación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Si procesa este mensaje, devuelve cero.

## <a name="remarks"></a>Observaciones

Para enviar el mensaje de **\_ WININICHANGE de WM** a todas las ventanas de nivel superior, use la función [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) con el parámetro *hWnd* establecido en la **\_ difusión HWND**.

En su lugar, las llamadas a funciones que cambian WIN.INI pueden estar asignadas al registro. Esta asignación se produce cuando WIN.INI y la sección que se va a cambiar se especifican en el registro con la siguiente clave:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**

El cambio en la ubicación de almacenamiento no tiene ningún efecto en el comportamiento de este mensaje.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
