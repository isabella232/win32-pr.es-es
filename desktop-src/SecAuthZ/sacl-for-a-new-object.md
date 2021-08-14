---
description: SACL para un nuevo objeto
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL para un nuevo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f9833fcfb45a612b6135579e44aca6f219661fd2aeb2998b899e5794fa7bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413845"
---
# <a name="sacl-for-a-new-object"></a>SACL para un nuevo objeto

El sistema usa el algoritmo siguiente para crear una SACL para la mayoría de los tipos de nuevos objetos protegibles:

1.  La SACL del objeto es la SACL del descriptor de [*seguridad*](/windows/desktop/SecGloss/s-gly) especificado por el creador del objeto. El sistema combina todas las ACE heredables en la SACL especificada, a menos que el bit SE SACL PROTECTED esté establecido en los bits de \_ control del descriptor de \_ seguridad. Las ACE de ATRIBUTO DE RECURSO DEL SISTEMA y las ACE de IDENTIFICADOR DE DIRECTIVA CON ÁMBITO DE SISTEMA de un objeto primario se combinarán en un nuevo objeto, incluso si se SE el bit \_ \_ PROTEGIDO de \_ \_ \_ \_ \_ \_ \_ SACL.
2.  Si el creador no especifica un descriptor de seguridad, el sistema compila la SACL del objeto a partir de ACE heredables.
3.  Si no hay ninguna SACL especificada o heredada, el objeto no tiene SACL.

Para especificar una SACL para un nuevo objeto, el creador del objeto debe tener habilitado el SE \_ SECURITY \_ NAME. [](privileges.md) Si la SACL especificada para un nuevo objeto solo contiene ACE de ATRIBUTO DE RECURSO DEL SISTEMA, no se requiere el privilegio SE \_ \_ SECURITY \_ \_ \_ NAME. El creador no necesita este privilegio si la SACL del objeto se crea a partir de ACE heredadas.

El sistema usa un algoritmo diferente para compilar una SACL para un nuevo Active Directory objeto . Para obtener más información, vea [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
