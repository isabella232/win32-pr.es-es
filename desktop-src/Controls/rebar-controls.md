---
title: Acerca de los controles rebar
description: Un control rebar actúa como contenedor de las ventanas secundarias.
ms.assetid: vs|controls|~\controls\rebar\rebar.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56bc68629db7387f4ba408a769f7d87a64256000
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078475"
---
# <a name="about-rebar-controls"></a>Acerca de los controles rebar

Un *control rebar* actúa como contenedor de las ventanas secundarias. Puede contener una o más *bandas*, y cada banda puede tener cualquier combinación de una barra de agarre, un mapa de bits, una etiqueta de texto y una ventana secundaria. Una aplicación asigna una ventana secundaria (normalmente otro control) a una banda de control rebar. A medida que cambia dinámicamente la posición de una banda de control rebar, el control rebar administra el tamaño y la posición de la ventana secundaria asignada a esa banda. Además, una aplicación puede especificar un mapa de bits de fondo para una banda, y el control rebar mostrará la ventana secundaria de la banda sobre el mapa de bits.

En la captura de pantalla siguiente se muestra un control rebar que tiene dos bandas. Una contiene una barra de herramientas y la otra contiene un ComboBox. Ambas bandas tienen un agarrador que permite que se muevan y cambien de tamaño.

![captura de pantalla del cuadro de diálogo que muestra un control rebar con una banda que contiene una barra de herramientas y una banda que contiene un cuadro combinado](images/rb-rebar.png)

> [!Note]  
> El control rebar se implementa en la versión 4,70 y versiones posteriores de Comctl32.dll.

 

## <a name="rebar-bands-and-child-windows"></a>Bandas rebar y ventanas secundarias

Una aplicación define los rasgos de una banda rebar mediante los mensajes [**RB \_ INSERTBAND**](rb-insertband.md) y [**RB \_ SETBANDINFO**](rb-setbandinfo.md) . Estos mensajes aceptan la dirección de una estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) como el parámetro *lParam* . Los miembros de la estructura **REBARBANDINFO** definen los rasgos de una banda determinada. Para establecer los rasgos de una banda, establezca el miembro **cbsize** para indicar el tamaño de la estructura, en bytes. A continuación, establezca el miembro **fMask** para indicar qué miembros de estructura está rellenando la aplicación.

Para asignar una ventana secundaria a una banda, incluya la \_ marca secundaria RBBIM en el miembro **fMask** de la estructura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) y, a continuación, establezca el miembro **hwndChild** en el identificador de la ventana secundaria. Las aplicaciones pueden establecer el ancho y el alto mínimos permitidos de una ventana secundaria en los miembros **cxMinChild** y **cyMinChild** .

Cuando se destruye un control rebar, destruye todas las ventanas secundarias asignadas a las bandas que contiene. Para evitar que el control destruya las ventanas secundarias asignadas a sus bandas, elimine las bandas mediante el envío del mensaje de [**\_ DELETEBAND de RB**](rb-deleteband.md) y, a continuación, [**use el mensaje de este \_**](rb-setparent.md) elemento para restablecer el elemento primario a otra ventana antes de destruir el control rebar.

## <a name="the-rebar-control-user-interface"></a>Interfaz de usuario del control rebar

Se puede cambiar el tamaño de todas las bandas de control rebar, excepto las que usan el \_ estilo RBBS FIXEDSIZE. Para cambiar el tamaño o el orden de las bandas dentro del control, haga clic y arrastre la barra de redimensionamiento de una banda. El control rebar cambia automáticamente el tamaño y la posición de las ventanas secundarias asignadas a sus bandas. Además, puede alternar el tamaño de una banda haciendo clic en el texto de la banda, si existe.

## <a name="the-rebar-controls-image-list"></a>La lista de imágenes del control rebar

Si una aplicación usa una lista de imágenes con un control rebar, debe enviar el mensaje [**RB \_ SETBARINFO**](rb-setbarinfo.md) antes de agregar bandas al control. Este mensaje acepta la dirección de una estructura [**REBARINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarinfo) como el parámetro *lParam* . Antes de enviar el mensaje, prepare la estructura **REBARINFO** estableciendo el miembro **cbSize** en el tamaño de la estructura, en bytes. Después, si el control rebar va a mostrar imágenes en las bandas, establezca el miembro **fMask** en la marca RBIM \_ ImageList y asigne un identificador de lista de imágenes al miembro **himl** . Si el rebar no va a usar imágenes de banda, establezca **fMask** en cero.

## <a name="rebar-control-message-forwarding"></a>Reenvío de mensajes del control rebar

Un control rebar reenvía todos los mensajes de la ventana de [**\_ notificación de WM**](wm-notify.md) a su ventana primaria. Además, un control rebar reenvía todos los mensajes que se le envíen desde Windows asignados a sus bandas, como [**WM \_ CHARTOITEM**](wm-chartoitem.md), [**\_ comando de WM**](/windows/desktop/menurc/wm-command)y otros.

 

 