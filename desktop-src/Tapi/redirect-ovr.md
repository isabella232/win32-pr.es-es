---
description: La redirección de la sesión permite que una aplicación desvíe una sesión ofrecida a otra dirección sin responder a la llamada.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Redirect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819435"
---
# <a name="redirect"></a>Redirect

La redirección de la sesión permite que una aplicación desvíe una sesión ofrecida a otra dirección sin responder a la llamada. La aplicación puede realizar la redirección en función de la llamada. Por ejemplo, una aplicación podría permitir a un usuario especificar redireccionamientos diferentes en función de la información del identificador del autor de la llamada. Una vez que se ha redirigido correctamente una llamada, el estado normalmente realiza la transición a los recursos inactivos y asociados.

La redirección es diferente de [reenviar](forward-ovr.md) en que, una vez que se ha configurado el reenvío, la operación la realiza TAPI, el proveedor de servicios o el conmutador sin necesidad de más implicación de la aplicación. La redirección es diferente de la [transferencia](transfer-ovr.md) en que la redirección no requiere responder primero a la llamada.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2. x:** Vea [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).

 

 
