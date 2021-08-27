---
description: Las ventanas de estado, composición y candidatos forman la interfaz de usuario del IME.
ms.assetid: a0e52743-f9be-4934-9469-71d3cb5a768a
title: Estado, composición y candidatos Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f5c385c14cd265630de77352e12e4c63bce806837462f3c9ab3c204940e66c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130115"
---
# <a name="status-composition-and-candidates-windows"></a>Estado, composición y candidatos Windows

Las ventanas de estado, composición y candidatos forman la interfaz de usuario del IME. La ventana de estado indica que el IME está abierto y proporciona al usuario los medios para establecer los modos de conversión. La ventana de composición aparece cuando el usuario escribe texto y, en función del modo de conversión, muestra el texto como especificado o muestra el texto convertido. La ventana candidatos aparece junto con la ventana de composición. Contiene una lista de "candidatos" (caracteres alternativos) para el carácter o los caracteres seleccionados en la ventana de composición. El usuario puede desplazarse por la lista de candidatos y seleccionar los caracteres deseados y, a continuación, volver a la ventana de composición. El usuario puede crear el texto deseado de esta manera hasta que la cadena de composición se haya finalizado y se cierre la ventana.

El IME envía los caracteres compuestos a la aplicación que tiene en cuenta IME en forma de mensajes [**WM \_ IME \_ CHAR**](wm-ime-char.md) o [**WM \_ IME \_ COMPOSITION**](wm-ime-composition.md)/GCS \_ RESULT. Si la aplicación no procesa estos mensajes, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) los traduce en uno o varios [**mensajes WM \_ CHAR.**](../inputdev/wm-char.md)

De forma predeterminada, el sistema operativo crea y administra automáticamente las ventanas de estado, composición y candidatos para los requisitos de entrada de texto. Para muchas aplicaciones, este procesamiento predeterminado es suficiente. Estas aplicaciones se basan completamente en el sistema operativo para la compatibilidad con IME y se dice que no son conscientes de IME porque no son conscientes de las muchas tareas que el sistema operativo lleva a cabo para administrar las ventanas de IME.

Por otro lado, una aplicación que tenga en cuenta IME participa en la creación y administración de ventanas de IME. Estas aplicaciones controlan la operación, la posición y la apariencia de las ventanas predeterminadas mediante el envío de mensajes a estas ventanas y la interceptación y procesamiento de mensajes desde las ventanas. En algunos casos, las aplicaciones crean sus propias ventanas IME y proporcionan un procesamiento completo para sus ventanas de estado, composición y candidatos personalizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 
