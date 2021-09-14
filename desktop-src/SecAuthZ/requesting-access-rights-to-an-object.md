---
description: Cuando se abre un identificador para un objeto , el identificador devuelto tiene alguna combinación de derechos de acceso al objeto.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Solicitud de derechos de acceso a un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244094"
---
# <a name="requesting-access-rights-to-an-object"></a>Solicitud de derechos de acceso a un objeto

Cuando se abre un identificador para un objeto , el identificador devuelto tiene alguna combinación de derechos de acceso al objeto. Algunas funciones, como [**CreateSemaphore,**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)no requieren un conjunto específico de derechos de acceso solicitados. Estas funciones siempre intentan abrir el identificador para el acceso completo. Otras funciones, como [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y [**OpenProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)permiten especificar el conjunto de derechos de acceso que desea. Debe solicitar solo los derechos de acceso que necesita, en lugar de abrir un identificador para el acceso completo. Esto evita el uso del identificador de forma no intencionado y aumenta las posibilidades de que la solicitud de acceso se realizará correctamente si la DACL del objeto solo permite el acceso limitado.

Use [derechos de acceso genéricos](generic-access-rights.md) para especificar el tipo de acceso necesario al abrir un identificador para un objeto . Esto suele ser más sencillo que especificar todos los derechos estándar y específicos correspondientes. Como alternativa, use la constante MAXIMUM ALLOWED para solicitar que el objeto se abra con todos los derechos de acceso válidos \_ para el autor de la llamada.

> [!Note]  
> La constante MAXIMUM \_ ALLOWED no se puede usar en una ACE.

 

Para obtener o establecer la SACL en el [*descriptor*](/windows/desktop/SecGloss/s-gly)de seguridad de un objeto , solicite el acceso ACCESS [SYSTEM \_ \_ SECURITY](sacl-access-right.md) directamente al abrir un identificador para el objeto.

 

 
