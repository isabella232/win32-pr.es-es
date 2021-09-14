---
description: Las consultas de esquema son instrucciones WQL que solicitan definiciones de clase e información sobre las asociaciones de esquema.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Recuperar definiciones de clase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063915"
---
# <a name="retrieving-class-definitions"></a>Recuperar definiciones de clase

Las consultas de esquema son instrucciones WQL que solicitan definiciones de clase e información sobre las [asociaciones de esquema](schema-associations.md). Los proveedores de clases usan consultas de esquema en sus instancias de la [**\_ \_ clase ClassProviderRegistration**](--classproviderregistration.md) para especificar las clases que admiten cuando se registran con WMI. Las consultas de esquema se colocan en las propiedades **ResultSetQueries**, **ReferencedSetQueries** y **UnsupportedQueries** de la **\_ \_ instancia classProviderRegistration.**

Las consultas de esquema son similares a las consultas de datos en que admiten las siguientes instrucciones WQL:

-   [SELECT](select-statement-for-schema-queries.md)
-   [ASOCIADORES DE](schema-associations.md)
-   [REFERENCIAS DE](schema-associations.md)
-   [ISA](isa-operator-for-schema-queries.md)

Una consulta de esquema es similar a una consulta de datos [REFERENCES OF](references-of-statement.md) que especifica la palabra clave **ClassDefsOnly;** es decir, que devuelve un conjunto de resultados de objetos de definición de clase en lugar de instancias reales de clases de asociación. Sin embargo, REFERENCES OF devuelve definiciones de clase solo si hay instancias presentes. Una consulta de esquema devuelve definiciones de clase tanto si las instancias están presentes como si no.

 

 



