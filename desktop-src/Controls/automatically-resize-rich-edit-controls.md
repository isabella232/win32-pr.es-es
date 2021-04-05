---
title: Cómo cambiar automáticamente el tamaño de los controles Rich Edit
description: Una aplicación puede cambiar el tamaño de un control Rich Edit según sea necesario para que tenga siempre el mismo tamaño que su contenido.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078460"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>Cómo cambiar automáticamente el tamaño de los controles Rich Edit

Una aplicación puede cambiar el tamaño de un control Rich Edit según sea necesario para que tenga siempre el mismo tamaño que su contenido. Un control Rich Edit es compatible con esto, lo que *se denomina funcionalidad* sin límite mediante el envío de su ventana primaria a un código de notificación [en \_ REQUESTRESIZE](en-requestresize.md) cada vez que cambia el tamaño del contenido del control.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="automatically-resize-a-rich-edit-control"></a>Cambiar automáticamente el tamaño de un control Rich Edit

Al procesar el código de notificación [en \_ REQUESTRESIZE](en-requestresize.md) , una aplicación debe cambiar el tamaño del control a las dimensiones de la estructura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) especificada. Una aplicación también puede trasladar cualquier información que esté cerca del control para acomodar el cambio de alto del control. Para cambiar el tamaño del control, puede usar la función [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .

Puede forzar que un control Rich Edit con un control Rich-less envíe un código de notificación [en \_ REQUESTRESIZE](en-requestresize.md) mediante el mensaje [**\_ REQUESTRESIZE em**](em-requestresize.md) . Este mensaje puede ser útil al procesar el mensaje de [**\_ tamaño de WM**](/windows/desktop/winmsg/wm-size) .

## <a name="remarks"></a>Observaciones

Para recibir los códigos de notificación [en \_ REQUESTRESIZE](en-requestresize.md) , debe habilitar la notificación mediante el mensaje [em \_ SETEVENTMASK](em-seteventmask.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 