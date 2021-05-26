---
title: Acerca de los controles de dirección IP
description: Un control de direcciones de Protocolo de Internet (IP) permite al usuario escribir una dirección IP en un formato fácil de entender.
ms.assetid: cf6a59fc-661c-420a-a67f-a42619946357
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6859bd31250d30bcf26d0c5fde37afeca8cc81bd
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424235"
---
# <a name="about-ip-address-controls"></a>Acerca de los controles de dirección IP

Un control de direcciones de Protocolo de Internet (IP) permite al usuario escribir una dirección IP en un formato fácil de entender. Este control también permite a la aplicación obtener la dirección en formato numérico en lugar de en formato de texto.

-   [Acerca de los controles de dirección IP](#about-ip-address-controls)
-   [Creación de un control de direcciones IP](#creating-an-ip-address-control)
-   [¿Un control de direcciones IP es un control de edición?](#is-an-ip-address-control-an-edit-control)

## <a name="about-ip-address-controls"></a>Acerca de los controles de dirección IP

Windows Internet Explorer Versión 4.0 presenta el control de dirección IP, un nuevo control similar a un control de edición que permite al usuario escribir una dirección numérica en formato de protocolo de Internet (IP). Este formato consta de cuatro campos de tres dígitos. Cada campo se trata individualmente; Los números de campo se basan en cero y proceden de izquierda a derecha, como se muestra en esta ilustración.

![diagrama que muestra valores en cada uno de los cuatro campos de un control de direcciones IP](images/ipa-scrn.png)

El control solo permite especificar texto numérico en cada uno de los campos. Una vez que se han escrito tres dígitos en un campo determinado, el foco del teclado se mueve automáticamente al campo siguiente. Si la aplicación no necesita rellenar todo el campo, el usuario puede escribir menos de tres dígitos. Por ejemplo, si el campo solo debe contener el número 21, escribir "21" y presionar la tecla llevará al usuario al siguiente campo.

El intervalo predeterminado para cada campo es de 0 a 255, pero la aplicación puede establecer el intervalo en cualquier valor entre esos límites con el mensaje [**\_ SETRANGE de IPM.**](ipm-setrange.md)

> [!Note]  
> El control de direcciones IP se implementa en la versión 4.71 y posteriores de Comctl32.dll.

 

## <a name="creating-an-ip-address-control"></a>Creación de un control de direcciones IP

Antes de crear un control de dirección IP, llame a [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) con la marca DE CLASES INTERNET **\_ \_ DE LA CLASE DE INTERNET DE LA QUE SE HA ESTABLECIDO** en el miembro **dwICC** de la estructura [**INITCOMMONCONTROLSEX.**](/windows/win32/api/commctrl/ns-commctrl-initcommoncontrolsex)

Use las [**funciones CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) para crear un control de dirección IP. El nombre de clase del control es [**WC \_ IPADDRESS**](common-control-window-classes.md), que se define en Commctrl.h. No existen estilos específicos del control de direcciones IP; sin embargo, dado que se trata de un control secundario, use el [**estilo \_ SECUNDARIO**](/windows/desktop/winmsg/window-styles) de WS como mínimo.

## <a name="is-an-ip-address-control-an-edit-control"></a>¿Un control de direcciones IP es un control de edición?

Un control de dirección IP no es un control de edición y no responderá a los mensajes \_ EM. Sin embargo, enviará a la ventana de propietario las siguientes notificaciones de control de edición a través del [**mensaje \_ WM COMMAND.**](/windows/desktop/menurc/wm-command) Tenga en cuenta que el control de direcciones IP también enviará notificaciones IPN \_ privadas a través del [**mensaje WM \_ NOTIFY.**](wm-notify.md)



|     Notificación                              |     Motivo de la notificación                                                                                                                                                                                                    |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [EN \_ SETFOCUS](en-setfocus.md)   | Se envía cuando el control de direcciones IP obtiene el foco del teclado.                                                                                                                                              |
| [EN \_ KILLFOCUS](en-killfocus.md) | Se envía cuando el control de direcciones IP pierde el foco del teclado.                                                                                                                                              |
| [CAMBIO \_ DE EN](en-change.md)       | Se envía cuando cambia cualquier campo del control de direcciones IP. Al igual [que la notificación EN \_ CHANGE](en-change.md) de un control de edición estándar, esta notificación se recibe una vez actualizada la pantalla. |



 

 

 