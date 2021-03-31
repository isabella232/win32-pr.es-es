---
title: Base de datos de asignación de marcado automático
description: La base de datos de asignación de marcado automático asigna direcciones de red a entradas de libretas de teléfonos RAS.
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511f15f98848559a892e8c20e766d47a07780fbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904644"
---
# <a name="autodial-mapping-database"></a>Base de datos de asignación de marcado automático

La base de datos de asignación de marcado automático asigna direcciones de red a entradas de libretas de teléfonos RAS. La base de datos puede incluir direcciones IP (por ejemplo, "172.21.167.35"), nombres de host de Internet (por ejemplo, "www.microsoft.com") o nombres NetBIOS (por ejemplo, "products1"). Asociados a cada dirección de la base de datos de marcado automático es un conjunto de una o más entradas de [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) . Cada una de estas entradas especifica una entrada de libreta de teléfonos que RAS puede marcar para conectarse a la dirección desde una determinada ubicación de marcado de la interfaz de programación de aplicaciones de telefonía (TAPI). Para obtener más información acerca de las ubicaciones de marcado TAPI, consulte la documentación de TAPI.

El marcado automático crea automáticamente entradas en la base de datos de asignación de marcado automático en dos situaciones:

-   Cuando se produce un error al intentar conectarse a una dirección de red

    Si no hay ninguna entrada para la dirección en la base de datos de asignación y el equipo no está conectado a una red, ya sea directamente o a través de RAS, el marcado automático solicitará al usuario que especifique la información necesaria para establecer una conexión de acceso telefónico. Si el usuario proporciona la información y la operación de conexión de acceso telefónico se realiza correctamente, el marcado automático almacena la información en la base de datos de asignación.

-   Cuando el equipo está conectado a una red a través de RAS

    Cada vez que el usuario se conecta a una dirección de red, el marcado automático crea una entrada en la base de datos. La entrada asigna la dirección de red a la entrada de la libreta de teléfonos que se usó para establecer la conexión RAS.

Puede usar la función [**RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) para agregar una dirección a la base de datos de asignación de marcado automático, eliminar una dirección de la base de datos o cambiar las entradas de marcado automático asociadas a una dirección existente en la base de datos. Puede usar la función [**RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) para recuperar las entradas de marcado automático asociadas a una dirección de red especificada en la base de datos de asignación de marcado automático. La función [**RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) devuelve una lista de todas las direcciones en la base de datos de asignación de marcado automático.

 

 