---
title: Acerca de los controles Rebar
description: Un control Rebar actúa como contenedor para las ventanas secundarias.
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bc68629db7387f4ba408a769f7d87a64256000
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167173"
---
# <a name="about-rebar-controls"></a>Acerca de los controles Rebar

Un *control Rebar* actúa como contenedor para las ventanas secundarias. Puede contener una o varias bandas y cada banda puede tener cualquier combinación de una barra de control, un mapa de bits, una etiqueta de texto y una ventana secundaria. Una aplicación asigna una ventana secundaria (normalmente otro control) a una banda de control rebar. A medida que cambia de posición dinámicamente una banda de control de rebar, el control rebar administra el tamaño y la posición de la ventana secundaria asignada a esa banda. Además, una aplicación puede especificar un mapa de bits de fondo para una banda y el control rebar mostrará la ventana secundaria de la banda sobre el mapa de bits.

En la siguiente captura de pantalla se muestra un control de barra de rebar que tiene dos bandas. Una contiene una barra de herramientas y la otra contiene un cuadro combinado. Ambas bandas tienen un control que permite moverlas y cambiar su tamaño.

![captura de pantalla del cuadro de diálogo que muestra un control de barra de rebar con una banda que contiene una barra de herramientas y una banda que contiene un cuadro combinado](images/rb-rebar.png)

> [!Note]  
> El control rebar se implementa en la versión 4.70 y posteriores de Comctl32.dll.

 

## <a name="rebar-bands-and-child-windows"></a>Bandas de rebar y grupos Windows

Una aplicación define los rasgos de una banda de rebar mediante los mensajes [**\_ INSERTBAND**](rb-insertband.md) y [**RB \_ SETBANDINFO de RB.**](rb-setbandinfo.md) Estos mensajes aceptan la dirección de una [**estructura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) como *parámetro lParam.* Los **miembros de la estructura REBARBANDINFO** definen los rasgos de una banda determinada. Para establecer los rasgos de una banda, establezca el **miembro cbsize** para indicar el tamaño de la estructura, en bytes. A continuación, **establezca el miembro fMask** para indicar qué miembros de estructura está rellenando la aplicación.

Para asignar una ventana secundaria a una banda, incluya la marca CHILD de RBBIM en el miembro fMask de la estructura \_ [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) y, a continuación, establezca el miembro **hwndChild** en el identificador de la ventana  secundaria. Las aplicaciones pueden establecer el ancho y alto mínimos permitidos de una ventana secundaria en los **miembros cxMinChild** **y cyMinChild.**

Cuando se destruye un control de rebar, destruye las ventanas secundarias asignadas a las bandas dentro de él. Para evitar que el control destruya las ventanas secundarias asignadas a sus bandas, quite las bandas mediante el envío del mensaje [**\_ DELETEBAND**](rb-deleteband.md) de RB y, a continuación, use el mensaje [**\_ SETPARENT**](rb-setparent.md) de RB para restablecer el elemento primario en otra ventana antes de destruir el control de barra de rebar.

## <a name="the-rebar-control-user-interface"></a>El control Rebar Interfaz de usuario

Se puede cambiar el tamaño de todas las bandas de control de rebar, excepto aquellas que usan el estilo \_ FIXEDSIZE de RBBS. Para cambiar el tamaño o el orden de las bandas dentro del control, haga clic y arrastre la barra de control de una banda. El control rebar cambia automáticamente el tamaño y cambia la posición de las ventanas secundarias asignadas a sus bandas. Además, puede alternar el tamaño de una banda haciendo clic en el texto de la banda, si existe.

## <a name="the-rebar-controls-image-list"></a>Lista de imágenes del control Rebar

Si una aplicación usa una lista de imágenes con un control rebar, debe enviar el mensaje [**\_ SETBARINFO**](rb-setbarinfo.md) de RB antes de agregar bandas al control. Este mensaje acepta la dirección de una [**estructura REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) como parámetro *lParam.* Antes de enviar el mensaje, prepare la **estructura REBARINFO** estableciendo el **miembro cbSize** en el tamaño de la estructura, en bytes. A continuación, si el control rebar va a mostrar imágenes en las bandas, establezca el miembro **fMask** en la marca IMAGELIST de RBIM y asigne un identificador de lista de imágenes al \_ **miembro himl.** Si la barra de rebar no usará imágenes de banda, establezca **fMask** en cero.

## <a name="rebar-control-message-forwarding"></a>Rebar Control Message Forwarding

Un control rebar reenvía todos los mensajes de la ventana [**\_ WM NOTIFY**](wm-notify.md) a su ventana primaria. Además, un control rebar reenvía los mensajes que se le envían desde ventanas asignadas a sus bandas, como [**WM \_ CHARTOITEM,**](wm-chartoitem.md) [**WM \_ COMMAND**](/windows/desktop/menurc/wm-command)y otros.

 

 