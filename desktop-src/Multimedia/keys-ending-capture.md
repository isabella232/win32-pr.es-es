---
title: Captura final de claves
description: Captura final de claves
ms.assetid: 932ed4ee-0928-41f7-a242-8b7435313647
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup macro
- Estructura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a91d6ee7d07ed36c11cce7e888c9a9710f403cf9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246159"
---
# <a name="keys-ending-capture"></a>Captura final de claves

Puede permitir que el usuario anule una sesión de captura presionando una combinación de teclas o pulsaciones desde el teclado o presionando el botón derecho o izquierdo del mouse. Si el usuario anula una sesión de captura en tiempo real, se descarta el contenido del archivo de captura. Si el usuario anula una sesión de captura de fotogramas paso a paso, se guarda el contenido del archivo de captura hasta el punto de anular la captura.

Puede recuperar la configuración para anular una sesión de captura mediante el mensaje [**\_ GET SEQUENCE \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) La configuración de pulsación de tecla actual se almacena en el **miembro vKeyAbort** de la [**estructura CAPTUREPARMS;**](/windows/win32/api/vfw/ns-vfw-captureparms) la configuración actual del mouse se almacena en los **miembros fAbortLeftMouse** **y fAbortRightMouse.** Puede establecer una nueva combinación de teclas o pulsaciones de tecla especificando la combinación de código de clave o código de clave (como en una combinación de teclas CTRL o MAYÚS) como el valor de **vKeyAbort** o establecer el botón primario o derecho del mouse como clave de anulación especificando el miembro **fAbortLeftMouse** o **fAbortRightMouse.** Después de establecer estos miembros, envíe la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje [**SET SEQUENCE SETUP \_ \_ \_ \_ de WM CAP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) El valor predeterminado de **vKeyAbort** es ESCAPE de \_ VK. Debe llamar a la [función RegisterHotKey antes](/windows/win32/api/winuser/nf-winuser-registerhotkey) de especificar una pulsación de tecla que pueda anular una sesión de captura. Los valores predeterminados de **fAbortLeftMouse** y **fAbortRightMouse** son **TRUE.**

 

 