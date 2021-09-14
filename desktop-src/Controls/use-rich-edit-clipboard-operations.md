---
title: Cómo usar las operaciones de edición enriquecte del Portapapeles
description: Una aplicación puede pegar el contenido del Portapapeles en un control de edición enriquecido mediante el mejor formato de portapapeles disponible o un formato específico del Portapapeles.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165406"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>Cómo usar las operaciones de edición enriquecte del Portapapeles

Una aplicación puede pegar el contenido del Portapapeles en un control de edición enriquecido mediante el mejor formato de portapapeles disponible o un formato específico del Portapapeles. También puede determinar si un control de edición enriquecido es capaz de pegar un formato del Portapapeles.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-a-rich-edit-clipboard-operation"></a>Usar una operación de edición enriquecte del Portapapeles

Al igual que con un control de edición, puede copiar o cortar el contenido de la selección actual mediante el mensaje [**WM \_ COPY**](/windows/desktop/dataxchg/wm-copy) o [**WM \_ CUT.**](/windows/desktop/dataxchg/wm-cut) De forma similar, puede pegar el contenido del Portapapeles en un control de edición enriquecido mediante el [**mensaje WM \_ PASTE.**](/windows/desktop/dataxchg/wm-paste) El control pega el primer formato disponible que reconoce, que presumiblemente es el formato más descriptivo.

Para pegar un formato específico del Portapapeles, puede usar el [**mensaje EM \_ PASTESPECIAL.**](em-pastespecial.md) Este mensaje es útil para las aplicaciones con un **comando Pegar** especial que permite al usuario seleccionar el formato del Portapapeles. Puede usar el mensaje [**EM \_ CANPASTE**](em-canpaste.md) para determinar si el control reconoce un formato determinado.

También puede usar el mensaje [**EM \_ CANPASTE**](em-canpaste.md) para determinar si un control de edición enriquecido reconoce algún formato de Portapapeles disponible. Este mensaje es útil al procesar el [**mensaje \_ WM INITMENUPOPUP.**](/windows/desktop/menurc/wm-initmenupopup) Una aplicación podría habilitar o atenuar su **comando Pegar** en función de si el control puede pegar cualquier formato disponible.

Los controles de edición enriquecciones registran dos formatos del Portapapeles:

-   Formato de texto enriquecido
-   Formato de texto enriquecido sin objetos
-   RichEdit Text and Objects

Una aplicación puede registrar estos formatos mediante la función [**RegisterClipboardFormat,**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) especificando los valores CF \_ RTF, CF \_ RTFNOOBJS y CF \_ RETEXTOBJ.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles rich edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 