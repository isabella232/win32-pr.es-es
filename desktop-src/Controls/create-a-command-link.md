---
title: Cómo crear un vínculo de comando
description: En este tema se describe una manera de crear un vínculo de comando.
ms.assetid: F342075B-2D3B-40E0-B657-E1C57EDC2E3A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c61888921f06e017ec1ea625730c3cc52de5ab364db22fc01fd021ce5629c63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920905"
---
# <a name="how-to-create-a-command-link"></a>Cómo crear un vínculo de comando

En este tema se describe una manera de crear un vínculo de comando.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Prerrequisitos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="step-1-create-an-instance-of-the-command-link-button"></a>Paso 1: Crear una instancia del botón de vínculo de comando.

En el siguiente ejemplo de código de C++, la constante de estilo [**BS \_ COMMANDLINK**](button-styles.md) especifica el botón como un botón de vínculo de comando.


```C++
HWND hwndCommandLink = CreateWindow(
    L"BUTTON",  // Predefined class; Unicode assumed
    L"",        // Text will be defined later
    WS_TABSTOP | WS_VISIBLE | WS_CHILD | BS_COMMANDLINK,  // Styles
    200,        // x position 
    10,         // y position 
    100,        // Button width
    100,        // Button height
    m_hwnd,     // Parent window
    NULL,       // No menu
    (HINSTANCE)GetWindowLongPtr(m_hwnd, GWLP_HINSTANCE), 
    NULL);      // Pointer not needed
```



### <a name="step-2-set-the-command-link-label-and-explanation-text"></a>Paso 2: Establecer la etiqueta del vínculo de comando y el texto de la explicación

Use la [**función SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para establecer la etiqueta del vínculo de comando y el texto complementario a través del mensaje [**\_ SETTEXT**](/windows/desktop/winmsg/wm-settext) de WM y el mensaje [**\_ SETNOTE de BCM,**](bcm-setnote.md) respectivamente.


```C++
SendMessage(hwndCommandLink, WM_SETTEXT, 0, (LPARAM)L"Command link");
SendMessage(hwndCommandLink, BCM_SETNOTE, 0, (LPARAM)L"with note");
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

 

 