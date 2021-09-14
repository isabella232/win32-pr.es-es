---
title: Cómo procesar la notificación DTN_WMKEYDOWN aplicación
description: En este tema se muestra cómo procesar una notificación \_ WMKEYDOWN de DTN. El control de este código de notificación permite al propietario del control proporcionar respuestas específicas a las pulsaciones de tecla dentro de los campos de devolución de llamada del control.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167630"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>Cómo procesar la notificación \_ WMKEYDOWN de DTN

En este tema se muestra cómo procesar una [notificación \_ WMKEYDOWN de DTN.](dtn-wmkeydown.md) El control de este código de notificación permite al propietario del control proporcionar respuestas específicas a las pulsaciones de tecla dentro de los campos de devolución de llamada del control.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instrucciones


Los controles de selector de fecha y hora (DTP) envían el mensaje [ \_ WMKEYDOWN](dtn-wmkeydown.md) de DTN para informar de que el usuario ha especificado la entrada en un campo de devolución de llamada. Si desea emular las mismas respuestas de teclado que se admiten para los campos DTP estándar o proporcionar respuestas personalizadas, la aplicación debe incluir código para controlar esta notificación.

El siguiente ejemplo de código de C++ es una función definida por la aplicación que procesa la [notificación \_ WMKEYDOWN de DTN.](dtn-wmkeydown.md)

**Advertencia de seguridad:** El **uso incorrecto de lstrcmp** puede poner en peligro la seguridad de la aplicación. Por ejemplo, antes de llamar **a lstrcmp** en el ejemplo de código siguiente, debe asegurarse de que las dos cadenas terminan en NULL. Debe revisar [Consideraciones de seguridad: Microsoft Windows antes](sec-comctls.md) de continuar.



```C++
//  DoWMKeydown increments or decrements the day of month according 
//  to user keyboard input.

void WINAPI DoWMKeydown(
 HWND hwndDP,
 LPNMDATETIMEWMKEYDOWN lpDTKeystroke)
{
    int delta =1;
    if(!lstrcmp(lpDTKeystroke->pszFormat,L"XX")){
        switch(lpDTKeystroke->nVirtKey){
            case VK_DOWN:
            case VK_SUBTRACT:
                delta = -1;  // fall through

            case VK_UP:
            case VK_ADD:
                lpDTKeystroke->st.wDay += (WORD) delta;
                break;
        }
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles selectores de fecha y hora](using-date-and-time-picker.md)
</dt> <dt>

[Referencia del control Selector de fecha y hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




