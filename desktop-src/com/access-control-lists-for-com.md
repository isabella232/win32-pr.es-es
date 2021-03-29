---
title: Access Control listas para COM
description: Access Control listas para COM
ms.assetid: ceb37563-7e7f-4704-b671-72ed65e3e102
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811b6cdbca36ef75bb5ee3f185b0261967d736d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774797"
---
# <a name="access-control-lists-for-com"></a>Access Control listas para COM

Windows Server XP Service Pack 2 (SP 2) y Windows Server 2003 Service Pack 1 (SP 1) presentan mejoras de seguridad para el modelo de objetos componentes distribuido (DCOM). Una de estas mejoras son derechos de acceso más específicos para su uso en las listas de control de acceso (ACL). Los derechos de acceso son:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Para proporcionar compatibilidad con versiones anteriores, puede existir una ACL en el formato usado antes de Windows XP SP 2 y Windows Server 2003 SP 1. que usa solo los derechos de acceso de COM correctos para la \_ \_ ejecución, o puede existir en el nuevo formato usado en Windows XP SP 2 y windows Server 2003 SP 1, que usa los \_ derechos com \_ ejecutarse junto con una combinación de \_ derechos COM \_ ejecutar \_ local, \_ derechos com \_ ejecutar \_ remoto, \_ derechos com \_ activar \_ local y \_ derechos com \_ activar \_ remoto.

> [!Note]  
> \_Los derechos com \_ Execute siempre deben estar presentes; la ausencia de este derecho genera un descriptor de seguridad no válido.

 

No debe mezclar el formato antiguo y el nuevo formato en una sola ACL; todas las entradas de control de acceso (ACE) deben conceder solo el derecho de acceso de permisos de COM \_ \_ , o todos deben conceder derechos de com ejecutarse \_ \_ junto con una combinación de \_ derechos COM \_ ejecutar \_ local, \_ derechos com \_ ejecutar \_ remoto, derechos de com \_ \_ activar \_ local y derechos de com \_ \_ activar \_ remoto.

A continuación se presenta un ejemplo de una ACL con formato incorrecto:

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

Tenga en cuenta que la primera entrada de control de acceso (ACE) \_ solo concede derechos com \_ Execute (0x1), mientras que la segunda ACE concede \_ derechos com \_ Execute, \_ los derechos com se \_ EJECUTAn \_ localmente y \_ los derechos com se \_ activan en \_ local (0xb), y el tercero concede \_ derechos com \_ Execute y com \_ Rights \_ Activate \_ local (0x9).

Para corregirlo, la primera ACE debe cambiarse para que los \_ derechos \_ de com se ejecuten en combinación con uno de los otros cuatro derechos de acceso, o bien se debe cambiar la segunda y tercera ACE para conceder solo los \_ derechos com \_ Execute.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejoras de seguridad de DCOM en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[Seguridad en COM](security-in-com.md)
</dt> </dl>

 

 




