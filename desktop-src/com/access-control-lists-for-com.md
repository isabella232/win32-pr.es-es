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
# <a name="access-control-lists-for-com"></a><span data-ttu-id="76491-103">Access Control listas para COM</span><span class="sxs-lookup"><span data-stu-id="76491-103">Access Control Lists for COM</span></span>

<span data-ttu-id="76491-104">Windows Server XP Service Pack 2 (SP 2) y Windows Server 2003 Service Pack 1 (SP 1) presentan mejoras de seguridad para el modelo de objetos componentes distribuido (DCOM).</span><span class="sxs-lookup"><span data-stu-id="76491-104">Windows Server XP Service Pack 2 (SP 2) and Windows Server 2003 Service Pack 1 (SP 1) introduce security enhancements for the Distributed Component Object Model (DCOM).</span></span> <span data-ttu-id="76491-105">Una de estas mejoras son derechos de acceso más específicos para su uso en las listas de control de acceso (ACL).</span><span class="sxs-lookup"><span data-stu-id="76491-105">One of these enhancements is more specific access rights for use in access control lists (ACLs).</span></span> <span data-ttu-id="76491-106">Los derechos de acceso son:</span><span class="sxs-lookup"><span data-stu-id="76491-106">The access rights are:</span></span>

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

<span data-ttu-id="76491-107">Para proporcionar compatibilidad con versiones anteriores, puede existir una ACL en el formato usado antes de Windows XP SP 2 y Windows Server 2003 SP 1. que usa solo los derechos de acceso de COM correctos para la \_ \_ ejecución, o puede existir en el nuevo formato usado en Windows XP SP 2 y windows Server 2003 SP 1, que usa los \_ derechos com \_ ejecutarse junto con una combinación de \_ derechos COM \_ ejecutar \_ local, \_ derechos com \_ ejecutar \_ remoto, \_ derechos com \_ activar \_ local y \_ derechos com \_ activar \_ remoto.</span><span class="sxs-lookup"><span data-stu-id="76491-107">To provide backward compatibility, an ACL may exist in the format used before Windows XP SP 2 and Windows Server 2003 SP 1, which uses only the access right COM\_RIGHTS\_EXECUTE, or it may exist in the new format used in Windows XP SP 2 and Windows Server 2003 SP 1, which uses COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

> [!Note]  
> <span data-ttu-id="76491-108">\_Los derechos com \_ Execute siempre deben estar presentes; la ausencia de este derecho genera un descriptor de seguridad no válido.</span><span class="sxs-lookup"><span data-stu-id="76491-108">COM\_RIGHTS\_EXECUTE must always be present; the absence of this right generates an invalid security descriptor.</span></span>

 

<span data-ttu-id="76491-109">No debe mezclar el formato antiguo y el nuevo formato en una sola ACL; todas las entradas de control de acceso (ACE) deben conceder solo el derecho de acceso de permisos de COM \_ \_ , o todos deben conceder derechos de com ejecutarse \_ \_ junto con una combinación de \_ derechos COM \_ ejecutar \_ local, \_ derechos com \_ ejecutar \_ remoto, derechos de com \_ \_ activar \_ local y derechos de com \_ \_ activar \_ remoto.</span><span class="sxs-lookup"><span data-stu-id="76491-109">You must not mix the old format and the new format within a single ACL; either all access control entries (ACEs) must grant only the COM\_RIGHTS\_EXECUTE access right, or they all must grant COM\_RIGHTS\_EXECUTE together with a combination of COM\_RIGHTS\_EXECUTE\_LOCAL, COM\_RIGHTS\_EXECUTE\_REMOTE, COM\_RIGHTS\_ACTIVATE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_REMOTE.</span></span>

<span data-ttu-id="76491-110">A continuación se presenta un ejemplo de una ACL con formato incorrecto:</span><span class="sxs-lookup"><span data-stu-id="76491-110">The following is an example of an incorrectly formatted ACL:</span></span>

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

<span data-ttu-id="76491-111">Tenga en cuenta que la primera entrada de control de acceso (ACE) \_ solo concede derechos com \_ Execute (0x1), mientras que la segunda ACE concede \_ derechos com \_ Execute, \_ los derechos com se \_ EJECUTAn \_ localmente y \_ los derechos com se \_ activan en \_ local (0xb), y el tercero concede \_ derechos com \_ Execute y com \_ Rights \_ Activate \_ local (0x9).</span><span class="sxs-lookup"><span data-stu-id="76491-111">Note that the first access control entry (ACE) grants COM\_RIGHTS\_EXECUTE (0x1) only, while the second ACE grants COM\_RIGHTS\_EXECUTE, COM\_RIGHTS\_EXECUTE\_LOCAL, and COM\_RIGHTS\_ACTIVATE\_LOCAL (0xb), and the third grants COM\_RIGHTS\_EXECUTE and COM\_RIGHTS\_ACTIVATE\_LOCAL (0x9).</span></span>

<span data-ttu-id="76491-112">Para corregirlo, la primera ACE debe cambiarse para que los \_ derechos \_ de com se ejecuten en combinación con uno de los otros cuatro derechos de acceso, o bien se debe cambiar la segunda y tercera ACE para conceder solo los \_ derechos com \_ Execute.</span><span class="sxs-lookup"><span data-stu-id="76491-112">To correct this, the first ACE should be changed to grant COM\_RIGHTS\_EXECUTE in combination with one of the other four access rights, or else the second and third ACEs should be changed to grant only COM\_RIGHTS\_EXECUTE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76491-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76491-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76491-114">Mejoras de seguridad de DCOM en Windows XP Service Pack 2 y Windows Server 2003 Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="76491-114">DCOM Security Enhancements in Windows XP Service Pack 2 and Windows Server 2003 Service Pack 1</span></span>](dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1.md)
</dt> <dt>

[<span data-ttu-id="76491-115">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="76491-115">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




