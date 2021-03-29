---
description: Resource Manager se ejecuta como un servicio de confianza en un único proceso. Todas las solicitudes de acceso a tarjetas inteligentes se realizan en el administrador de recursos, que las enruta al lector que contiene la tarjeta de destino.
ms.assetid: 4a62588a-14d9-43dc-9572-25a9cbcd0efd
title: Implementación de Administrador de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04ec653f999b74bb9851893b11e1fa49120a7bd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652651"
---
# <a name="resource-manager-implementation"></a>Implementación de Administrador de recursos

[*Resource Manager*](../secgloss/r-gly.md) se ejecuta como un servicio de confianza en un único proceso. Todas las solicitudes de acceso a [*tarjetas inteligentes*](../secgloss/s-gly.md) se realizan en el administrador de recursos, que las enruta al [*lector*](../secgloss/r-gly.md) que contiene la tarjeta de destino.

Las tarjetas inteligentes suelen usarse junto con la seguridad y la privacidad personal. Siempre que sea posible, el administrador de recursos utiliza los mecanismos de seguridad existentes en el sistema operativo subyacente al tener acceso a un lector o tarjeta inteligente.

 

 
