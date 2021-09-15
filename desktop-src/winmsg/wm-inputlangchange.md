---
description: Se envía a la ventana afectada más arriba después de cambiar el idioma de entrada de una aplicación. Debe realizar cualquier configuración específica de la aplicación y pasar el mensaje a la función DefWindowProc, que pasa el mensaje a todas las ventanas secundarias de primer nivel.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Mensaje WM_INPUTLANGCHANGE (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573121"
---
# <a name="wm_inputlangchange-message"></a>Mensaje \_ INPUTLANGCHANGE de WM

Se envía a la ventana afectada más arriba después de cambiar el idioma de entrada de una aplicación. Debe realizar cualquier configuración específica de la aplicación y pasar el mensaje a la función [**DefWindowProc,**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) que pasa el mensaje a todas las ventanas secundarias de primer nivel. Estas ventanas secundarias pueden pasar el mensaje [**a DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) que pase el mensaje a sus ventanas secundarias, y así sucesivamente.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
#define WM_INPUTLANGCHANGE              0x0051
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam*

</dt> <dd>
  
Tipo: **WPARAM**

Página [de códigos](../Intl/code-pages.md) de la nueva configuración regional.

</dd> <dt>

*lParam*

</dt> <dd>
 
Tipo: **LPARAM**

Identificador de configuración regional de entrada **HKL.** Para obtener más información, [vea Idiomas, configuraciones regionales y diseños de teclado.](../inputdev/about-keyboard-input.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver un valor distinto de cero si procesa este mensaje.

## <a name="remarks"></a>Observaciones

Puede recuperar el nombre de [la configuración regional del teclado](../Intl/locale-names.md) mediante la función [LCIDToLocaleName.](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) Con el nombre de configuración regional puede usar funciones [de configuración regional modernas:](/windows/win32/intl/calling-the--locale-name--functions)

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |

## <a name="see-also"></a>Consulte también

**Referencia**

- [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [**WM \_ INPUTLANGCHANGEREQUEST**](wm-inputlangchangerequest.md)

**Conceptual**

- [Windows](windows.md) 
