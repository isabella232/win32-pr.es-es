---
title: Cuándo responder al mensaje de WM_GETOBJECT
description: Si una aplicación admite Microsoft Active Accessibility o la automatización de la interfaz de usuario para un elemento de la interfaz de usuario, la aplicación no debe responder al mensaje de la GETOBJECT de WM \_ antes de que el objeto que representa el elemento de la interfaz de usuario esté completamente inicializado o después de que la aplicación haya empezado a cerrarse.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cfa8d6604a13e84ffa89bf1fcf93d5d13e66e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488138"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a>Cuándo responder al mensaje de la \_ GETOBJECT de WM

Si una aplicación admite Microsoft Active Accessibility o la automatización de la interfaz de usuario para un elemento de la interfaz de usuario, la aplicación no debe responder al mensaje de la [**\_ GETOBJECT de WM**](wm-getobject.md) antes de que el objeto que representa el elemento de la interfaz de usuario esté completamente inicializado o después de que la aplicación haya empezado a cerrarse. Cuando una aplicación crea una ventana nueva, el sistema genera el [**objeto de evento \_ \_ Create**](event-constants.md) WinEvent para notificar a los clientes antes de enviar el mensaje de [**\_ creación de WM**](/windows/desktop/winmsg/wm-create) al procedimiento de ventana de la aplicación. Dado que muchas aplicaciones usan **WM \_ Create** para iniciar el proceso de inicialización, cualquier implementación de accesibilidad de un elemento de la interfaz de usuario no responde al mensaje de la [**\_ GETOBJECT de WM**](wm-getobject.md) hasta que la aplicación haya finalizado el procesamiento del mensaje de **\_ creación de WM** .

 

 