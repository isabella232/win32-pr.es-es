---
title: Requisitos previos para la instalación de una extensión de esquema
description: Para modificar el esquema, asegúrese de que tiene los siguientes derechos y de que tiene en cuenta la siguiente información; debe tener derechos suficientes para modificar el esquema.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104358719"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a><span data-ttu-id="542f8-103">Requisitos previos para la instalación de una extensión de esquema</span><span class="sxs-lookup"><span data-stu-id="542f8-103">Prerequisites for Installing a Schema Extension</span></span>

<span data-ttu-id="542f8-104">Para modificar el esquema, asegúrese de que tiene los siguientes derechos y de que tiene en cuenta la siguiente información:</span><span class="sxs-lookup"><span data-stu-id="542f8-104">To modify the schema, ensure you have the following rights and are aware of the following information:</span></span>

-   <span data-ttu-id="542f8-105">Debe tener derechos suficientes para modificar el esquema.</span><span class="sxs-lookup"><span data-stu-id="542f8-105">You must have sufficient rights to modify the schema.</span></span> <span data-ttu-id="542f8-106">El esquema contiene todas las definiciones de datos de Active Directory Domain Services para toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="542f8-106">The schema contains all of the data definitions for Active Directory Domain Services for the entire enterprise.</span></span> <span data-ttu-id="542f8-107">Para actualizar el esquema, un usuario debe ser miembro del grupo administradores de esquema o tener delegados los derechos para actualizar el esquema.</span><span class="sxs-lookup"><span data-stu-id="542f8-107">To update the schema, a user must be a member of the Schema Administrators group, or have been delegated the rights to update the schema.</span></span>
-   <span data-ttu-id="542f8-108">Solo puede realizar cambios de esquema en el maestro de esquema.</span><span class="sxs-lookup"><span data-stu-id="542f8-108">You can only make schema changes at the schema master.</span></span> <span data-ttu-id="542f8-109">Para obtener más información, vea [detectar el maestro de esquema](detecting-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="542f8-109">For more information, see [Detecting the Schema Master](detecting-the-schema-master.md).</span></span>
-   <span data-ttu-id="542f8-110">El maestro de esquema debe ser grabable; es decir, se debe quitar el interbloqueo de seguridad en el registro.</span><span class="sxs-lookup"><span data-stu-id="542f8-110">The schema master must be writable; that is, the safety interlock in the registry must be removed.</span></span> <span data-ttu-id="542f8-111">Para obtener más información, vea [habilitar los cambios de esquema en el maestro de esquema](enabling-schema-changes-at-the-schema-master.md).</span><span class="sxs-lookup"><span data-stu-id="542f8-111">For more information, see [Enabling Schema Changes at the Schema Master](enabling-schema-changes-at-the-schema-master.md).</span></span>
-   <span data-ttu-id="542f8-112">Para obtener más información sobre cómo comprobar si se puede modificar el maestro de esquema y cómo cambiar su configuración, vea "XADM: no se puede actualizar el esquema en el propietario del esquema" en la base de conocimiento de ayuda y soporte técnico en [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span><span class="sxs-lookup"><span data-stu-id="542f8-112">For more information about how to check whether the schema master can be modified, and how to change its settings, see "XADM: Unable to Update the Schema on the Schema Owner" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .</span></span>

 

 




