---
description: La API de Peer Identity Manager permite crear, enumerar y manipular identidades del mismo nivel en una aplicación del mismo nivel.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Acerca de Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d062f7324bb949c657b7687b533058cb9e74d3102eea1e484284453d3ff7f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579925"
---
# <a name="about-identity-manager"></a>Acerca de Identity Manager

La API de Peer Identity Manager permite crear, enumerar y manipular identidades del mismo nivel en una aplicación del mismo nivel. Puede usar las identidades del mismo nivel creadas con esta API como entrada para las API de proveedor de espacios de nombres pnrp (Protocolo de resolución de nombres del mismo nivel) y agrupación del mismo nivel.

## <a name="peer-identity-manager-best-practices"></a>Procedimientos recomendados de Peer Identity Manager

Cada usuario debe tener algunas identidades del mismo nivel que puedan usar para las actividades del mismo nivel. Por ejemplo, un usuario podría tener dos identidades del mismo nivel para el trabajo y el trabajo.

Una aplicación del mismo nivel bien diseñada permite que un usuario seleccione una identidad del mismo nivel que se usará. Un usuario puede crear una nueva identidad del mismo nivel si ninguna de las identidades del mismo nivel existentes es adecuada para usarla con una aplicación.

Una aplicación del mismo nivel bien diseñada también controla el número de identidades que crea. Si una aplicación crea una identidad temporal del mismo nivel, la aplicación debe eliminar la identidad del mismo nivel cuando no sea necesaria. Si una aplicación no realiza este mantenimiento, es posible que Peer Identity Manager no pueda crear identidades del mismo nivel hasta que se quiten algunas identidades del mismo nivel.

 

 



