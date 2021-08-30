---
title: Cómo crear un botón
description: Para crear botones dinámicamente, use las funciones CreateWindow o CreateWindowEx. En este tema se muestra cómo usar la función CreateWindow para crear un botón de inserción predeterminado.
ms.assetid: A8C56D09-90A3-4C70-9907-61390521D1DA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4940016eaab8f64cd82f18579b31b13f2835ab8a0de00752eabfe81da316d6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920925"
---
# <a name="how-to-create-a-button"></a>Cómo crear un botón

Para crear botones dinámicamente, use las [**funciones CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) [**o CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) En este tema se muestra cómo usar la **función CreateWindow** para crear un botón de inserción predeterminado.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions


Use la [**función CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para crear un control de botón.

En el siguiente ejemplo de C++, el *parámetro m \_ hwnd* es el identificador de la ventana primaria. El [**estilo \_ BS DEFPUSHBUTTON**](button-styles.md) especifica que se debe crear un botón de inserción predeterminado. Tenga en cuenta que los valores de tamaño y posición deben especificarse porque el uso de **CW \_ USEDEFAULT** para un botón establece los valores en cero.


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

 

 