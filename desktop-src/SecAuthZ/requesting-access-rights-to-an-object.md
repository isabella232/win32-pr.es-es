---
description: Al abrir un identificador de un objeto, el identificador devuelto tiene una combinación de derechos de acceso al objeto.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Solicitar derechos de acceso a un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666665"
---
# <a name="requesting-access-rights-to-an-object"></a>Solicitar derechos de acceso a un objeto

Al abrir un identificador de un objeto, el identificador devuelto tiene una combinación de derechos de acceso al objeto. Algunas funciones, como [**createsemaphore (**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), no requieren un conjunto específico de derechos de acceso solicitados. Estas funciones siempre intentan abrir el identificador de acceso completo. Otras funciones, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), permiten especificar el conjunto de derechos de acceso que se desea. Debe solicitar solo los derechos de acceso que necesita, en lugar de abrir un identificador de acceso completo. Esto evita el uso del identificador de manera no intencionada y aumenta las posibilidades de que la solicitud de acceso se realice correctamente si la DACL del objeto solo permite el acceso limitado.

Use los [derechos de acceso genéricos](generic-access-rights.md) para especificar el tipo de acceso necesario al abrir un identificador de un objeto. Normalmente es más sencillo que especificar todos los derechos estándar y específicos correspondientes. También puede usar la constante MAXIMUM \_ allowed para solicitar que el objeto se abra con todos los derechos de acceso que son válidos para el autor de la llamada.

> [!Note]  
> \_No se puede usar la constante máxima permitida en una ACE.

 

Para obtener o establecer la SACL en el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)de un objeto, solicite el [derecho de acceso de \_ \_ seguridad del sistema de acceso](sacl-access-right.md) al abrir un identificador del objeto.

 

 
