---
title: Cómo crear un botón
description: Para crear botones dinámicamente, se usa la función CreateWindow o CreateWindowEx. En este tema se muestra cómo usar la función CreateWindow para crear un botón de método de envío predeterminado.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dadc53f91f773e5fce9e29bdf1ae50cc59bfdfd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078632"
---
# <a name="how-to-create-a-button"></a>Cómo crear un botón

Para crear botones dinámicamente, se usa la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . En este tema se muestra cómo usar la función **CreateWindow** para crear un botón de método de envío predeterminado.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Utilice la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para crear un control de botón.

En el siguiente ejemplo de C++, el parámetro *\_ hWnd de m* es el identificador de la ventana primaria. El estilo [**BS \_ DEFPUSHBUTTON**](button-styles.md) especifica que se debe crear un botón de envío predeterminado. Tenga en cuenta que los valores de tamaño y posición deben especificarse porque el uso de **CW \_ USEDEFAULT** para un botón establece los valores en cero.


```C++
HWND hwndButton = CreateWindow( 
    L"BUTTON",  // Predefined class; Unicode assumed 
    L"OK",      // Button text 
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_DEFPUSHBUTTON,  // Styles 
    10,         // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu.
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed.
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los botones](about-buttons.md)
</dt> <dt>

[Referencia de control de botón](bumper-button-button-control-reference.md)
</dt> <dt>

[Usar botones](using-buttons.md)
</dt> <dt>

[Botón](buttons.md)
</dt> </dl>

 

 