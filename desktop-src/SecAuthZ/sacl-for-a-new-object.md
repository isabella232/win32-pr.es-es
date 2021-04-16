---
description: SACL para un nuevo objeto
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL para un nuevo objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652451"
---
# <a name="sacl-for-a-new-object"></a><span data-ttu-id="c2238-103">SACL para un nuevo objeto</span><span class="sxs-lookup"><span data-stu-id="c2238-103">SACL for a New Object</span></span>

<span data-ttu-id="c2238-104">El sistema utiliza el siguiente algoritmo para compilar una SACL para la mayoría de los tipos de objetos protegibles nuevos:</span><span class="sxs-lookup"><span data-stu-id="c2238-104">The system uses the following algorithm to build a SACL for most types of new securable objects:</span></span>

1.  <span data-ttu-id="c2238-105">La SACL del objeto es la SACL del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) especificado por el creador del objeto.</span><span class="sxs-lookup"><span data-stu-id="c2238-105">The object's SACL is the SACL from the [*security descriptor*](/windows/desktop/SecGloss/s-gly) specified by the object's creator.</span></span> <span data-ttu-id="c2238-106">El sistema combina cualquier ACE heredable en la SACL especificada, a menos que \_ el \_ bit protegido de SACL se establezca en los bits de control del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c2238-106">The system merges any inheritable ACEs into the specified SACL unless the SE\_SACL\_PROTECTED bit is set in the security descriptor's control bits.</span></span> <span data-ttu-id="c2238-107">\_ \_ \_ Las ACE de atributo de recurso del sistema y \_ \_ el ID. de directiva de ámbito del sistema \_ \_ ACE de un objeto primario se combinarán con un nuevo objeto incluso si \_ SE establece el bit protegido de SACL de se \_ .</span><span class="sxs-lookup"><span data-stu-id="c2238-107">SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs and SYSTEM\_SCOPED\_POLICY\_ID\_ACEs from a parent object will be merged to a new object even if the SE\_SACL\_PROTECTED bit is set.</span></span>
2.  <span data-ttu-id="c2238-108">Si el creador no especifica un descriptor de seguridad, el sistema genera la SACL del objeto a partir de las ACE heredables.</span><span class="sxs-lookup"><span data-stu-id="c2238-108">If the creator does not specify a security descriptor, the system builds the object's SACL from inheritable ACEs.</span></span>
3.  <span data-ttu-id="c2238-109">Si no hay ninguna SACL especificada o heredada, el objeto no tiene SACL.</span><span class="sxs-lookup"><span data-stu-id="c2238-109">If there is no specified or inherited SACL, the object has no SACL.</span></span>

<span data-ttu-id="c2238-110">Para especificar una SACL para un nuevo objeto, el creador del objeto debe tener el \_ privilegio de nombre de seguridad se \_ habilitado. [](privileges.md)</span><span class="sxs-lookup"><span data-stu-id="c2238-110">To specify a SACL for a new object, the object's creator must have the SE\_SECURITY\_NAME [privilege](privileges.md) enabled.</span></span> <span data-ttu-id="c2238-111">Si la SACL especificada para un nuevo objeto solo contiene \_ ACE de \_ atributo de recurso del sistema \_ , el \_ privilegio de nombre de seguridad se \_ no es necesario.</span><span class="sxs-lookup"><span data-stu-id="c2238-111">If the specified SACL for a new object contain only SYSTEM\_RESOURCE\_ATTRIBUTE\_ACEs, then the SE\_SECURITY\_NAME privilege is not required.</span></span> <span data-ttu-id="c2238-112">El creador no necesita este privilegio si la SACL del objeto se crea a partir de las ACE heredadas.</span><span class="sxs-lookup"><span data-stu-id="c2238-112">The creator does not need this privilege if the object's SACL is built from inherited ACEs.</span></span>

<span data-ttu-id="c2238-113">El sistema utiliza un algoritmo diferente para compilar una SACL para un nuevo objeto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2238-113">The system uses a different algorithm to build a SACL for a new Active Directory object.</span></span> <span data-ttu-id="c2238-114">Para obtener más información, consulte [cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span><span class="sxs-lookup"><span data-stu-id="c2238-114">For more information, see [How Security Descriptors are Set on New Directory Objects](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).</span></span>

 

 
