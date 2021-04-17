---
description: Explica cómo cambiar los privilegios de un token mediante las funciones AdjustTokenPrivileges y CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Cambiar los privilegios de un token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8b77d966acf90db101269b77a767550bcae3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669670"
---
# <a name="changing-privileges-in-a-token"></a>Cambiar los privilegios de un token

Puede cambiar los privilegios en un token principal o de suplantación de dos maneras:

-   Habilitar o deshabilitar privilegios mediante la función [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .
-   Restrinja o quite privilegios mediante la función [**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) .

[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) no puede agregar ni quitar privilegios del token. Solo puede habilitar los privilegios existentes que están deshabilitados actualmente o deshabilitar los privilegios existentes que están habilitados actualmente. Para obtener ejemplos, vea [habilitar y deshabilitar privilegios en C++](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--).

Para asignar privilegios a una cuenta de usuario, consulte [asignación de privilegios a una cuenta](assigning-privileges-to-an-account.md).

[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) tiene funcionalidades más amplias, como se indica a continuación:

-   Quitar un privilegio. Tenga en cuenta que quitar un privilegio no es lo mismo que deshabilitar uno. Una vez que se quita un privilegio de un token, no se puede devolver.
-   Adjuntando el atributo de solo denegación a los SID en el token. Esto tiene el efecto de no permitir cuentas o grupos específicos, por ejemplo, denegar el acceso de eliminación del grupo todos a un archivo determinado. Para obtener más información sobre cómo restringir los SID, consulte [atributos de SID en un token de acceso](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token).
-   Especificación de una lista de los SID restrictivos en el token. Para obtener información acerca de cómo restringir los SID, consulte [tokens restringidos](/windows/desktop/SecAuthZ/restricted-tokens).

 

 
