---
title: Publicación en un objeto de equipo
description: Normalmente, los servicios basados en host crean los SCP en el objeto de equipo para el equipo host. Los servicios basados en host están estrechamente relacionados con un solo equipo host.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904477"
---
# <a name="publishing-under-a-computer-object"></a>Publicación en un objeto de equipo

Normalmente, los servicios basados en host crean los SCP en el objeto de equipo para el equipo host. Los servicios basados en host están estrechamente relacionados con un solo equipo host.

**Para crear SCP en un objeto de equipo**

1.  Llame a la función [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) para obtener el nombre distintivo (DN) en el directorio del objeto de equipo del equipo local.
2.  Use ese DN para enlazar con el objeto de equipo y crear el SCP.

Para obtener más información y un ejemplo de código, vea [cómo los clientes buscan y usan un punto de conexión de servicio](how-clients-find-and-use-a-service-connection-point.md).

Tenga en cuenta que solo los equipos miembros del dominio tienen objetos de equipo válidos en el directorio.

Para obtener el nombre DNS o NetBIOS del equipo local, llame a la función [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .

 

 