---
title: Uso de notificaciones syslink
description: Hay dos mensajes de notificación asociados al control SysLink \ 8212; uno para el mouse (NM CLICK (syslink)) y otro para el teclado \_ (NM \_ RETURN).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb8a3c8f0f589e17e6fe413b8232876e131734aa053b9a091b83e7d94b14b7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132065"
---
# <a name="how-to-use-syslink-notifications"></a>Uso de notificaciones syslink

Hay dos mensajes de notificación asociados al control SysLink: uno para el mouse[ \_ (NM CLICK (syslink) )](nm-click-syslink.md)y otro para el teclado[(NM \_ RETURN](nm-return.md)).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-syslink-notifications"></a>Uso de notificaciones syslink

El código de ejemplo siguiente muestra cómo procesar las notificaciones SysLink que se generan cuando el usuario hace clic en cualquiera de los dos vínculos del [ejemplo anterior.](create-syslink-controls.md) Cuando el usuario hace clic en la dirección URL de Internet, se abre la página web asociada en el explorador predeterminado. Cuando el usuario hace clic en el hipervínculo definido por la aplicación, se muestra un cuadro de mensaje.


```C++
// g_hLink is the handle of the SysLink control.
case WM_NOTIFY:

    switch (((LPNMHDR)lParam)->code)
    {
    
    case NM_CLICK:          // Fall through to the next case.
    
    case NM_RETURN:
        {
            PNMLINK pNMLink = (PNMLINK)lParam;
            LITEM   item    = pNMLink->item;
            
            if ((((LPNMHDR)lParam)->hwndFrom == g_hLink) && (item.iLink == 0))
              {
                ShellExecute(NULL, L"open", item.szUrl, NULL, NULL, SW_SHOW);
              }
            
            else if (wcscmp(item.szID, L"idInfo") == 0)
              {
                MessageBox(hDlg, L"This isn't much help.", L"Example", MB_OK);
              }
            
            break;
        }
    }
    
    break;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de controles SysLink](using-syslink-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




