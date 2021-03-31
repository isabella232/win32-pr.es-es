---
title: Acerca de los controles de dirección IP
description: Un control de dirección de protocolo de Internet (IP) permite al usuario escribir una dirección IP en un formato fácil de entender.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb8cf39400c97d211d83b5496067fe6d4772e1e7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995660"
---
# <a name="about-ip-address-controls"></a>Acerca de los controles de dirección IP

Un control de dirección de protocolo de Internet (IP) permite al usuario escribir una dirección IP en un formato fácil de entender. Este control también permite a la aplicación obtener la dirección en formato numérico en lugar de en formato de texto.

-   [Acerca de los controles de dirección IP](#about-ip-address-controls)
-   [Crear un control de dirección IP](#creating-an-ip-address-control)
-   [¿Controla una dirección IP un control de edición?](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>Acerca de los controles de dirección IP

Windows Internet Explorer versión 4,0 introduce el control de dirección IP, un nuevo control similar a un control de edición que permite al usuario escribir una dirección numérica en formato de protocolo de Internet (IP). Este formato consta de campos de 4 3 dígitos. Cada campo se trata individualmente; los números de campo son de base cero y continúan de izquierda a derecha, como se muestra en esta ilustración.

![diagrama que muestra los valores de cada uno de los cuatro campos de un control de dirección IP](images/ipa-scrn.png)

El control solo permite escribir texto numérico en cada uno de los campos. Una vez especificados tres dígitos en un campo determinado, el foco de teclado se mueve automáticamente al siguiente campo. Si la aplicación no necesita llenar todo el campo, el usuario puede escribir menos de tres dígitos. Por ejemplo, si el campo solo debe contener el número veinte, escribir "21" y presionar la tecla llevará al usuario al siguiente campo.

El intervalo predeterminado para cada campo es de 0 a 255, pero la aplicación puede establecer el intervalo en cualquier valor entre esos límites con el mensaje [**IPM \_ SetRange**](ipm-setrange.md) .

> [!Note]  
> El control de direcciones IP se implementa en la versión 4,71 y versiones posteriores de Comctl32.dll.

 

## <a name="creating-an-ip-address-control"></a>Crear un control de dirección IP

Antes de crear un control de dirección IP, llame a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con la marca de **clases de \_ Internet \_ de ICC** establecida en el miembro **dwICC** de la estructura [**InitCommonControlsEx**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex) .

Utilice la función [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de dirección IP. El nombre de clase del control es [**WC \_ IPAddress**](common-control-window-classes.md), que se define en commctrl. h. No existe ningún estilo específico del control de direcciones IP; sin embargo, dado que se trata de un control secundario, use el estilo de [**WS \_ Child**](/windows/desktop/winmsg/window-styles) como mínimo.

## <a name="is-an-ip-address-control-an-edit-control"></a>¿Controla una dirección IP un control de edición?

Un control de dirección IP no es un control de edición y no responde a \_ los mensajes em. Sin embargo, enviará a la ventana propietaria las siguientes notificaciones de control de edición a través del mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) . Tenga en cuenta que el control de direcciones IP también enviará notificaciones de IPN privadas \_ a través del mensaje de [**\_ notificación de WM**](wm-notify.md) .



|                                   |                                                                                                                                                                                                         |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Notificación**                  | **Motivo de la notificación**                                                                                                                                                                             |
| [EN \_ SETFOCUS](en-setfocus.md)   | Se envía cuando el control de dirección IP obtiene el foco de teclado.                                                                                                                                              |
| [EN \_ KILLFOCUS](en-killfocus.md) | Se envía cuando el control de dirección IP pierde el foco de teclado.                                                                                                                                              |
| [EN \_ cambio](en-change.md)       | Se envía cuando cambia cualquier campo del control de dirección IP. Al igual que la notificación de [ \_ cambio de en](en-change.md) un control estándar de edición, esta notificación se recibe una vez actualizada la pantalla. |



 

 

 