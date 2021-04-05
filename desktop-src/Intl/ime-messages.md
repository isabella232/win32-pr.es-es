---
description: El sistema operativo envía mensajes de la ventana del IME al procedimiento de ventana de una aplicación cuando se producen determinados eventos que afectan a las ventanas del IME.
ms.assetid: 7eac1ab7-d04b-4e1b-9e2c-fa9a778756cd
title: Mensajes IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f30baa01081e0aca1423f3384926938e6fdc07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082192"
---
# <a name="ime-messages"></a>Mensajes IME

El sistema operativo envía mensajes de la ventana del IME al procedimiento de ventana de una aplicación cuando se producen determinados eventos que afectan a las ventanas del IME. Por ejemplo, el sistema operativo envía el mensaje de la aplicación del [**\_ \_ IME de WM**](wm-ime-setcontext.md) a la aplicación cuando se activa una ventana. Las aplicaciones que no reconocen IME pasan estos mensajes a la función [DefWindowProc](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , que los envía a la ventana IME predeterminada correspondiente. Las aplicaciones que tienen en cuenta el IME procesan estos mensajes o los reenvían a sus propias ventanas de IME.

La aplicación puede dirigir una ventana del IME para llevar a cabo un comando, por ejemplo, cambiar la posición de una ventana de composición mediante el mensaje de [**\_ \_ control de IME de WM**](wm-ime-control.md) . El IME notifica a la aplicación los cambios en la cadena de composición mediante el mensaje de [**\_ \_ composición del IME de WM**](wm-ime-composition.md) y los cambios generales en el estado de las ventanas del IME mediante el envío del mensaje de [**\_ \_ notificación del IME de WM**](wm-ime-notify.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
