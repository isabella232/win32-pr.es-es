---
title: Proporcionar la propiedad Name
description: Los desarrolladores de servidores deben tener cuidado al crear controles predefinidos y comunes para asegurarse de que Microsoft Active Accessibility puede exponer la propiedad de nombre del control.
ms.assetid: 2b4ec5ae-bda1-41e6-9387-6ee3cb6c3163
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d7a4c30c6bc228785a886d9a41717f8cdb8dda
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995351"
---
# <a name="providing-the-name-property"></a>Proporcionar la propiedad Name

Los desarrolladores de servidores deben tener cuidado al crear controles predefinidos y comunes para asegurarse de que Microsoft Active Accessibility puede exponer la [propiedad de nombre](name-property.md) del control. Dependiendo del tipo de control, el texto de la propiedad Name proviene de uno de los siguientes elementos:

-   Texto (o título) de la ventana del control
-   Texto estático que etiqueta el control

Para encontrar el texto de la ventana del control, Microsoft Active Accessibility envía el mensaje [**\_ GETTEXT de WM**](/windows/desktop/winmsg/wm-gettext) al control. Este texto corresponde al parámetro text de la instrucción de definición de recursos del control. En algunos controles, como los botones, este es el mismo texto que se muestra con el control. En el caso de otros controles, como las barras de herramientas, este texto no se muestra. Por lo tanto, los desarrolladores de servidores deben proporcionar texto significativo en la instrucción de definición de recursos del control para ayudar a los usuarios de las utilidades de cliente a identificar el control.

Para encontrar la etiqueta del control, Microsoft Active Accessibility busca un control de texto estático llamando a [**GetWindow**](/windows/desktop/api/winuser/nf-winuser-getwindow) con la \_ marca HWNDPREV de GW. La búsqueda se detiene si se encuentra un control de texto estático o si se encuentra un control con los estilos de ventana WS \_ Group \| WS \_ . Este orden de búsqueda corresponde al orden de tabulación inversa de un cuadro de diálogo. Los desarrolladores de servidores deben observar el orden de tabulación al crear controles para que un control de texto estático preceda inmediatamente al control que etiqueta.

Para obtener más información sobre las técnicas que Microsoft Active Accessibility usa para exponer la [propiedad Name](name-property.md), vea referencia de elementos de la [interfaz de usuario](user-interface-element-reference.md).

 

 