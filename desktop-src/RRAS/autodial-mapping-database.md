---
title: Base de datos de asignación automática
description: La base de datos de asignación de AutoDial asigna direcciones de red a las entradas de la libreta de teléfono ras.
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e89bd065a136492281adb3424636a8820c76c76bf6867e70db75aecfa0f345d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036725"
---
# <a name="autodial-mapping-database"></a>Base de datos de asignación automática

La base de datos de asignación de AutoDial asigna direcciones de red a las entradas de la libreta de teléfono ras. La base de datos puede incluir direcciones IP (por ejemplo, "172.21.167.35"), nombres de host de Internet (por ejemplo, "www.microsoft.com") o nombres NetBIOS (por ejemplo, "products1"). Asociado a cada dirección de la base de datos AutoDial es un conjunto de una o varias [**entradas RASAUTODIALENTRY.**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) Cada una de estas entradas especifica una entrada de libreta de teléfonos que RAS puede marcar para conectarse a la dirección desde una ubicación de marcado de interfaz de programación de aplicaciones de telefonía (TAPI) determinada. Para más información sobre las ubicaciones de marcado de TAPI, consulte la documentación de TAPI.

AutoDial crea automáticamente entradas en la base de datos de asignación AutoDial en dos situaciones:

-   Cuando se produce un error al intentar conectarse a una dirección de red

    Si no hay ninguna entrada para la dirección en la base de datos de asignación y el equipo no está conectado a una red, ya sea directamente o a través de RAS, AutoDial solicita al usuario que especifique la información necesaria para establecer una conexión de acceso telefónico. Si el usuario proporciona la información y la operación de conexión de acceso telefónico se realiza correctamente, AutoDial almacena la información en la base de datos de asignación.

-   Cuando el equipo está conectado a una red a través de RAS

    Cada vez que el usuario se conecta a una dirección de red, AutoDial crea una entrada en la base de datos. La entrada asigna la dirección de red a la entrada de la libreta de teléfonos que se usó para establecer la conexión RAS.

Puede usar la función [**RasSetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) para agregar una dirección a la base de datos de asignación AutoDial, eliminar una dirección de la base de datos o cambiar las entradas AutoDial asociadas a una dirección existente en la base de datos. Puede usar la función [**RasGetAutodialAddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) para recuperar las entradas AutoDial asociadas a una dirección de red especificada en la base de datos de asignación AutoDial. La [**función RasEnumAutodialAddresses**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) devuelve una lista de todas las direcciones de la base de datos de asignación AutoDial.

 

 