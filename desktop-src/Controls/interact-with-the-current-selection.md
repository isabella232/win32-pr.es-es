---
title: Cómo interactuar con la selección actual
description: El usuario puede seleccionar texto en un control de edición enriquecido mediante el mouse o el teclado.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a6e60ef0ba4aa9a8034256c8c272950f4983d16c0195737065563b378e14202
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434645"
---
# <a name="how-to-interact-with-the-current-selection"></a>Cómo interactuar con la selección actual

El usuario puede seleccionar texto en un control de edición enriquecido mediante el mouse o el teclado. La *selección actual* es el intervalo de caracteres seleccionados o la posición del punto de inserción si no se selecciona ningún carácter. Una aplicación puede obtener información sobre la selección actual, establecerla, determinar cuándo cambia y mostrar u ocultar el resaltado de selección.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="interact-with-the-current-selection"></a>Interacción con la selección actual

Para determinar la selección actual en un control de edición enriquecido, use el [**mensaje EM \_ EXGETSEL.**](em-exgetsel.md) Para establecer la selección actual, use el [**mensaje EM \_ EXSETSEL.**](em-exsetsel.md) La [**estructura CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) se usa con ambos mensajes y especifica un intervalo de caracteres. Para recuperar información sobre el contenido de la selección actual, puede usar el [**mensaje EM \_ SELECTIONTYPE.**](em-selectiontype.md)

Una aplicación puede detectar cuándo cambia la selección actual procesando el código [de \_ notificación EN SELCHANGE.](en-selchange.md) El código de notificación especifica una [**estructura SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que contiene información sobre la nueva selección. Un control de edición enriquecido envía este código de notificación solo si lo habilita mediante el mensaje [**\_ EM SETEVENTMASK.**](em-seteventmask.md)

De forma predeterminada, un control de edición enriquecido muestra y oculta el resaltado de selección cuando obtiene y pierde el foco. Puede mostrar u ocultar el resaltado de selección en cualquier momento mediante el mensaje [**EM \_ HIDESELECTION.**](em-hideselection.md) Por ejemplo, una aplicación podría proporcionar un cuadro de diálogo Buscar para buscar texto en un control de edición enriquecido. La aplicación podría seleccionar texto correspondiente sin cerrar el cuadro de diálogo, en cuyo caso debe usar el mensaje **EM \_ HIDESELECTION** para resaltar la selección.

Al igual que con los controles de edición, puede especificar el estilo de ventana [**ES \_ NOHIDESEL**](edit-control-styles.md) para evitar que un control de edición enriquecido oculte el resaltado de selección cuando pierde el foco.

Como alternativa al uso de los mensajes [**EM \_ EXGETSEL**](em-exgetsel.md) y [**EM \_ EXSETSEL,**](em-exsetsel.md) puede recuperar y establecer la selección actual mediante los mensajes de control de edición [**EM \_ GETSEL**](em-getsel.md) y [**EM \_ SETSEL.**](em-setsel.md) El **mensaje EM \_ GETSEL** empaqueta dos índices de caracteres de 16 bits en su valor devuelto de 32 bits y, por tanto, solo funciona para las selecciones que se encuentran completamente dentro de los primeros 64 K. Sin embargo, un control de edición enriquecido nunca contendrá más de 32 000 caracteres de texto, a menos que extienda este límite mediante el mensaje [**EM \_ LIMITTEXT**](em-limittext.md) o [**EM \_ EXLIMITTEXT.**](em-exlimittext.md) Para las selecciones que se extienden más allá de los primeros 64 KB de texto, el mensaje **EM \_ GETSEL** devuelve –1. En tal caso, puede seguir utilizando los valores que se devuelven en *wParam* y *lParam* para buscar los caracteres inicial y final de la selección.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles rich edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




