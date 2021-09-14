---
title: Cómo cambiar automáticamente el tamaño de los controles Rich Edit
description: Una aplicación puede cambiar el tamaño de un control de edición enriquecido según sea necesario para que siempre sea del mismo tamaño que su contenido.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170153"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>Cómo cambiar automáticamente el tamaño de los controles Rich Edit

Una aplicación puede cambiar el tamaño de un control de edición enriquecido según sea necesario para que siempre sea del mismo tamaño que su contenido. Un control de edición  enriquecido admite esta funcionalidad denominada sin fondo mediante el envío de un código de notificación [EN \_ REQUESTRESIZE](en-requestresize.md) a su ventana primaria cada vez que cambia el tamaño del contenido del control.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación

## <a name="instructions"></a>Instrucciones

### <a name="automatically-resize-a-rich-edit-control"></a>Cambiar automáticamente el tamaño de un control Rich Edit

Al procesar el código de notificación [EN \_ REQUESTRESIZE,](en-requestresize.md) una aplicación debe cambiar el tamaño del control a las dimensiones de la estructura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) especificada. Una aplicación también puede mover cualquier información que esté cerca del control para dar cabida al cambio de altura del control. Para cambiar el tamaño del control, puede usar la [**función SetWindowPos.**](/windows/desktop/api/winuser/nf-winuser-setwindowpos)

Puede forzar un control de edición enriquecido sin fondo para enviar un código de notificación [EN \_ REQUESTRESIZE](en-requestresize.md) mediante el mensaje [**EM \_ REQUESTRESIZE.**](em-requestresize.md) Este mensaje puede ser útil al procesar el [**mensaje WM \_ SIZE.**](/windows/desktop/winmsg/wm-size)

## <a name="remarks"></a>Observaciones

Para recibir [los códigos de notificación EN \_ REQUESTRESIZE,](en-requestresize.md) debe habilitar la notificación mediante el mensaje [EM \_ SETEVENTMASK.](em-seteventmask.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Windows demostración de controles comunes (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 