---
description: Las consultas de esquema son instrucciones WQL que solicitan definiciones de clase e información sobre las asociaciones de esquema.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Recuperar definiciones de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155857"
---
# <a name="retrieving-class-definitions"></a>Recuperar definiciones de clase

Las consultas de esquema son instrucciones WQL que solicitan definiciones de clase e información sobre las [asociaciones de esquema](schema-associations.md). Los proveedores de clases utilizan consultas de esquema en sus instancias de la clase [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) para especificar las clases que admiten cuando se registran en WMI. Las consultas de esquema se colocan en las propiedades **ResultSetQueries**, **ReferencedSetQueries** y **UnsupportedQueries** de la instancia de **\_ \_ ClassProviderRegistration** .

Las consultas de esquema son similares a las consultas de datos, ya que admiten las siguientes instrucciones WQL:

-   [SELECT](select-statement-for-schema-queries.md)
-   [ASSOCIATORS OF](schema-associations.md)
-   [REFERENCIAS DE](schema-associations.md)
-   [ISA](isa-operator-for-schema-queries.md)

Una consulta de esquema es similar a una [referencia de consulta de](references-of-statement.md) datos que especifica la palabra clave **ClassDefsOnly** . en otras palabras, que devuelve un conjunto de resultados de objetos de definición de clase en lugar de instancias reales de clases de asociación. Sin embargo, las referencias de solo devuelven definiciones de clase si hay instancias presentes. Una consulta de esquema devuelve definiciones de clase tanto si las instancias están presentes como si no.

 

 



