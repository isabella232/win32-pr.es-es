---
description: Todos los objetos protegibles organizan sus derechos de acceso mediante el formato de máscara de acceso que se muestra en la siguiente ilustración.
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: Formato de máscara de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910622"
---
# <a name="access-mask-format"></a><span data-ttu-id="7cc5c-103">Formato de máscara de acceso</span><span class="sxs-lookup"><span data-stu-id="7cc5c-103">Access Mask Format</span></span>

<span data-ttu-id="7cc5c-104">Todos los objetos protegibles organizan sus derechos de acceso mediante el formato de [*máscara de acceso*](/windows/desktop/SecGloss/a-gly) que se muestra en la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-104">All securable objects arrange their access rights by using the [*access mask*](/windows/desktop/SecGloss/a-gly) format shown in the following illustration.</span></span>

![formato de máscara de acceso](images/accctrl4.png)

<span data-ttu-id="7cc5c-106">En este formato, los 16 bits de orden inferior son para los derechos de acceso específicos del objeto, los 8 bits siguientes son para los [derechos de acceso estándar](standard-access-rights.md), que se aplican a la mayoría de los tipos de objetos, y los 4 bits de orden superior se usan para especificar [derechos de acceso genéricos](generic-access-rights.md) que cada tipo de objeto puede asignar a un conjunto de derechos estándar y específicos del objeto.</span><span class="sxs-lookup"><span data-stu-id="7cc5c-106">In this format, the low-order 16 bits are for object-specific access rights, the next 8 bits are for [standard access rights](standard-access-rights.md), which apply to most types of objects, and the 4 high-order bits are used to specify [generic access rights](generic-access-rights.md) that each object type can map to a set of standard and object-specific rights.</span></span> <span data-ttu-id="7cc5c-107">El \_ bit de seguridad del sistema de acceso \_ corresponde a la [derecha para tener acceso a la SACL del objeto](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="7cc5c-107">The ACCESS\_SYSTEM\_SECURITY bit corresponds to the [right to access the object's SACL](sacl-access-right.md).</span></span>

 

 
