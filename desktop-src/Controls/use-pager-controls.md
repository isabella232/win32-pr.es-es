---
title: Cómo usar los controles de buscapersonas
description: En esta sección se describe cómo implementar el control de paginación en la aplicación.
ms.assetid: 5703FE4B-987E-49DA-9741-F8B45AD26467
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586bfff0c8d8097c4b0e861506bb73f55467b711
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078452"
---
# <a name="how-to-use-pager-controls"></a>Cómo usar los controles de buscapersonas

En esta sección se describe cómo implementar el control de paginación en la aplicación.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="initialize-a-pager-control"></a>Inicializar un control de paginación

Para usar el control de paginación, debe llamar a la función [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con la \_ \_ marca de clase PAGESCROLLER de ICC establecida en el miembro **dwICC** de la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .

### <a name="create-a-pager-control"></a>Crear un control de paginación

Use la API [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de paginación. El nombre de clase del control es [**WC \_ PAGESCROLLER**](common-control-window-classes.md), que se define en commctrl. h. El estilo [**págs \_ horizontal**](pager-control-styles.md) se usa para crear un buscapersonas horizontal y el estilo [**págs \_ Vert**](pager-control-styles.md) se usa para crear un buscapersonas vertical. Dado que se trata de un control secundario, también debe usarse el estilo [**WS \_ Child**](/windows/desktop/winmsg/window-styles) .

Una vez creado el control de paginación, lo más probable es que desee asignarle una ventana contenida. Si la ventana contenida es una ventana secundaria, debe convertir la ventana secundaria en un elemento secundario del control de paginación para que el tamaño y la posición se calculen correctamente. A continuación, asigne la ventana al control de paginación con el mensaje [**PGM \_ SETCHILD**](pgm-setchild.md) . Tenga en cuenta que este mensaje no cambia realmente la ventana primaria de la ventana contenida; simplemente asigna la ventana contenida. Si la ventana contenida es uno de los controles comunes, debe tener el estilo [**CCS \_ NORESIZE**](common-control-styles.md) para evitar que el control intente cambiar su tamaño al tamaño del control de paginación.

### <a name="process-pager-control-notifications"></a>Procesar notificaciones del control de buscapersonas

Como mínimo, es necesario procesar la notificación de [ \_ CALCSIZE de PGN](pgn-calcsize.md) . Si no procesa esta notificación y especifica un valor para el ancho o el alto, no se mostrarán las flechas de desplazamiento en el control de paginación. Esto se debe a que el control de paginación utiliza el ancho o el alto proporcionado en la notificación de CALCSIZE de PGN \_ para determinar el tamaño "ideal" de la ventana contenida.

En el ejemplo siguiente se muestra cómo procesar el caso de notificación [PGN \_ CALCSIZE](pgn-calcsize.md) . En este ejemplo, la ventana contenida es un control de barra de herramientas que contiene un número desconocido de botones con un tamaño desconocido. En el ejemplo se muestra cómo usar el mensaje [**TB \_ GETMAXSIZE**](tb-getmaxsize.md) para determinar el tamaño de todos los elementos de la barra de herramientas. A continuación, el ejemplo coloca el ancho de todos los elementos en el miembro **iWidth** de la estructura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que se pasa a la notificación.


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

[Usar controles de buscapersonas](using-pager-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 