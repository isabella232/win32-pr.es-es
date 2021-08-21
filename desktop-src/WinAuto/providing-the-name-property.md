---
title: Proporcionar la propiedad Name
description: Los desarrolladores de servidores deben tener cuidado al crear controles predefinidos y comunes para asegurarse Microsoft Active Accessibility puedan exponer la propiedad Name del control.
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c93205430f3063b993c49a7145658d7748aac0e697257789c31ac0653d6189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052553"
---
# <a name="providing-the-name-property"></a>Proporcionar la propiedad Name

Los desarrolladores de servidores deben tener cuidado al crear controles predefinidos y comunes para asegurarse de que Microsoft Active Accessibility pueda exponer la [propiedad Name](name-property.md) del control. Según el tipo de control, el texto de la propiedad Name procede de uno de los siguientes elementos:

-   Texto de ventana del control (o título)
-   Texto estático que etiqueta el control

Para buscar el texto de la ventana del control, Microsoft Active Accessibility el mensaje [**\_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) de WM al control. Este texto corresponde al parámetro text de la instrucción de definición de recursos del control. Para algunos controles, como los botones, se trata del mismo texto que se muestra con el control . Para otros controles, como las barras de herramientas, este texto no se muestra. Por lo tanto, los desarrolladores de servidores deben proporcionar texto significativo en la instrucción de definición de recursos del control para ayudar a los usuarios de utilidades cliente a identificar el control.

Para buscar la etiqueta del control, Microsoft Active Accessibility un control de texto estático llamando a [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) con la marca \_ GW HWNDPREV. La búsqueda se detiene si se encuentra un control de texto estático o si se encuentra un control que tiene los estilos de ventana WS \_ GROUP \| WS \_ TABSTOP. Este orden de búsqueda corresponde al orden de tabulación inverso en un cuadro de diálogo. Los desarrolladores de servidores deben observar el orden de tabulación al crear controles para que un control de texto estático preceda inmediatamente al control que etiqueta.

Para obtener más información sobre las técnicas que Microsoft Active Accessibility para exponer la propiedad [Name](name-property.md), vea referencia [Interfaz de usuario elemento .](user-interface-element-reference.md)

 

 