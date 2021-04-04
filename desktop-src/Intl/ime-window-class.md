---
description: La clase de ventana IME es una clase global del sistema predefinida que define la apariencia y el comportamiento de las ventanas del IME estándar.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Clase de ventana IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910118"
---
# <a name="ime-window-class"></a>Clase de ventana IME

La clase de ventana IME es una clase global del sistema predefinida que define la apariencia y el comportamiento de las ventanas del IME estándar. La clase es similar a las clases de controles comunes en que la aplicación crea una ventana de esta clase mediante la función [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Al igual que los controles estáticos, una ventana del IME no responde a la entrada del usuario por sí sola. En su lugar, notifica al IME las acciones de entrada del usuario y procesa los mensajes de control enviados por el IME o las aplicaciones para llevar a cabo una respuesta a la acción del usuario.

A veces, las aplicaciones que reconocen el IME crean ventanas de IME personalizadas mediante la clase de ventana de IME. El uso de la personalización de ventanas permite a la aplicación aprovechar el procesamiento predeterminado de la ventana del IME mientras controla la posición de la ventana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
