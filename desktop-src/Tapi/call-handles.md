---
description: Como se menciona en la introducción al identificador de sesión, un identificador de llamada es el medio por el que una aplicación TAPI 2,2 identifica una sesión de comunicaciones determinada.
ms.assetid: 5f6a7adf-c074-4bf6-9828-76604eb7609c
title: Identificadores de llamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacad5b73d9d22caa006b734acaf8b992203d7d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677450"
---
# <a name="call-handles"></a>Identificadores de llamada

Como se menciona en la introducción al [identificador de sesión](./session-identifier-ovr.md) , un identificador de llamada es el medio por el que una aplicación TAPI 2,2 identifica una sesión de comunicaciones determinada. Cuando una aplicación inicia una sesión, TAPI devuelve un identificador de llamada para su uso en operaciones o consultas adicionales. Cuando una aplicación recibe una notificación de una sesión entrante, TAPI también pasa un identificador de llamada.

Una vez finalizada una sesión y el estado de la sesión es inactivo, el identificador de llamada sigue siendo válido hasta que la aplicación Desasigne el identificador o se cierre la línea. Es posible que la aplicación cierre la línea o que reciba un mensaje de [**\_ cierre de línea**](line-close.md) . Si se cierra una línea, todos los identificadores de llamada a las llamadas en la línea dejan de ser válidos al instante.

Después de que una llamada revierta al estado de *inactividad* , la aplicación todavía podrá leer la estructura y el estado de la información de la llamada. Esto permite a las aplicaciones usar operaciones como [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) para recuperar información de llamadas con fines de registro.

Cuando la aplicación no tiene más uso para el identificador de una llamada inactiva, debe llamar a [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) para liberar memoria asignada por el sistema relacionada con la llamada. TAPI asigna memoria para cada llamada de cada aplicación que tenga un identificador a la llamada. Es probable que los proveedores de servicios asignen memoria para contener también información de llamadas. La desasignación del identificador de llamada de una aplicación permite que la biblioteca y el proveedor de servicios recuperen estos recursos de memoria. El identificador de una aplicación para una llamada se convierte en void después de una desasignación correcta.

La aplicación debe liberar la memoria relacionada con la llamada asignada para sus propios fines.

 

 
