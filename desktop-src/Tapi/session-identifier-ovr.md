---
description: TAPI asigna identificadores de sesión que son únicos para cada sesión y aplicación.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificador de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527706159328b3919e47c39bc5fb160615ed2c202d33c1ce39c711b6921235a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760787"
---
# <a name="session-identifier"></a>Identificador de sesión

TAPI asigna identificadores de sesión que son únicos para cada sesión y aplicación. Una aplicación usa un identificador de sesión para comunicarse con TAPI en relación con una sesión específica. Normalmente, una aplicación obtiene un identificador mediante la creación de una nueva sesión de comunicaciones o cuando TAPI ofrece una sesión.

No se puede usar un identificador de sesión para pasar información a otra aplicación. Para ello, use el identificador [de llamada](call-id-ovr.md), que puede asignar un proveedor de servicios.

Consulte [Inicio de una sesión para](initiate-a-session-ovr.md) obtener información sobre las operaciones que crean sesiones y devuelven un identificador de sesión. Consulte [Respuesta a la sesión iniciada en otro lugar para](respond-to-session-initiated-elsewhere-ovr.md) obtener información sobre las operaciones que adquieren identificadores de sesión de TAPI. Consulte [Terminate a Session (Finalizar una](terminate-a-session-ovr.md) sesión) para obtener información sobre cómo liberar recursos de sesión.

Todos los proveedores de servicios deben admitir algún tipo de identificación de sesión.

**TAPI 2.x:** El identificador principal de una sesión de comunicaciones es el identificador de llamada.

**TAPI 3.x:** Una sesión se representa mediante un [objeto Call y](call-object.md) el identificador principal es un puntero a la interfaz [**ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

 

 



