---
description: El redireccionamiento de sesión permite a una aplicación desviar una sesión ofrecida a otra dirección sin responder a la llamada.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Redirect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ea44aaa10bc174784822032359d68d24ba01b6f7f1dcdf0fb211554107b8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761209"
---
# <a name="redirect"></a>Redirect

El redireccionamiento de sesión permite a una aplicación desviar una sesión ofrecida a otra dirección sin responder a la llamada. La aplicación puede realizar el redireccionamiento mediante llamada a llamada. Por ejemplo, una aplicación podría permitir que un usuario especifique diferentes redireccionamientos en función de la información del identificador de autor de la llamada. Una vez que se ha redirigido correctamente una llamada, el estado normalmente pasa a inactivo y se deben liberar los recursos asociados.

La redirección difiere de [hacia](forward-ovr.md) delante en que, una vez configurado el reenvío, TAPI, el proveedor de servicios o el conmutador realizan la operación sin intervención adicional de la aplicación. La redirección difiere de [la transferencia](transfer-ovr.md) en que la redirección no requiere responder primero a la llamada.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2.x:** Vea [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).

 

 
