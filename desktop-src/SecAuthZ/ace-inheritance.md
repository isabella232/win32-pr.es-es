---
description: Una ACL de objetos puede contener las ACE que heredó de su contenedor primario.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Herencia ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6462ed9523c94090924981db252b938f2056cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001698"
---
# <a name="ace-inheritance"></a><span data-ttu-id="b2ec3-103">Herencia ACE</span><span class="sxs-lookup"><span data-stu-id="b2ec3-103">ACE Inheritance</span></span>

<span data-ttu-id="b2ec3-104">La ACL de un objeto puede contener las ACE que heredó de su contenedor primario.</span><span class="sxs-lookup"><span data-stu-id="b2ec3-104">An object's ACL can contain ACEs that it inherited from its parent container.</span></span> <span data-ttu-id="b2ec3-105">Por ejemplo, una subclave del registro puede heredar las ACE de la clave que se encuentra por encima en la jerarquía del registro.</span><span class="sxs-lookup"><span data-stu-id="b2ec3-105">For example, a registry subkey can inherit ACEs from the key above it in the registry hierarchy.</span></span> <span data-ttu-id="b2ec3-106">Del mismo modo, un archivo en un sistema de archivos NTFS puede heredar las ACE del directorio que lo contiene.</span><span class="sxs-lookup"><span data-stu-id="b2ec3-106">Likewise, a file in an NTFS file system can inherit ACEs from the directory that contains it.</span></span>

<span data-ttu-id="b2ec3-107">La estructura de [**\_ encabezado ACE**](/windows/desktop/api/Winnt/ns-winnt-ace_header) de una ACE contiene un conjunto de marcadores de herencia que controlan la herencia de ACE y el efecto de una ACE en el objeto al que está asociada.</span><span class="sxs-lookup"><span data-stu-id="b2ec3-107">The [**ACE\_HEADER**](/windows/desktop/api/Winnt/ns-winnt-ace_header) structure of an ACE contains a set of inheritance flags that control ACE inheritance and the effect of an ACE on the object to which it is attached.</span></span> <span data-ttu-id="b2ec3-108">El sistema interpreta los marcadores de herencia y otra información de herencia de acuerdo con las [reglas de herencia de ACE](ace-inheritance-rules.md).</span><span class="sxs-lookup"><span data-stu-id="b2ec3-108">The system interprets the inheritance flags and other inheritance information according to the [rules of ACE inheritance](ace-inheritance-rules.md).</span></span>

<span data-ttu-id="b2ec3-109">Estas reglas se han mejorado con las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="b2ec3-109">These rules have been enhanced with the following features:</span></span>

-   <span data-ttu-id="b2ec3-110">Compatibilidad con la [propagación automática de ACE heredables](automatic-propagation-of-inheritable-aces.md).</span><span class="sxs-lookup"><span data-stu-id="b2ec3-110">Support for [automatic propagation of inheritable ACEs](automatic-propagation-of-inheritable-aces.md).</span></span>
-   <span data-ttu-id="b2ec3-111">Marca que diferencia entre las ACE y ACE heredadas que se aplicaron directamente a un objeto.</span><span class="sxs-lookup"><span data-stu-id="b2ec3-111">A flag that differentiates between inherited ACEs and ACEs that were directly applied to an object.</span></span>
-   <span data-ttu-id="b2ec3-112">ACE específicas del objeto que permiten especificar el tipo de objeto secundario que puede heredar la ACE.</span><span class="sxs-lookup"><span data-stu-id="b2ec3-112">Object-specific ACEs that allow you to specify the type of child object that can inherit the ACE.</span></span>
-   <span data-ttu-id="b2ec3-113">La capacidad de evitar que una DACL o SACL herede las ACE mediante el establecimiento de los bits protegidos de la DACL de SE \_ \_ protegió o la \_ SACL \_ protegida en los bits de control [*del descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) , excepto para el atributo de recurso del sistema \_ \_ \_ ACE y el identificador de directiva del ámbito del sistema \_ \_ \_ \_ ACE.</span><span class="sxs-lookup"><span data-stu-id="b2ec3-113">The ability to prevent a DACL or SACL from inheriting ACEs by setting the SE\_DACL\_PROTECTED or SE\_SACL\_PROTECTED bits in the [*security descriptor's*](/windows/desktop/SecGloss/s-gly) control bits except for SYSTEM\_RESOURCE\_ATTRIBUTE\_ACE and SYSTEM\_SCOPED\_POLICY\_ID\_ACE.</span></span>

 

 
