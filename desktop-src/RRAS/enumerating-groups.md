---
title: Enumerar grupos (RRAS)
description: En la tabla siguiente se resume una serie de pasos en una interacción entre un protocolo de enrutamiento y el administrador de grupos de multidifusión.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4df3731e8370a213636ea12ad2a9b072903908888eba6983909c01201c655ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101845"
---
# <a name="enumerating-groups"></a>Enumeración de grupos

En la tabla siguiente se resume una serie de pasos en una interacción entre un protocolo de enrutamiento y el administrador de grupos de multidifusión. En la primera columna se describen las acciones que realiza el protocolo de enrutamiento y las respuestas del protocolo de enrutamiento al administrador de grupos de multidifusión. En la segunda columna se describen las respuestas del administrador de grupos de multidifusión al protocolo de enrutamiento. La tercera columna presenta cualquier información adicional.

Cada fila de la tabla representa un paso.



| Acción del protocolo de enrutamiento                                                                                                                                                    | Acción del administrador de grupos de multidifusión                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Obtenga un identificador para una enumeración mediante la [**función MgmGroupEnumerationStart.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)                                                         | Devuelve un identificador.                                                                                                                                                                                                                                                                                             |
| Obtenga uno o varios grupos mediante la [**función MgmGroupEnumerationGetNext.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)                                                             | Devuelve tantos grupos como quepa en el búfer proporcionado por el cliente. Si no se puede devolver ningún grupo en el búfer proporcionado, devuelva ERROR INSUFFICIENT BUFFER y el tamaño del búfer necesario \_ \_ para devolver un grupo.<br/> Devuelve EL ERROR \_ NO HAY MÁS ELEMENTOS cuando no hay más \_ \_ grupos.<br/> |
| Si se recibe ERROR INSUFFICIENT BUFFER, llame de nuevo a la función \_ \_ [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) con un búfer del tamaño indicado. |                                                                                                                                                                                                                                                                                                              |
| Siga llamando a [**la función MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) hasta que se reciba ERROR \_ NO MORE \_ \_ ITEMS.                                   |                                                                                                                                                                                                                                                                                                              |
| Finalice el proceso de enumeración mediante [**la función MgmGroupEnumerationEnd.**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)                                                                   | Destruya el identificador.                                                                                                                                                                                                                                                                                          |



 

 

 





