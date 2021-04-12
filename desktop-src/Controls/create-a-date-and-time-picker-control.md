---
title: Cómo crear un control de selector de fecha y hora
description: En este tema se muestra cómo crear dinámicamente un control de selector de fecha y hora (DTP).
ms.assetid: D4ACA939-3004-48D3-ADD9-FC5E53128BA2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1253a2972b8d858a7440b3e472d5b3aa347b8175
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104271373"
---
# <a name="how-to-create-a-date-and-time-picker-control"></a>Cómo crear un control de selector de fecha y hora

En este tema se muestra cómo crear dinámicamente un control de selector de fecha y hora (DTP). El ejemplo de código de C++ que lo acompaña crea un control de DTP en un cuadro de diálogo no modal. Usa el estilo [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) para permitir que el usuario simule la desactivación de la fecha dentro del control.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="step-1"></a>Paso 1:

Registre la clase de ventana llamando a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) y especificando el \_ \_ bit de clases de fecha de ICC en la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) correspondiente.


```C++
 INITCOMMONCONTROLSEX icex;

 icex.dwSize = sizeof(icex);
 icex.dwICC = ICC_DATE_CLASSES;

 InitCommonControlsEx(&icex);
```



### <a name="step-2"></a>Paso 2:

Para crear el control de DTP, utilice la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Especifique [**la \_ clase DATETIMEPICK**](common-control-window-classes.md) como clase de ventana y pase el identificador al cuadro de diálogo primario.

En el siguiente ejemplo de código de C++ se usa la función [**CreateDialog**](/windows/desktop/api/winuser/nf-winuser-createdialoga) para crear un cuadro de diálogo no modal. A continuación, llama a **CreateWindowEx** para crear el control de DTP.


```C++
  hwndDlg = CreateDialog  (g_hinst,
                           MAKEINTRESOURCE(IDD_DIALOG1),
                           hwndMain,
                           DlgProc);

  if(hwndDlg)
      hwndDP = CreateWindowEx(0,
                           DATETIMEPICK_CLASS,
                           TEXT("DateTime"),
                           WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                           20,50,220,20,
                           hwndDlg,
                           NULL,
                           g_hinst,
                           NULL);
```



## <a name="complete-example"></a>Ejemplo completo


```C++
//  CreateDatePick creates a DTP control within a dialog box.
//  Returns the handle to the new DTP control if successful, or NULL 
//  otherwise.
// 
//    hwndMain - The handle to the main window.
//    g_hinst  - global handle to the program instance.

HWND WINAPI CreateDatePick(HWND hwndMain)
{
    HWND hwndDP = NULL;
    HWND hwndDlg = NULL;

    INITCOMMONCONTROLSEX icex;

    icex.dwSize = sizeof(icex);
    icex.dwICC = ICC_DATE_CLASSES;

    InitCommonControlsEx(&icex);

    hwndDlg = CreateDialog  (g_hinst,
                             MAKEINTRESOURCE(IDD_DIALOG1),
                             hwndMain,
                             DlgProc);

    if(hwndDlg)
        hwndDP = CreateWindowEx(0,
                             DATETIMEPICK_CLASS,
                             TEXT("DateTime"),
                             WS_BORDER|WS_CHILD|WS_VISIBLE|DTS_SHOWNONE,
                             20,50,220,20,
                             hwndDlg,
                             NULL,
                             g_hinst,
                             NULL);

    return (hwndDP);
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de selector de fecha y hora](using-date-and-time-picker.md)
</dt> <dt>

[Referencia de control de selector de fecha y hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 