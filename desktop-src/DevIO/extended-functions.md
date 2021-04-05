---
description: Se puede llamar a algunas funciones de comunicaciones para un dispositivo mediante la función EscapeCommFunction.
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: Funciones extendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0e57c316b521cbc246e5f31dcfb683238e216e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080248"
---
# <a name="extended-functions"></a>Funciones extendidas

Se puede llamar a algunas funciones de comunicaciones para un dispositivo mediante la función [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) . Esta función envía un código para indicar al dispositivo que realice una función extendida. Por ejemplo, una aplicación puede suspender la transmisión de caracteres con el código SETBREAK y reanudar la transmisión con el código CLRBREAK. Estas operaciones concretas también se pueden iniciar llamando a las funciones [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) y [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) . **EscapeCommFunction** también se puede usar para implementar el control de módem manual. Por ejemplo, los códigos CLRDTR y SETDTR se pueden usar para implementar el control de flujo DTR manual (terminal de datos preparado). Tenga en cuenta, sin embargo, que se produce un error si un proceso usa **EscapeCommFunction** para manipular la línea DTR cuando el dispositivo se ha configurado para habilitar el protocolo de enlace de DTR o la línea RTS (solicitud de envío) si está habilitado el protocolo de enlace RTS.

La función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) permite a un proceso enviar un código de función extendida directamente a un controlador de dispositivo especificado, lo que hace que el dispositivo realice una operación determinada. **DeviceIoControl** proporciona un dispositivo asociado a las capacidades de recursos de comunicaciones no admitidas por las funciones de comunicaciones serie estándar. Permite a una aplicación configurar un dispositivo con parámetros únicos para ese dispositivo, así como llamar a cualquier función específica del dispositivo.

 

 
