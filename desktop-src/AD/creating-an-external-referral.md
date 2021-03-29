---
title: Crear una referencia externa
description: Si se crea un objeto crossRef externo y un controlador de dominio lo utiliza para generar una referencia, el objeto crossRef proporciona dos elementos de datos importantes en las siguientes propiedades.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- referencias externas Active Directory
- Active Directory ejemplos Active Directory, crear una referencia externa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789592"
---
# <a name="creating-an-external-referral"></a>Crear una referencia externa

Si se crea un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) externo y un controlador de dominio lo utiliza para generar una referencia, el objeto **crossRef** proporciona dos elementos de datos importantes en las siguientes propiedades. Para obtener más información sobre las situaciones en las que esto puede ocurrir, consulte la sección anterior.



| Propiedad                           | Descripción                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Especifica el servidor o dominio que puede servir a los datos del contexto de nomenclatura especificado en [**NCName**](/windows/desktop/ADSchema/a-ncname).                                           |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | Especifica el nombre distintivo del dominio, el esquema o el contenedor de configuración con raíz en el servidor o dominio especificado por [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot). |



 

Por ejemplo, si el servidor con la dirección DNS de serv1.Northwest.fabrikam.com atiende el contexto de nomenclatura cuya raíz es CN =, ou = MyDOM, O = Fabrikam, establezca [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) en la dirección DNS de ese servidor y el [**NCName**](/windows/desktop/ADSchema/a-ncname) en el nombre distintivo del dominio, el esquema o el contenedor de configuración.

Para obtener más información y un ejemplo de código que muestra cómo crear una referencia externa, vea [código de ejemplo para crear un objeto crossRef externo](example-code-for-creating-an-external-crossref-object.md).

 

 