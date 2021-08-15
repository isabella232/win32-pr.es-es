---
title: Publicación en un objeto de equipo
description: Normalmente, los servicios basados en host crean SCP en el objeto de equipo para el equipo host. Los servicios basados en host son servicios estrechamente vinculados a un único equipo host.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aac659ab2bf482ee6d6c57dd1481e487d6e2af95dfd85a092f48f4928499b102
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025363"
---
# <a name="publishing-under-a-computer-object"></a>Publicación en un objeto de equipo

Normalmente, los servicios basados en host crean SCP en el objeto de equipo para el equipo host. Los servicios basados en host son servicios estrechamente vinculados a un único equipo host.

**Para crear SCP en un objeto de equipo**

1.  Llame a [**la función GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) para obtener el nombre distintivo (DN) en el directorio del objeto de equipo del equipo local.
2.  Use ese DN para enlazar al objeto de equipo y crear el SCP.

Para obtener más información y un ejemplo de código, vea [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).

Tenga en cuenta que solo los equipos miembros del dominio tienen objetos de equipo válidos en el directorio .

Para obtener el nombre DNS o NetBIOS del equipo local, llame a la [**función GetComputerNameEx.**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)

 

 