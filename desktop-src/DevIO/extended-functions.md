---
description: Se puede llamar a algunas funciones de comunicaciones para un dispositivo mediante la función EscapeCommFunction.
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: Funciones extendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913feb46f61777bcb07fda1639519c4ef04fcb4905075b1c67955a3e911b9d0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405340"
---
# <a name="extended-functions"></a>Funciones extendidas

Se puede llamar a algunas funciones de comunicaciones para un dispositivo mediante la [**función EscapeCommFunction.**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) Esta función envía un código para dirigir el dispositivo para realizar una función extendida. Por ejemplo, una aplicación puede suspender la transmisión de caracteres con el código SETBREAK y reanudar la transmisión con el código CLRBREAK. Estas operaciones concretas también se pueden iniciar llamando a las [**funciones SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) [**y ClearCommBreak.**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) **EscapeCommFunction también** se puede usar para implementar el control de módem manual. Por ejemplo, los códigos CLRDTR y SETDTR se pueden usar para implementar el control manual de flujo DTR (listo para terminal de datos). Sin embargo, tenga en cuenta que se produce un error si un proceso usa **EscapeCommFunction** para manipular la línea DTR cuando el dispositivo se ha configurado para habilitar el protocolo de enlace DTR, o la línea RTS (solicitud de envío) si el protocolo de enlace RTS está habilitado.

La [**función DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) permite a un proceso enviar un código de función extendido directamente a un controlador de dispositivo especificado, lo que hace que el dispositivo realice una operación determinada. **DeviceIoControl proporciona** un dispositivo asociado a funcionalidades de recursos de comunicaciones no compatibles con las funciones de comunicaciones serie estándar. Permite a una aplicación configurar un dispositivo mediante parámetros únicos para ese dispositivo, así como llamar a cualquier función específica del dispositivo.

 

 
