---
description: Un administrador de confianza es la cuenta de usuario, la cuenta de grupo o la sesión de inicio de sesión a la que se aplica una entrada de control de acceso (ACE). Cada ACE de una lista de control de acceso (ACL) tiene un identificador de seguridad (SID) que identifica a un administrador de confianza.
ms.assetid: 1c34faa0-936a-433a-9280-a94033f3f815
title: Confianza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90084a0b6bfc7f63db12b7f47eba335adc87239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279475"
---
# <a name="trustees"></a>Confianza

Un administrador de confianza es la cuenta de usuario, la cuenta de grupo o la [*sesión de inicio*](/windows/desktop/SecGloss/l-gly) de sesión a la que se aplica una entrada de [*control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE). Cada ACE de una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) tiene un [*identificador de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que identifica a un administrador de confianza.

Las cuentas de usuario incluyen cuentas que los usuarios o programas humanos, como los servicios de Windows, usan para iniciar sesión en el equipo local.

Las cuentas de grupo no se pueden usar para iniciar sesión en un equipo, pero son útiles en las ACE para permitir o denegar un conjunto de derechos de acceso a una o varias cuentas de usuario.

Un [*SID de inicio de sesión*](/windows/desktop/SecGloss/l-gly) que identifica la sesión de inicio de sesión actual es útil para permitir o denegar los derechos de acceso solo hasta que el usuario cierre la sesión.

Las funciones de control de acceso usan la estructura de [**confianza**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) para identificar a un administrador de confianza. La estructura de **confianza** le permite utilizar una cadena de nombre o un SID para identificar un administrador de confianza. Si utiliza un nombre, las funciones que crean una ACE a partir de la estructura de **confianza** realizan la tarea de asignación de los búferes de SID y la búsqueda del SID que corresponde al nombre de la cuenta. Hay dos funciones auxiliares, [**BuildTrusteeWithSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithsida) y [**BuildTrusteeWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithnamea), que inicializan una estructura de **confianza** con un SID o un nombre especificados. [**BuildTrusteeWithObjectsAndSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandsida) y [**BuildTrusteeWithObjectsAndName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandnamea) permiten inicializar una estructura de **confianza** con información de ACE específica del objeto. Otras tres funciones auxiliares, [**GetTrusteeForm**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteeforma), [**GetTrusteeName**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteenamea)y [**GetTrusteeType**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteetypea), recuperan los valores de los distintos miembros de una estructura de **confianza** .

El miembro **ptstrName** de la estructura [**Trustee**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) puede ser un puntero a los [**objetos \_ , \_ el nombre**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) , los objetos y la estructura de [**\_ \_ SID**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) . Estas estructuras especifican información sobre una [ACE específica del objeto](object-specific-aces.md) además de un nombre de administrador de confianza o SID. Esto permite que funciones como [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) y [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) almacenen información de ACE específica del objeto en el miembro de **confianza** de la estructura de [**\_ acceso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) .

 

 
