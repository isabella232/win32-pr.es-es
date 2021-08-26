---
description: La clase de ventana IME es una clase global del sistema predefinida que define la apariencia y el comportamiento de las ventanas IME estándar.
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: Clase de ventana de IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56449534467a2b01ce8e59991bfc1c5f5ad4e1a9156f86cee5e154a8b8eb1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107195"
---
# <a name="ime-window-class"></a>Clase de ventana de IME

La clase de ventana IME es una clase global del sistema predefinida que define la apariencia y el comportamiento de las ventanas IME estándar. La clase es similar a las clases de control comunes en que la aplicación crea una ventana de esta clase mediante la [**función CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Al igual que los controles estáticos, una ventana de IME no responde a la entrada del usuario por sí misma. En su lugar, notifica al IME las acciones de entrada del usuario y procesa los mensajes de control que el IME o las aplicaciones le envían para llevar a cabo una respuesta a la acción del usuario.

Las aplicaciones con IME a veces crean ventanas IME personalizadas mediante la clase de ventana IME. El uso de la personalización de ventanas permite que la aplicación aproveche el procesamiento predeterminado de la ventana IME mientras tiene el control del posicionamiento de la ventana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
