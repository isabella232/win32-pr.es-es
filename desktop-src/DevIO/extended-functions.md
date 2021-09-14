---
description: Se puede llamar a algunas funciones de comunicación para un dispositivo mediante la función EscapeCommFunction.
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: Funciones extendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0e57c316b521cbc246e5f31dcfb683238e216e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164373"
---
# <a name="extended-functions"></a>Funciones extendidas

Se puede llamar a algunas funciones de comunicación para un dispositivo mediante la [**función EscapeCommFunction.**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) Esta función envía un código para dirigir el dispositivo para realizar una función extendida. Por ejemplo, una aplicación puede suspender la transmisión de caracteres con el código SETBREAK y reanudar la transmisión con el código CLRBREAK. Estas operaciones concretas también se pueden iniciar mediante una llamada a las [**funciones SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) [**y ClearCommBreak.**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) **EscapeCommFunction** también se puede usar para implementar el control manual del módem. Por ejemplo, los códigos CLRDTR y SETDTR se pueden usar para implementar el control de flujo dtr manual (listo para terminal de datos). Sin embargo, tenga en cuenta que se produce un error si un proceso usa **EscapeCommFunction** para manipular la línea DTR cuando el dispositivo se ha configurado para habilitar el protocolo de enlace DTR, o la línea RTS (solicitud-envío) si el protocolo de enlace RTS está habilitado.

La [**función DeviceIoControl permite**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) que un proceso envíe un código de función extendido directamente a un controlador de dispositivo especificado, lo que hace que el dispositivo realice una operación determinada. **DeviceIoControl proporciona** un dispositivo asociado a funcionalidades de recursos de comunicaciones no compatibles con las funciones de comunicaciones serie estándar. Permite a una aplicación configurar un dispositivo mediante parámetros únicos para ese dispositivo, así como llamar a cualquier función específica del dispositivo.

 

 
