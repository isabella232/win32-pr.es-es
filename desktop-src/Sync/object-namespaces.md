---
description: Un espacio de nombres de objeto protege los objetos con nombre frente al acceso no autorizado.
ms.assetid: 6a84ec16-fa65-4cdd-861a-eccf5d0eee2b
title: Espacios de nombres de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6137d53e45f27a8de2c76075bc2a5565a5942bd38bf6fa3cd3891e4561870b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117765492"
---
# <a name="object-namespaces"></a>Espacios de nombres de objeto

Un *espacio de nombres de* objeto protege los objetos con nombre frente al acceso no autorizado. La creación de un espacio de nombres privado permite a las aplicaciones y servicios crear un entorno más seguro.

Un proceso puede crear un espacio de nombres privado mediante [**la función CreatePrivateNamespace.**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) Esta función requiere que especifique un *límite que* defina cómo se van a aislar los objetos del espacio de nombres. El autor de la llamada debe estar dentro del límite especificado para que la operación de creación se realiza correctamente. Para especificar un límite, use las [**funciones CreateBoundaryDescriptor**](/windows/desktop/api/WinBase/nf-winbase-createboundarydescriptora) [**y AddSIDToBoundaryDescriptor.**](/windows/win32/api/namespaceapi/nf-namespaceapi-addsidtoboundarydescriptor)

El *parámetro lpAliasPrefix* [**de CreatePrivateNamespace**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) actúa como nombre del espacio de nombres. Cada espacio de nombres se identifica de forma única por su nombre y límites. El sistema admite varios espacios de nombres privados con el mismo nombre, siempre que especifiquen límites diferentes.

Supongamos que un proceso solicita la creación de un espacio de nombres, NS1, que define un límite que contiene dos elementos: el SID de administrador y el número de sesión actual. El espacio de nombres se crea si el proceso se ejecuta en la cuenta de administrador de la sesión especificada. Otro proceso puede acceder a este espacio de nombres mediante [**la función OpenPrivateNamespace.**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) El nombre y el límite especificados deben coincidir si este proceso va a abrir el espacio de nombres creado por el primer proceso. Tenga en cuenta que un proceso puede abrir un espacio de nombres existente aunque no esté dentro del límite a menos que el creador haya restringido el acceso al espacio de nombres mediante el parámetro *lpPrivateNamespaceAttributes.*

Los objetos que se crean en este espacio de nombres tienen nombres que tienen el formato *prefijo* \\ *objectname*. El prefijo es el nombre del espacio de nombres especificado por *el parámetro lpAliasPrefix* [**de CreatePrivateNamespace.**](/windows/desktop/api/WinBase/nf-winbase-createprivatenamespacea) Por ejemplo, para crear un objeto de evento denominado MyEvent en el espacio de nombres NS1, llame a la [**función CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) con el parámetro *lpName* establecido en NS1 \\ MyEvent.

El proceso que creó el espacio de nombres puede usar [**la función ClosePrivateNamespace**](/windows/win32/api/namespaceapi/nf-namespaceapi-closeprivatenamespace) para cerrar el identificador del espacio de nombres. El identificador también se cierra cuando finaliza el proceso que creó el espacio de nombres. Una vez cerrado el identificador del espacio de nombres, se producirá un error en las llamadas posteriores a [**OpenPrivateNamespace,**](/windows/desktop/api/WinBase/nf-winbase-openprivatenamespacea) pero todas las operaciones en los objetos del espacio de nombres se realizarán correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Espacios de nombres de objeto kernel](../termserv/kernel-object-namespaces.md)
</dt> </dl>

 

 
