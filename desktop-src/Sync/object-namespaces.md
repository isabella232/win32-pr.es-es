---
description: Un espacio de nombres de objeto protege los objetos con nombre del acceso no autorizado.
ms.assetid: 6a84ec16-fa65-4cdd-861a-eccf5d0eee2b
title: Espacios de nombres de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3eed750bc91c128251cc66fd7f9ed167771150
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910029"
---
# <a name="object-namespaces"></a>Espacios de nombres de objetos

Un *espacio de nombres de objeto* protege los objetos con nombre del acceso no autorizado. La creación de un espacio de nombres privado permite a las aplicaciones y los servicios crear un entorno más seguro.

Un proceso puede crear un espacio de nombres privado mediante la función [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) . Esta función requiere que se especifique un *límite* que defina cómo se van a aislar los objetos del espacio de nombres. El autor de la llamada debe estar dentro del límite especificado para que la operación de creación se realice correctamente. Para especificar un límite, use las funciones [**CreateBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora) y [**AddSIDToBoundaryDescriptor**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor) .

El parámetro *lpAliasPrefix* de [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) sirve como nombre del espacio de nombres. Cada espacio de nombres se identifica de forma única mediante su nombre y sus límites. El sistema admite varios espacios de nombres privados con el mismo nombre, siempre y cuando especifiquen límites diferentes.

Supongamos que un proceso solicita la creación de un espacio de nombres, NS1, que define un límite que contiene dos elementos: el SID de administrador y el número de sesión actual. El espacio de nombres se crea si el proceso se ejecuta con la cuenta de administrador en la sesión especificada. Otro proceso puede tener acceso a este espacio de nombres mediante la función [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) . Tanto el nombre como el límite especificados deben coincidir si este proceso es para abrir el espacio de nombres creado por el primer proceso. Tenga en cuenta que un proceso puede abrir un espacio de nombres existente aunque no esté dentro del límite a menos que el creador restrinja el acceso al espacio de nombres mediante el parámetro *lpPrivateNamespaceAttributes* .

Los objetos que se crean en este espacio de nombres tienen nombres con el formato *prefijo* \\ *objectname*. El prefijo es el nombre del espacio de nombres especificado por el parámetro *lpAliasPrefix* de [**CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea). Por ejemplo, para crear un objeto de evento denominado onEvent en el espacio de nombres de NS1, llame a la función [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) con el parámetro *LPNAME* establecido en ns1 \\ onEvent.

El proceso que creó el espacio de nombres puede usar la función [**ClosePrivateNamespace**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace) para cerrar el identificador del espacio de nombres. El identificador también se cierra cuando finaliza el proceso que creó el espacio de nombres. Una vez cerrado el identificador del espacio de nombres, las llamadas subsiguientes a [**OpenPrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) generan un error, pero todas las operaciones en los objetos del espacio de nombres se realizan correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Espacios de nombres de objetos de kernel](../termserv/kernel-object-namespaces.md)
</dt> </dl>

 

 
