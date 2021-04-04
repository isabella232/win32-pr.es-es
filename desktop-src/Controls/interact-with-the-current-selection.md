---
title: Cómo interactuar con la selección actual
description: El usuario puede seleccionar texto en un control Rich Edit mediante el mouse o el teclado.
ms.assetid: A529792C-DFA7-4BE1-8607-5A1556B64626
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec776ab0c8e07bb61dcc0e12d13af46b17d094a
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103789358"
---
# <a name="how-to-interact-with-the-current-selection"></a>Cómo interactuar con la selección actual

El usuario puede seleccionar texto en un control Rich Edit mediante el mouse o el teclado. La *selección actual* es el intervalo de caracteres seleccionados o la posición del punto de inserción si no se selecciona ningún carácter. Una aplicación puede obtener información sobre la selección actual, establecerla, determinar cuándo cambia y mostrar u ocultar el resaltado de la selección.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="interact-with-the-current-selection"></a>Interactuar con la selección actual

Para determinar la selección actual en un control Rich Edit, utilice el [**mensaje \_ EXGETSEL em**](em-exgetsel.md) . Para establecer la selección actual, use el [**mensaje \_ EXSETSEL em**](em-exsetsel.md) . La estructura [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) se usa con ambos mensajes y especifica un intervalo de caracteres. Para recuperar información sobre el contenido de la selección actual, puede usar el mensaje [**\_ SELECTIONTYPE em**](em-selectiontype.md) .

Una aplicación puede detectar cuándo cambia la selección actual procesando el código de notificación [en \_ SELCHANGE](en-selchange.md) . El código de notificación especifica una estructura [**SELCHANGE**](/windows/desktop/api/Richedit/ns-richedit-selchange) que contiene información sobre la nueva selección. Un control Rich Edit envía este código de notificación solo si se habilita mediante el mensaje [**em \_ SETEVENTMASK**](em-seteventmask.md) .

De forma predeterminada, un control Rich Edit muestra y oculta el resaltado de la selección cuando gana y pierde el foco. Puede mostrar u ocultar el resaltado de la selección en cualquier momento mediante el mensaje de [**\_ HIDESELECTION em**](em-hideselection.md) . Por ejemplo, una aplicación podría proporcionar un cuadro de diálogo de búsqueda para buscar texto en un control Rich Edit. La aplicación podría seleccionar texto coincidente sin cerrar el cuadro de diálogo, en cuyo caso debe usar el mensaje de **\_ HIDESELECTION em** para resaltar la selección.

Al igual que con los controles de edición, puede especificar el estilo de ventana [**\_ NOHIDESEL es**](edit-control-styles.md) para evitar que un control Rich Edit oculte el resaltado de la selección cuando pierde el foco.

Como alternativa al uso de los [**mensajes \_ em EXGETSEL**](em-exgetsel.md) y [**em \_ EXSETSEL**](em-exsetsel.md) , puede recuperar y establecer la selección actual mediante los mensajes de control de edición [**em \_ GETSEL**](em-getsel.md) y [**em \_ SETSEL**](em-setsel.md) . El **carácter \_ GETSEL de EM** de paquetes de mensajes 2 16 bits indiza en el valor devuelto de 32 bits y, por lo tanto, solo funciona para las selecciones que se encuentran completamente dentro de los primeros 64 KB. Sin embargo, un control Rich Edit nunca contendrá más de 32 000 caracteres de texto, a menos que amplíe este límite mediante el mensaje [**em \_ LIMITTEXT**](em-limittext.md) o [**em \_ EXLIMITTEXT**](em-exlimittext.md) . En las selecciones que superen los primeros 64 KB de texto, el mensaje **\_ GETSEL em** devuelve – 1. En tal caso, puede seguir usando los valores que se devuelven en *wParam* e *lParam* para buscar los caracteres inicial y final de la selección.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




