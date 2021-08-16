---
title: Cómo usar los códigos de notificación del control Rich Edit
description: La ventana primaria de un control de edición enriquecido puede procesar códigos de notificación para supervisar los eventos que afectan al control. Los controles de edición enriquecciones admiten todos los códigos de notificación que se usan con los controles de edición, así como varios más.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6bc730c648e76137db480f14895d540a9142ae6a80ffa58533e38ef513653ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828646"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>Cómo usar los códigos de notificación del control Rich Edit

La ventana primaria de un control de edición enriquecido puede procesar códigos de notificación para supervisar los eventos que afectan al control. Los controles de edición enriquecciones admiten todos los códigos de notificación que se usan con los controles de edición, así como varios más.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instructions

### <a name="use-a-rich-edit-control-notification-code"></a>Usar un código de notificación de control rich edit

Puede determinar qué códigos de notificación envía un control de edición enriquecido a su ventana primaria estableciendo su máscara de eventos. Para establecer la máscara de eventos para un control de edición enriquecido, use el mensaje [**\_ EM SETEVENTMASK.**](em-seteventmask.md) Puede recuperar la máscara de evento actual para un control de edición enriquecido mediante el mensaje [**\_ EM GETEVENTMASK.**](em-geteventmask.md) Para obtener una lista de marcas de máscara de eventos, vea [Rich Edit Control Event Mask Flags](rich-edit-control-event-mask-flags.md).

La ventana primaria de un control rich edit puede filtrar todas las entradas de teclado y mouse en el control mediante el procesamiento del código [de notificación EN \_ MSGFILTER.](en-msgfilter.md) La ventana primaria puede impedir que se procese el mensaje del teclado o del mouse o puede cambiar el mensaje modificando la estructura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) especificada.

Una aplicación puede procesar el código [de notificación EN \_ PROTECTED](en-protected.md) para detectar cuándo el usuario intenta modificar el texto protegido. Para marcar un intervalo de texto como protegido, puede establecer el efecto de carácter protegido.

Puede permitir que el usuario coloque archivos en un control de edición enriquecido procesando el código de notificación [EN \_ DROPFILES.](en-dropfiles.md) La estructura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) especificada contiene información sobre los archivos que se van a descartar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




