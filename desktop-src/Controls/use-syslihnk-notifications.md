---
title: Cómo usar notificaciones de SysLink
description: Hay dos mensajes de notificación asociados al control SysLink \ 8212; uno para el mouse (NM \_ click (SysLink)) y otro para el teclado ( \_ Return nm).
ms.assetid: 77E80EB2-180B-4EDD-9FB5-9930E8886CA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864a2b8942b1244be51f5c284e6ce07d973ed4db
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "105656321"
---
# <a name="how-to-use-syslink-notifications"></a>Cómo usar notificaciones de SysLink

Hay dos mensajes de notificación asociados al control SysLink: uno para el mouse ([nm \_ click (SysLink)](nm-click-syslink.md)) y otro para el teclado ([nm \_ Return](nm-return.md)).

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-syslink-notifications"></a>Usar notificaciones de SysLink

En el ejemplo de código siguiente se muestra cómo procesar las notificaciones de SysLink que se generan cuando el usuario hace clic en cualquiera de los dos vínculos del [ejemplo anterior](create-syslink-controls.md). Cuando el usuario hace clic en la dirección URL de Internet, se abre la página web asociada en el explorador predeterminado. Cuando el usuario hace clic en el hipervínculo definido por la aplicación, se muestra un cuadro de mensaje.


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

[Usar controles SysLink](using-syslink-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




