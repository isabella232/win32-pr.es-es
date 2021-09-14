---
description: Un administrador de confianza es la cuenta de usuario, la cuenta de grupo o la sesión de inicio de sesión a la que se aplica una entrada de control de acceso (ACE). Cada ACE de una lista de control de acceso (ACL) tiene un identificador de seguridad (SID) que identifica a un administrador de confianza.
ms.assetid: 1c34faa0-936a-433a-9280-a94033f3f815
title: Administradores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90084a0b6bfc7f63db12b7f47eba335adc87239a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253653"
---
# <a name="trustees"></a>Administradores

Un administrador de confianza es la cuenta de usuario, la cuenta de grupo o la sesión [*de*](/windows/desktop/SecGloss/l-gly) inicio de sesión a la que se aplica una entrada de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE). Cada ACE de una [*lista de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACL) tiene un identificador de seguridad (SID) que identifica a un administrador de confianza. [](/windows/desktop/SecGloss/s-gly)

Las cuentas de usuario incluyen cuentas que usuarios humanos o programas como Windows Services usan para iniciar sesión en el equipo local.

Las cuentas de grupo no se pueden usar para iniciar sesión en un equipo, pero son útiles en las ACE para permitir o denegar un conjunto de derechos de acceso a una o varias cuentas de usuario.

Un [*SID de inicio de*](/windows/desktop/SecGloss/l-gly) sesión que identifica la sesión de inicio de sesión actual es útil para permitir o denegar derechos de acceso solo hasta que el usuario cierre la sesión.

Las funciones de control de acceso usan la [**estructura TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) para identificar a un administrador de confianza. La **estructura TRUSTEE** permite usar una cadena de nombre o un SID para identificar a un administrador de confianza. Si usa un nombre, las funciones que crean una ACE a partir de la estructura **TRUSTEE** realizan la tarea de asignar los búferes de SID y buscar el SID correspondiente al nombre de cuenta. Hay dos funciones auxiliares, [**BuildTrusteeWithSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithsida) y [**BuildTrusteeWithName,**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithnamea)que inicializan una estructura **TRUSTEE** con un SID o un nombre especificados. [**BuildTrusteeWithObjectsAndSid**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandsida) y [**BuildTrusteeWithObjectsAndName**](/windows/desktop/api/Aclapi/nf-aclapi-buildtrusteewithobjectsandnamea) permiten inicializar una estructura **TRUSTEE** con información ACE específica del objeto. Otras tres funciones auxiliares, [**GetTrusteeForm,**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteeforma) [**GetTrusteeName**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteenamea)y [**GetTrusteeType,**](/windows/desktop/api/Aclapi/nf-aclapi-gettrusteetypea)recuperan los valores de los distintos miembros de una **estructura TRUSTEE.**

El **miembro ptstrName** de la [**estructura TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) puede ser un puntero a una estructura OBJECTS AND [**\_ \_ NAME**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_name_a) u [**OBJECTS AND \_ \_ SID.**](/windows/desktop/api/AccCtrl/ns-accctrl-objects_and_sid) Estas estructuras especifican información sobre una [ACE específica del objeto](object-specific-aces.md) además de un nombre de administrador de confianza o SID. Esto permite que funciones como [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) y [**GetExplicitEntriesFromAcl**](/windows/desktop/api/Aclapi/nf-aclapi-getexplicitentriesfromacla) almacenen información ACE específica del objeto en el miembro **Trustee** de la [**estructura EXPLICIT \_ ACCESS.**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a)

 

 
