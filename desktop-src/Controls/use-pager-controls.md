---
title: Cómo usar controles de paginación
description: En esta sección se describe cómo implementar el control de paginación en la aplicación.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b917943f5f86498bb3cbea2c58842049c4618caf64a66a6b8db1cb2ab86a315b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828647"
---
# <a name="how-to-use-pager-controls"></a>Cómo usar controles de paginación

En esta sección se describe cómo implementar el control de paginación en la aplicación.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="initialize-a-pager-control"></a>Inicializar un control de paginación

Para usar el control de paginación, debe llamar a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con la marca DE CLASE PAGESCROLLER DE PAGESCROLLER establecida en el miembro dwICC de la estructura \_ \_ [**INITCOMMONCONTROLSEX.**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) 

### <a name="create-a-pager-control"></a>Crear un control De paginación

Use [**CreateWindow o**](/windows/desktop/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) API para crear un control de paginación. El nombre de clase del control es [**WC \_ PAGESCROLLER**](common-control-window-classes.md), que se define en Commctrl.h. El [**estilo \_ HORZ**](pager-control-styles.md) de PGS se usa para crear un paginador horizontal y el estilo [**\_ PGS VERT**](pager-control-styles.md) se usa para crear un paginador vertical. Dado que se trata de un control secundario, también se debe usar el estilo CHILD de [**WS. \_**](/windows/desktop/winmsg/window-styles)

Una vez creado el control de paginación, lo más probable es que desee asignarle una ventana independiente. Si la ventana independiente es una ventana secundaria, debe convertirla en un elemento secundario del control de paginación para que el tamaño y la posición se calcule correctamente. A continuación, asigne la ventana al control de paginación con el [**mensaje \_ SETCHILD de PGM.**](pgm-setchild.md) Tenga en cuenta que este mensaje no cambia realmente la ventana primaria de la ventana independiente; simplemente asigna la ventana independiente. Si la ventana independiente es uno de los controles comunes, debe tener el estilo [**\_ CCS NORESIZE**](common-control-styles.md) para evitar que el control intente cambiar su tamaño al tamaño del control de paginación.

### <a name="process-pager-control-notifications"></a>Procesar notificaciones de control de paginación

Como mínimo, es necesario procesar la notificación [PGN \_ CALCSIZE.](pgn-calcsize.md) Si no procesa esta notificación y escribe un valor para el ancho o alto, no se mostrarán las flechas de desplazamiento del control de paginación. Esto se debe a que el control de paginación usa el ancho o alto proporcionados en la notificación PGN CALCSIZE para determinar el tamaño \_ "ideal" de la ventana independiente.

En el ejemplo siguiente se muestra cómo procesar el caso [de notificación \_ PGN CALCSIZE.](pgn-calcsize.md) En este ejemplo, la ventana independiente es un control de barra de herramientas que contiene un número desconocido de botones con un tamaño desconocido. En el ejemplo se muestra cómo usar el mensaje [**\_ TB GETMAXSIZE**](tb-getmaxsize.md) para determinar el tamaño de todos los elementos de la barra de herramientas. A continuación, el ejemplo coloca el ancho de todos los elementos en el miembro **iWidth** de la estructura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que se pasa a la notificación.


```C++
case PGN_SCROLL:{

    LPNMPGSCROLL pScroll = (LPNMPGSCROLL)lParam;
 
    switch(pScroll->iDir){
     
        case PGF_SCROLLLEFT:
        case PGF_SCROLLRIGHT:
        case PGF_SCROLLUP:
        case PGF_SCROLLDOWN:
     
            pScroll->iScroll = 20;
        
            break;
        }
    }
  
return 0;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles de paginación](using-pager-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 