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
# <a name="prerequisites-for-installing-a-schema-extension"></a>Requisitos previos para la instalación de una extensión de esquema

Para modificar el esquema, asegúrese de que tiene los siguientes derechos y de que tiene en cuenta la siguiente información:

-   Debe tener derechos suficientes para modificar el esquema. El esquema contiene todas las definiciones de datos de Active Directory Domain Services para toda la empresa. Para actualizar el esquema, un usuario debe ser miembro del grupo administradores de esquema o tener delegados los derechos para actualizar el esquema.
-   Solo puede realizar cambios de esquema en el maestro de esquema. Para obtener más información, vea [detectar el maestro de esquema](detecting-the-schema-master.md).
-   El maestro de esquema debe ser grabable; es decir, se debe quitar el interbloqueo de seguridad en el registro. Para obtener más información, vea [habilitar los cambios de esquema en el maestro de esquema](enabling-schema-changes-at-the-schema-master.md).
-   Para obtener más información sobre cómo comprobar si se puede modificar el maestro de esquema y cómo cambiar su configuración, vea "XADM: no se puede actualizar el esquema en el propietario del esquema" en la base de conocimiento de ayuda y soporte técnico en [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .

 

 




