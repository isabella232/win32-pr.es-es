---
description: Cuando se abre un identificador en un objeto , el identificador devuelto tiene alguna combinación de derechos de acceso al objeto.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Solicitud de derechos de acceso a un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a168a5c9aa97d95acb13cb1cfeb3e776ea1e7ae6e2e090df5c8395a4b61fabea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907545"
---
# <a name="requesting-access-rights-to-an-object"></a>Solicitud de derechos de acceso a un objeto

Cuando se abre un identificador en un objeto , el identificador devuelto tiene alguna combinación de derechos de acceso al objeto. Algunas funciones, como [**CreateSemaphore,**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)no requieren un conjunto específico de derechos de acceso solicitados. Estas funciones siempre intentan abrir el identificador para el acceso completo. Otras funciones, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y [**OpenProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)permiten especificar el conjunto de derechos de acceso que desea. Debe solicitar solo los derechos de acceso que necesita, en lugar de abrir un identificador para el acceso completo. Esto evita el uso del identificador de forma no intencionado y aumenta las posibilidades de que la solicitud de acceso se haga correctamente si la DACL del objeto solo permite un acceso limitado.

Use [derechos de acceso genéricos](generic-access-rights.md) para especificar el tipo de acceso necesario al abrir un identificador para un objeto . Esto suele ser más sencillo que especificar todos los derechos estándar y específicos correspondientes. Como alternativa, use la constante MAXIMUM ALLOWED para solicitar que el objeto se abra con todos los derechos de acceso válidos \_ para el autor de la llamada.

> [!Note]  
> La constante MAXIMUM \_ ALLOWED no se puede usar en una ACE.

 

Para obtener o establecer la SACL en el descriptor de seguridad de un [*objeto*](/windows/desktop/SecGloss/s-gly), solicite el derecho de acceso [ACCESS SYSTEM \_ \_ SECURITY](sacl-access-right.md) al abrir un identificador para el objeto.

 

 
