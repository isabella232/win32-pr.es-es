---
title: Bloqueo de cuenta (proveedor LDAP)
description: Cuando se supera el número de intentos de inicio de sesión con errores, la cuenta de usuario se bloquea durante un período de tiempo especificado por el atributo lockoutDuration.
ms.assetid: bf86f6ac-8209-4306-8736-99ce53c93617
ms.tgt_platform: multiple
keywords:
- ADSI de bloqueo de cuenta (proveedor LDAP)
- ADSI de bloqueo de cuenta, proveedor LDAP
- ADSI del proveedor LDAP, ejemplos de administración de usuarios, bloqueo de cuentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b7a25943debfd08469ce9a28463c88159ded9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970407"
---
# <a name="account-lockout-ldap-provider"></a>Bloqueo de cuenta (proveedor LDAP)

Cuando se supera el número de intentos de inicio de sesión con errores, la cuenta de usuario se bloquea durante un período de tiempo especificado por [**el atributo lockoutDuration.**](/windows/desktop/ADSchema/a-lockoutduration) La propiedad [**IADsUser.IsAccountLocked**](iadsuser-property-methods.md) parece ser la propiedad que se va a usar para leer y modificar el estado de bloqueo de una cuenta de usuario, pero el proveedor ADSI LDAP no admite con precisión la **propiedad IsAccountLocked.** Para obtener y establecer datos de bloqueo de cuentas precisos, use el proveedor WinNT. Para obtener más información sobre el uso de **la propiedad IsAccountLocked** con el proveedor winNT, vea [Bloqueo de cuenta (proveedor de WinNT).](winnt-account-lockout.md)

 

 