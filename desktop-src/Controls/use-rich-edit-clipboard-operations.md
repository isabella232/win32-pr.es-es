---
title: Cómo usar las operaciones de edición enriquecida del portapapeles
description: Una aplicación puede pegar el contenido del portapapeles en un control Rich Edit mediante el mejor formato de Portapapeles disponible o un formato específico del portapapeles.
ms.assetid: 1FEFFD95-839B-4A26-A26E-B8429D5FF4C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a46432054956914b484c9faeeeda78f2a18e132
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995677"
---
# <a name="how-to-use-rich-edit-clipboard-operations"></a>Cómo usar las operaciones de edición enriquecida del portapapeles

Una aplicación puede pegar el contenido del portapapeles en un control Rich Edit mediante el mejor formato de Portapapeles disponible o un formato específico del portapapeles. También puede determinar si un control Rich Edit es capaz de pegar un formato de Portapapeles.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-a-rich-edit-clipboard-operation"></a>Usar una operación de edición enriquecida del portapapeles

Al igual que con un control de edición, puede copiar o cortar el contenido de la selección actual mediante el mensaje de [**\_ copia de WM**](/windows/desktop/dataxchg/wm-copy) o de [**\_ corte de WM**](/windows/desktop/dataxchg/wm-cut) . Del mismo modo, puede pegar el contenido del portapapeles en un control Rich Edit mediante el mensaje de [**\_ pegado de WM**](/windows/desktop/dataxchg/wm-paste) . El control pega el primer formato disponible que reconoce, lo que supuestamente es el formato más descriptivo.

Para pegar un formato específico del portapapeles, puede usar el mensaje de la [**\_ PASTESPECIAL em**](em-pastespecial.md) . Este mensaje es útil para las aplicaciones con un comando **Pegar especial** que permite al usuario seleccionar el formato del portapapeles. Puede usar el mensaje [**de \_ CANPASTE de EM**](em-canpaste.md) para determinar si el control reconoce un formato determinado.

También puede usar el mensaje de la [**\_ CANPASTE de EM**](em-canpaste.md) para determinar si un control Rich Edit reconoce cualquier formato de Portapapeles disponible. Este mensaje es útil cuando se procesa el mensaje de [**\_ INITMENUPOPUP de WM**](/windows/desktop/menurc/wm-initmenupopup) . Una aplicación podría habilitar o atenuar el comando **pegar** dependiendo de si el control puede pegar cualquier formato disponible.

Los controles Rich Edit registran dos formatos de portapapeles:

-   Formato de texto enriquecido
-   Formato de texto enriquecido sin objetos
-   Texto y objetos de RichEdit

Una aplicación puede registrar estos formatos mediante la función [**RegisterClipboardFormat**](/windows/desktop/api/winuser/nf-winuser-registerclipboardformata) , especificando los valores de CF \_ RTF, CF \_ RTFNOOBJS y CF \_ RETEXTOBJ.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 