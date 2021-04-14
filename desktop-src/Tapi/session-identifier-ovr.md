---
description: TAPI asigna identificadores de sesión únicos para cada sesión y aplicación.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificador de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424071"
---
# <a name="session-identifier"></a>Identificador de sesión

TAPI asigna identificadores de sesión únicos para cada sesión y aplicación. Una aplicación utiliza un identificador de sesión para comunicarse con TAPI en relación con una sesión específica. Normalmente, una aplicación obtiene un identificador mediante la creación de una nueva sesión de comunicaciones o cuando TAPI ofrece una sesión.

No se puede usar un identificador de sesión para pasar información a otra aplicación. Para este propósito, use el [identificador de llamada](call-id-ovr.md), que puede ser asignado por un proveedor de servicios.

Vea [iniciar una sesión](initiate-a-session-ovr.md) para obtener información sobre las operaciones que crean sesiones y devuelven un identificador de sesión. Vea [responder a una sesión iniciada en otro lugar](respond-to-session-initiated-elsewhere-ovr.md) para las operaciones que adquieren identificadores de sesión de TAPI. Vea [finalizar una sesión](terminate-a-session-ovr.md) para obtener información sobre la liberación de recursos de sesión.

Todos los proveedores de servicios deben admitir algún tipo de identificación de sesión.

**TAPI 2. x:** El identificador principal de una sesión de comunicaciones es el identificador de llamada.

**TAPI 3. x:** Una sesión se representa mediante un [objeto de llamada](call-object.md) y el identificador principal es un puntero a la interfaz [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

 

 



