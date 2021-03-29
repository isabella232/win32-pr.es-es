---
title: Cómo procesar la notificación de DTN_WMKEYDOWN
description: En este tema se muestra cómo procesar una \_ notificación de WMKEYDOWN de DTN. El control de este código de notificación permite que el propietario del control proporcione respuestas específicas a las pulsaciones de teclas dentro de los campos de devolución de llamada del control.
ms.assetid: CD521C62-CF52-4FFF-A598-E5EBA34471FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec97ffc5853743c357081b974d155ee0e0977d1
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103904912"
---
# <a name="how-to-process-the-dtn_wmkeydown-notification"></a>Cómo procesar la notificación de \_ WMKEYDOWN de DTN

En este tema se muestra cómo procesar una notificación de [ \_ WMKEYDOWN de DTN](dtn-wmkeydown.md) . El control de este código de notificación permite que el propietario del control proporcione respuestas específicas a las pulsaciones de teclas dentro de los campos de devolución de llamada del control.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones


Los controles de selector de fecha y hora (DTP) envían el mensaje [ \_ WMKEYDOWN de DTN](dtn-wmkeydown.md) para informar de que el usuario ha escrito entradas en un campo de devolución de llamada. Si desea emular las mismas respuestas del teclado que se admiten para los campos de DTP estándar o proporcionar respuestas personalizadas, la aplicación debe incluir código para controlar esta notificación.

El siguiente ejemplo de código C++ es una función definida por la aplicación que procesa la notificación [ \_ WMKEYDOWN de DTN](dtn-wmkeydown.md) .

**Advertencia de seguridad:** El uso incorrecto de **lstrcmp** puede poner en peligro la seguridad de la aplicación. Por ejemplo, antes de llamar a **lstrcmp** en el ejemplo de código siguiente, debe asegurarse de que las dos cadenas terminan en NULL. Debe revisar las [consideraciones de seguridad: controles de Microsoft Windows](sec-comctls.md) antes de continuar.



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

[Usar controles de selector de fecha y hora](using-date-and-time-picker.md)
</dt> <dt>

[Referencia de control de selector de fecha y hora](bumper-date-and-time-picker-date-and-time-picker-control-reference.md)
</dt> <dt>

[Selector de fecha y hora](date-and-time-picker-control-reference.md)
</dt> </dl>

 

 




