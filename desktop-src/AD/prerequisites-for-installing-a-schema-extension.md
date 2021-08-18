---
title: Requisitos previos para instalar una extensión de esquema
description: Para modificar el esquema, asegúrese de que tiene los siguientes derechos y de que conoce la siguiente información Debe tener derechos suficientes para modificar el esquema.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af50626d452c8e26cbf1e7d33addfcea4f854cd2b40b0860bb98c783044748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185307"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a>Requisitos previos para instalar una extensión de esquema

Para modificar el esquema, asegúrese de que tiene los siguientes derechos y de que conoce la siguiente información:

-   Debe tener derechos suficientes para modificar el esquema. El esquema contiene todas las definiciones de datos para Active Directory Domain Services para toda la empresa. Para actualizar el esquema, un usuario debe ser miembro del grupo Administradores de esquemas o tener delegados los derechos para actualizar el esquema.
-   Solo puede realizar cambios de esquema en el maestro de esquema. Para obtener más información, vea [Detectar el maestro de esquema.](detecting-the-schema-master.md)
-   El maestro de esquema debe poder escribirse; es decir, se debe quitar el bloqueo de seguridad en el registro. Para obtener más información, vea [Habilitar cambios de esquema en el maestro de esquema.](enabling-schema-changes-at-the-schema-master.md)
-   Para obtener más información sobre cómo comprobar si se puede modificar el maestro de esquema y cómo cambiar su configuración, vea "XADM: Unable to Update the Schema on the Schema Owner" (XADM: No se puede actualizar el esquema en el propietario del esquema) en la página ayuda y soporte Knowledge Base en [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .

 

 




