---
description: La API del administrador de identidades del mismo nivel permite crear, enumerar y manipular identidades del mismo nivel en una aplicación del mismo nivel.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Acerca de Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909793"
---
# <a name="about-identity-manager"></a>Acerca de Identity Manager

La API del administrador de identidades del mismo nivel permite crear, enumerar y manipular identidades del mismo nivel en una aplicación del mismo nivel. Puede usar las identidades del mismo nivel creadas con esta API como entrada para las API del proveedor de espacios de nombres del Protocolo de resolución de nombres de mismo nivel (PNRP) y de agrupación del mismo nivel.

## <a name="peer-identity-manager-best-practices"></a>Prácticas recomendadas para el administrador de identidades del mismo nivel

Cada usuario debe tener algunas identidades del mismo nivel que pueden usar para las actividades del mismo nivel. Por ejemplo, un usuario podría tener dos identidades del mismo nivel para trabajo y ocio.

Una aplicación del mismo nivel bien diseñada permite al usuario seleccionar la identidad del mismo nivel que se va a usar. Un usuario puede crear una nueva identidad del mismo nivel si ninguna de las identidades del mismo nivel existente es adecuada para usarla con una aplicación.

Una aplicación del mismo nivel bien diseñada también controla el número de identidades que crea. Si una aplicación crea una identidad del mismo nivel temporal, la aplicación debe eliminar la identidad del mismo nivel cuando no se necesita la identidad. Si una aplicación no realiza este mantenimiento, es posible que el administrador de identidad del mismo nivel no pueda crear identidades del mismo nivel hasta que se quiten algunas identidades del mismo nivel.

 

 



