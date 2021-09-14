---
description: El redireccionamiento de sesión permite a una aplicación desviar una sesión ofrecida a otra dirección sin responder a la llamada.
ms.assetid: b52cd5c2-fdd6-4240-b07b-b22733a89d27
title: Redirect
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100ade9315c3b5e8e68c17bf34a0b6d54a9d9663
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068724"
---
# <a name="redirect"></a>Redirect

El redireccionamiento de sesión permite a una aplicación desviar una sesión ofrecida a otra dirección sin responder a la llamada. La aplicación puede realizar el redireccionamiento en función de la llamada por llamada. Por ejemplo, una aplicación podría permitir que un usuario especifique diferentes redireccionamientos en función de la información del identificador de autor de la llamada. Una vez que se ha redirigido correctamente una llamada, el estado normalmente pasa a inactivo y se deben liberar los recursos asociados.

La redirección [](forward-ovr.md) difiere de hacia delante en que, una vez configurado el reenvío, tapi, el proveedor de servicios o el conmutador realizan la operación sin intervención adicional de la aplicación. La redirección difiere de [la transferencia](transfer-ovr.md) en que el redireccionamiento no requiere responder primero a la llamada.

No todos los proveedores de servicios admiten el uso de esta operación.

**TAPI 2.x:** Vea [**lineRedirect**](/windows/win32/api/tapi/nf-tapi-lineredirect).

 

 
