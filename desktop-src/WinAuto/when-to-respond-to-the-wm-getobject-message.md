---
title: Cuándo responder al mensaje WM_GETOBJECT mensaje
description: Si una aplicación admite Microsoft Active Accessibility o Automatización de la interfaz de usuario para un elemento de interfaz de usuario, la aplicación no debe responder al mensaje GETOBJECT de WM antes de que el objeto que representa el elemento de interfaz de usuario se inicialice por completo o después de que la aplicación haya empezado a \_ cerrarse.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdb12edde21b7906fdda91d1bc5d46e453696214b93a331e26034527e163a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114620"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a>Cuándo responder al mensaje \_ GETOBJECT de WM

Si una aplicación admite Microsoft Active Accessibility o Automatización de la interfaz de usuario para un elemento de interfaz de usuario, la aplicación no debe responder al mensaje [**\_ GETOBJECT**](wm-getobject.md) de WM antes de que el objeto que representa el elemento de interfaz de usuario se inicialice por completo o después de que la aplicación haya empezado a cerrarse. Cuando una aplicación crea una nueva ventana, el sistema genera el evento [**EVENT \_ OBJECT \_ CREATE**](event-constants.md) WinEvent para notificar a los clientes antes de enviar el [**mensaje WM \_ CREATE**](/windows/desktop/winmsg/wm-create) al procedimiento de ventana de la aplicación. Dado que muchas aplicaciones usan **WM \_ CREATE** para iniciar el proceso de inicialización, cualquier implementación de accesibilidad de un elemento de interfaz de usuario no responde al [**mensaje \_ GETOBJECT**](wm-getobject.md) de WM hasta que la aplicación haya terminado de procesar el **mensaje CREATE \_ de WM.**

 

 