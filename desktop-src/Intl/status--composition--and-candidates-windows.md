---
description: Las ventanas de estado, composición y candidatos forman la interfaz de usuario del IME.
ms.assetid: a0e52743-f9be-4934-9469-71d3cb5a768a
title: Ventanas de estado, composición y candidatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b800def67299a464fd232a08a2bbff0a2a60a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279349"
---
# <a name="status-composition-and-candidates-windows"></a>Ventanas de estado, composición y candidatos

Las ventanas de estado, composición y candidatos forman la interfaz de usuario del IME. La ventana de estado indica que el IME está abierto y proporciona al usuario los medios para establecer los modos de conversión. La ventana composición aparece cuando el usuario escribe texto y, en función del modo de conversión, muestra el texto como especificado o muestra texto convertido. La ventana candidatos aparece junto con la ventana composición. Contiene una lista de "candidatos" (caracteres alternativos) para el carácter o los caracteres seleccionados en la ventana de composición. El usuario puede desplazarse por la lista de candidatos y seleccionar los caracteres deseados y, a continuación, volver a la ventana de composición. El usuario puede crear el texto deseado de esta manera hasta que finalice la cadena de composición y se cierre la ventana.

El IME envía los caracteres compuestos a la aplicación compatible con el IME en forma de mensajes de resultados/GCS de la composición del IME de [**WM \_ \_**](wm-ime-char.md) o de [**WM \_ \_ IME**](wm-ime-composition.md) \_ . Si la aplicación no procesa estos mensajes, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) los convierte en uno o varios mensajes de tipo [**\_ Char de WM**](../inputdev/wm-char.md) .

De forma predeterminada, el sistema operativo crea y administra automáticamente ventanas de estado, composición y candidatos para los requisitos de entrada de texto. Para muchas aplicaciones, este procesamiento predeterminado es suficiente. Estas aplicaciones confían por completo en el sistema operativo para la compatibilidad con IME y se dice que no son compatibles con el IME porque no son conscientes de las muchas tareas que el sistema operativo lleva a cabo para administrar las ventanas del IME.

Por otro lado, una aplicación compatible con IME participa en la creación y la administración de las ventanas de IME. Dichas aplicaciones controlan la operación, la posición y la apariencia de las ventanas predeterminadas mediante el envío de mensajes a estas ventanas y la interceptación y el procesamiento de los mensajes de las ventanas. En algunos casos, las aplicaciones crean sus propias ventanas de IME y proporcionan un procesamiento completo para sus ventanas de estado personalizado, composición y candidatos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
