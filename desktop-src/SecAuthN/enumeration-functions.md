---
description: Si el proveedor de red necesita admitir la exploración de sus recursos de red, debe implementar las siguientes funciones. MPR llama a estas funciones para enumerar los recursos.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Funciones de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2670424be1540aad3e46e32c5b0606eb02e04bdc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271452"
---
# <a name="enumeration-functions"></a>Funciones de enumeración

Si el proveedor de red necesita admitir la exploración de sus recursos de red, debe implementar las siguientes funciones. MPR llama a estas funciones para enumerar los recursos.

No se requiere un proveedor de red para implementar ninguna de las funciones de enumeración. Sin embargo, si un proveedor de red implementa [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)o [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), también debe implementar las otras dos funciones de enumeración.



| Función                                                     | Descripción                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | Abre una enumeración de recursos de red o conexiones existentes.                                                                                                  |
| [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | Realiza una enumeración en un identificador devuelto por [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).                                                                                   |
| [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | Cierra una enumeración.                                                                                                                                              |
| [**NPGetResourceInformation**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | Determina si el proveedor es el proveedor correcto para responder a una solicitud de un recurso de red especificado y devuelve información sobre el tipo del recurso. |
| [**NPGetResourceParent**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | Devuelve el elemento primario de un recurso de red especificado en la jerarquía de exploración.                                                                                         |



 

 

 



