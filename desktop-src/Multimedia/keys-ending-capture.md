---
title: Captura de finalización de claves
description: Captura de finalización de claves
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup (macro)
- Estructura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5764f6b1853e1b161501f3c8df22ff0b7387649c517a28e7e36e7a094f35b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140055"
---
# <a name="keys-ending-capture"></a>Captura de finalización de claves

Puede permitir que el usuario anule una sesión de captura presionando una combinación de teclas o pulsaciones de tecla desde el teclado, o bien presionando el botón derecho o izquierdo del mouse. Si el usuario anula una sesión de captura en tiempo real, se descarta el contenido del archivo de captura. Si el usuario anula una sesión de captura de marco de pasos, se guarda el contenido del archivo de captura hasta el punto de anular la captura.

Puede recuperar la configuración para anular una sesión de captura mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) La configuración de pulsación de tecla actual se almacena en el **miembro vKeyAbort** de la [**estructura CAPTUREPARMS;**](/windows/win32/api/vfw/ns-vfw-captureparms) la configuración actual del mouse se almacena en los **miembros fAbortLeftMouse** **y fAbortRightMouse.** Puede establecer una nueva combinación de teclas o pulsaciones de teclas especificando la combinación de código de clave o código de teclado (como en una combinación de teclas CTRL o MAYÚS) como el valor de **vKeyAbort,** o bien establecer el botón primario o derecho del mouse como clave de anulación especificando el miembro **fAbortLeftMouse** o **fAbortRightMouse.** Después de establecer estos miembros, envíe la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje [**SET SEQUENCE SETUP \_ \_ \_ \_ de WM CAP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) El valor predeterminado de **vKeyAbort** es ESCAPE de \_ VK. Debe llamar a la [función RegisterHotKey antes](/windows/win32/api/winuser/nf-winuser-registerhotkey) de especificar una pulsación de tecla que pueda anular una sesión de captura. Los valores predeterminados de **fAbortLeftMouse** **y fAbortRightMouse** son **TRUE.**

 

 