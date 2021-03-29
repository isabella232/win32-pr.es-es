---
title: Enumerar grupos (RRAS)
description: En la tabla siguiente se resume una serie de pasos en una interacción entre un protocolo de enrutamiento y el administrador del grupo de multidifusión.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3860c6876ed6ea5caef4941efcdd949eb9890d
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104487182"
---
# <a name="enumerating-groups"></a>Enumerar grupos

En la tabla siguiente se resume una serie de pasos en una interacción entre un protocolo de enrutamiento y el administrador del grupo de multidifusión. En la primera columna se describen las acciones que realiza el protocolo de enrutamiento y las respuestas del Protocolo de enrutamiento al administrador del grupo de multidifusión. En la segunda columna se describen las respuestas del administrador del grupo de multidifusión al Protocolo de enrutamiento. La tercera columna presenta cualquier información adicional.

Cada fila de la tabla representa un paso.



| Acción del Protocolo de enrutamiento                                                                                                                                                    | Acción del administrador del grupo de multidifusión                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtener un identificador para una enumeración mediante la función [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) .                                                         | Devuelve un identificador.                                                                                                                                                                                                                                                                                             |
| Obtener uno o varios grupos mediante la función [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) .                                                             | Devuelva tantos grupos como quepan en el búfer proporcionado por el cliente. Si no se puede devolver ningún grupo en el búfer proporcionado, \_ se devuelve \_ un error de búfer insuficiente y el tamaño del búfer necesario para devolver un grupo.<br/> Devuelve el ERROR \_ no hay \_ más \_ elementos cuando no hay más grupos.<br/> |
| Si \_ \_ se recibe un error de búfer insuficiente, vuelva a llamar a la función [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) con un búfer con el tamaño indicado. |                                                                                                                                                                                                                                                                                                              |
| Continúe llamando a la función [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) hasta \_ que \_ no \_ se reciba ningún elemento más.                                   |                                                                                                                                                                                                                                                                                                              |
| Finalice el proceso de enumeración mediante la función [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) .                                                                   | Destruya el identificador.                                                                                                                                                                                                                                                                                          |



 

 

 





