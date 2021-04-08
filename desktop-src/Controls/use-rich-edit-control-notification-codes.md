---
title: Cómo usar los códigos de notificación de control Rich Edit
description: La ventana primaria de un control Rich Edit puede procesar los códigos de notificación para supervisar los eventos que afectan al control. Los controles Rich Edit admiten todos los códigos de notificación que se usan con controles de edición, así como varios otros.
ms.assetid: E045EADE-CB37-492A-85EC-6CF236677F08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68e510bf7c5abe6109862a01d8926c8956736f9
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/17/2020
ms.locfileid: "103995045"
---
# <a name="how-to-use-rich-edit-control-notification-codes"></a>Cómo usar los códigos de notificación de control Rich Edit

La ventana primaria de un control Rich Edit puede procesar los códigos de notificación para supervisar los eventos que afectan al control. Los controles Rich Edit admiten todos los códigos de notificación que se usan con controles de edición, así como varios otros.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows

## <a name="instructions"></a>Instrucciones

### <a name="use-a-rich-edit-control-notification-code"></a>Usar un código de notificación de control de edición enriquecido

Puede determinar los códigos de notificación que un control Rich Edit envía su ventana primaria mediante el establecimiento de su máscara de eventos. Para establecer la máscara de eventos para un control Rich Edit, utilice el mensaje de la [**\_ SETEVENTMASK em**](em-seteventmask.md) . Puede recuperar la máscara de eventos actual para un control Rich Edit mediante el mensaje [**\_ GetEventMask (EM**](em-geteventmask.md) . Para obtener una lista de marcas de máscara de eventos, vea [marcas de máscara de eventos de control de edición enriquecida](rich-edit-control-event-mask-flags.md).

La ventana primaria de un control Rich Edit puede filtrar todas las entradas del teclado y del mouse en el control procesando el código de notificación [en \_ MSGFILTER](en-msgfilter.md) . La ventana primaria puede impedir que se procese el mensaje del teclado o del mouse, o bien cambiar el mensaje modificando la estructura [**MSGFILTER**](/windows/desktop/api/Richedit/ns-richedit-msgfilter) especificada.

Una aplicación puede procesar el código de notificación [en \_ protegido](en-protected.md) para detectar cuándo el usuario intenta modificar texto protegido. Para marcar un intervalo de texto como protegido, puede establecer el efecto de carácter protegido.

Puede permitir que el usuario coloque archivos en un control Rich Edit procesando el código de notificación [en \_ DROPFILES](en-dropfiles.md) . La estructura [**ENDROPFILES**](/windows/desktop/api/Richedit/ns-richedit-endropfiles) especificada contiene información sobre los archivos que se van a quitar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar controles Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demostración de controles comunes de Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




