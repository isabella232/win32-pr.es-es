---
description: DACL para un nuevo objeto
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: DACL para un nuevo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155096"
---
# <a name="dacl-for-a-new-object"></a><span data-ttu-id="b4b31-103">DACL para un nuevo objeto</span><span class="sxs-lookup"><span data-stu-id="b4b31-103">DACL for a New Object</span></span>

<span data-ttu-id="b4b31-104">El sistema utiliza el siguiente algoritmo para crear una DACL para la mayoría de los tipos de objetos protegibles nuevos:</span><span class="sxs-lookup"><span data-stu-id="b4b31-104">The system uses the following algorithm to build a DACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="b4b31-105">La DACL del objeto es la DACL del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) especificado por el creador del objeto.</span><span class="sxs-lookup"><span data-stu-id="b4b31-105">The object's DACL is the DACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="b4b31-106">El sistema combina cualquier ACE heredable en la DACL especificada, a menos que \_ el \_ bit protegido de DACL se establezca en los bits de control del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b4b31-106">The system merges any inheritable ACEs into the specified DACL unless the SE\_DACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span>
2.  <span data-ttu-id="b4b31-107">Si el creador no especifica un descriptor de seguridad, el sistema crea la DACL del objeto a partir de las ACE heredables.</span><span class="sxs-lookup"><span data-stu-id="b4b31-107">If the creator does not specify a security descriptor, the system builds the object's DACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="b4b31-108">Si no se especifica ningún descriptor de seguridad y no hay ACE heredables, la DACL del objeto es la DACL predeterminada del [*token de suplantación*](/windows/desktop/SecGloss/i-gly) o [*principal*](/windows/desktop/SecGloss/p-gly) del creador.</span><span class="sxs-lookup"><span data-stu-id="b4b31-108">If no security descriptor is specified and there are no inheritable ACEs, the object's DACL is the default DACL from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creator.</span></span>
4.  <span data-ttu-id="b4b31-109">Si no hay ninguna DACL especificada, heredada o predeterminada, el sistema crea el objeto sin DACL, lo que permite que todos los usuarios tengan acceso total al objeto.</span><span class="sxs-lookup"><span data-stu-id="b4b31-109">If there is no specified, inherited, or default DACL, the system creates the object with no DACL, which allows everyone full access to the object.</span></span>

<span data-ttu-id="b4b31-110">El sistema utiliza un algoritmo diferente para crear una DACL para un nuevo objeto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b4b31-110">The system uses a different algorithm to build a DACL for a new Active Directory object.</span></span> <span data-ttu-id="b4b31-111">Para obtener más información, consulte [cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="b4b31-111">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
