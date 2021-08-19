---
description: El sistema operativo envía mensajes de ventana IME al procedimiento de ventana de una aplicación cuando se producen determinados eventos que afectan a las ventanas de IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Mensajes IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa34228f695a18187654707668067ac34562098b48aae185a8d66d777b6f507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949266"
---
# <a name="ime-messages"></a>Mensajes IME

El sistema operativo envía mensajes de ventana IME al procedimiento de ventana de una aplicación cuando se producen determinados eventos que afectan a las ventanas de IME. Por ejemplo, el sistema operativo envía el mensaje [**\_ \_ SETCONTEXT**](wm-ime-setcontext.md) de WM IME a la aplicación cuando se activa una ventana. Las aplicaciones que no son conscientes de IME pasan estos mensajes a la función [DefWindowProc,](/windows/desktop/api/winuser/nf-winuser-defwindowproca) que los envía a la ventana IME predeterminada correspondiente. Las aplicaciones que tienen en cuenta IME procesan estos mensajes o los reenvía a sus propias ventanas de IME.

La aplicación puede dirigir una ventana de IME para llevar a cabo un comando, por ejemplo, cambiar la posición de una ventana de composición mediante el mensaje [**\_ WM IME \_ CONTROL.**](wm-ime-control.md) El IME notifica a la aplicación los cambios en la cadena de composición mediante el mensaje [**WM \_ IME \_ COMPOSITION**](wm-ime-composition.md) y los cambios generales en el estado de las ventanas de IME mediante el envío del mensaje [**WM \_ IME \_ NOTIFY.**](wm-ime-notify.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
