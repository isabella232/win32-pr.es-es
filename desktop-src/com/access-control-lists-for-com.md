---
title: Access Control para COM
description: Access Control para COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811b6cdbca36ef75bb5ee3f185b0261967d736d0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369524"
---
# <a name="access-control-lists-for-com"></a>Access Control para COM

Windows Server XP Service Pack 2 (SP 2) y Windows Server 2003 Service Pack 1 (SP 1) presentan mejoras de seguridad para el modelo de objetos componentes distribuidos (DCOM). Una de estas mejoras son derechos de acceso más específicos para su uso en listas de control de acceso (ACL). Los derechos de acceso son:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Para proporcionar compatibilidad con versiones anteriores, puede existir una ACL en el formato usado antes de Windows XP SP 2 y Windows Server 2003 SP 1, que usa solo el derecho de acceso COM RIGHTS EXECUTE, o puede existir en el nuevo formato usado en Windows XP SP 2 y \_ Windows Server 2003 SP 1, que usa COM RIGHTS EXECUTE junto con una combinación de DERECHOS COM \_ \_ EXECUTE \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL y \_ COM RIGHTS ACTIVATE \_ \_ \_ \_ \_ \_ \_ \_ REMOTE.

> [!Note]  
> COM RIGHTS EXECUTE siempre debe estar presente; la ausencia \_ de este derecho genera un descriptor de seguridad no \_ válido.

 

No debe mezclar el formato anterior y el nuevo formato dentro de una sola ACL; Todas las entradas de control de acceso (ACE) solo deben conceder el derecho de acceso COM RIGHTS EXECUTE, o todas deben conceder DERECHOS COM EXECUTE junto con una combinación de DERECHOS \_ \_ COM EXECUTE \_ \_ \_ \_ \_ LOCAL, COM RIGHTS EXECUTE REMOTE, COM RIGHTS ACTIVATE LOCAL y \_ COM RIGHTS ACTIVATE \_ \_ \_ \_ \_ \_ \_ \_ REMOTE.

A continuación se muestra un ejemplo de una ACL con formato incorrecto:

``` syntax
Revision 1
Sbz1 0
Control 0x8004
    SE_DACL_PRESENT
    SE_SELF_RELATIVE
Owner: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
Group: S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
DACL:
    AclRevision 2
    Sbz1 0
    AclSize 128
    AceCount 4
    Sbz2 0
    Ace[0]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 36
        AccessMask 0x1
        S-1-5-21-1597522630-148096252-1166023319-500 (no name mapped)
    Ace[1]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0xb
        S-1-5-18 (Well Known Group: NT AUTHORITY\SYSTEM)
    Ace[2]
        AceType 0: ACCESS_ALLOWED_ACE_TYPE
        AceFlags 0
        AceSize 20
        AccessMask 0x9
        S-1-5-11 (Well Known Group: NT AUTHORITY\Authenticated Users)
SACL:
    (null)
```

Tenga en cuenta que la primera entrada de control de acceso (ACE) solo concede DERECHOS COM EXECUTE (0x1), mientras que la segunda ACE concede DERECHOS COM EXECUTE, COM RIGHTS EXECUTE LOCAL y COM RIGHTS ACTIVATE LOCAL (0xb) y la tercera concede DERECHOS COM EXECUTE y \_ \_ COM RIGHTS ACTIVATE \_ \_ \_ \_ LOCAL \_ \_ \_ \_ \_ \_ \_ \_ \_ (0x9).

Para corregirlo, se debe cambiar la primera ACE para conceder a COM RIGHTS EXECUTE en combinación con uno de los otros cuatro derechos de acceso; de lo contrario, el segundo y el tercer ASE deben cambiarse para conceder solo \_ \_ COM RIGHTS \_ \_ EXECUTE.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras de seguridad de DCOM en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




