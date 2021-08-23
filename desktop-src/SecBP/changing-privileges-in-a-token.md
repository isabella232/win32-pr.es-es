---
description: Explica cómo cambiar los privilegios de un token mediante las funciones AdjustTokenPrivileges y CreateRestrictedToken.
ms.assetid: b8e47d04-07c1-4d57-8209-6b0c397476e5
title: Cambio de privilegios en un token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c511ca66c5d4739057f5ea75cae589ee97e849f659002a612e7d22fd6be8eecb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622755"
---
# <a name="changing-privileges-in-a-token"></a>Cambio de privilegios en un token

Puede cambiar los privilegios en un token principal o en un token de suplantación de dos maneras:

-   Habilite o deshabilite los privilegios mediante [**la función AdjustTokenPrivileges.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges)
-   Restrinja o quite privilegios mediante [**la función CreateRestrictedToken.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken)

[**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) no puede agregar ni quitar privilegios del token. Solo puede habilitar los privilegios existentes que están deshabilitados actualmente o deshabilitar los privilegios existentes que están habilitados actualmente. Para obtener ejemplos, [vea Habilitación y deshabilitación de privilegios en C++.](/windows/desktop/SecAuthZ/enabling-and-disabling-privileges-in-c--)

Para asignar privilegios a una cuenta de usuario, consulte [Asignación de privilegios a una cuenta.](assigning-privileges-to-an-account.md)

[**CreateRestrictedToken**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createrestrictedtoken) tiene funcionalidades más amplias como se muestra a continuación:

-   Quitar un privilegio. Tenga en cuenta que quitar un privilegio no es lo mismo que deshabilitar uno. Después de quitar un privilegio de un token, no se puede devolver.
-   Adjuntar el atributo de solo denegación a los SID del token. Esto tiene el efecto de no permitir grupos o cuentas específicos, por ejemplo, denegar el acceso de eliminación del grupo Todos a un archivo determinado. Para obtener más información sobre cómo restringir los SID, vea [Atributos de SID en un token de acceso.](/windows/desktop/SecAuthZ/sid-attributes-in-an-access-token)
-   Especificación de una lista de SID restricting en el token. Para obtener información sobre cómo restringir los SID, vea [Tokens restringidos.](/windows/desktop/SecAuthZ/restricted-tokens)

 

 
