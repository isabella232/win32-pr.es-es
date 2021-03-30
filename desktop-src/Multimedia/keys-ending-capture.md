---
title: Captura de claves finalizando
description: Captura de claves finalizando
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Estructura CAPTUREPARMS
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a91d6ee7d07ed36c11cce7e888c9a9710f403cf9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789987"
---
# <a name="keys-ending-capture"></a>Captura de claves finalizando

Puede permitir que el usuario anule una sesión de captura presionando una tecla o combinación de teclas del teclado, o presionando el botón primario o secundario del mouse. Si el usuario anula una sesión de captura en tiempo real, se descarta el contenido del archivo de captura. Si el usuario anula una sesión de captura de fotogramas de paso, se guarda el contenido del archivo de captura hasta el punto de anulación de la captura.

Puede recuperar la configuración para anular una sesión de captura mediante el mensaje de configuración de la secuencia de obtención de Cap de WM (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). [**\_ \_ \_ \_**](wm-cap-get-sequence-setup.md) La configuración de la pulsación de tecla actual se almacena en el miembro **vKeyAbort** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . la configuración actual del mouse se almacena en los miembros **fAbortLeftMouse** y **fAbortRightMouse** . Puede establecer una nueva combinación de teclas o pulsaciones de tecla especificando la combinación KeyCode o KeyCode (como en una combinación de teclas CTRL o Mayús) como el valor de **vKeyAbort**, o bien establecer el botón primario o secundario del mouse como la clave de anulación especificando el miembro **fAbortLeftMouse** o **fAbortRightMouse** . Después de establecer estos miembros, envíe la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje de configuración de la secuencia de definición de [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Cap de [**WM \_ \_ \_ \_**](wm-cap-set-sequence-setup.md) (o la macro capCaptureSetSetup). El valor predeterminado de **vKeyAbort** es VK \_ escape. Debe llamar a la función [RegisterHotKey](/windows/win32/api/winuser/nf-winuser-registerhotkey) antes de especificar una pulsación de tecla que puede anular una sesión de captura. Los valores predeterminados de **fAbortLeftMouse** y **fAbortRightMouse** son **true**.

 

 