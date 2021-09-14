---
description: En la tabla CounterDetails se describe un contador específico en un equipo determinado.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: CounterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253736"
---
# <a name="counterdetails"></a>CounterDetails

En **la tabla CounterDetails** se describe un contador específico en un equipo determinado.

La **tabla CounterDetails** define los campos siguientes:

-   **CounterID:** Identificador único de la base de datos que se asigna a una cadena de texto de nombre de contador específica. Este campo es la clave principal de esta tabla.
-   **MachineName:** Nombre del equipo que registró este conjunto de datos.
-   **ObjectName:** Nombre del objeto de rendimiento.
-   **CounterName:** Nombre del contador.
-   **CounterType:** Tipo de contador. Para obtener una lista de tipos de contadores y sus fórmulas, vea la sección Tipos de contador del Kit de implementación de [Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).
-   **DefaultScale:** Escalado predeterminado que se va a aplicar a los datos del contador de rendimiento sin procesar.
-   **InstanceName:** Nombre de la instancia del contador.
-   **InstanceIndex:** Número de índice de la instancia del contador.
-   **ParentName:** Algunos contadores están asociados lógicamente a otros y se conocen como "secundarios". Por ejemplo, el elemento primario de un subproceso es un proceso y el elemento primario de un controlador de disco lógico es una unidad física. Este campo contiene el nombre del elemento primario. El valor de este campo o el **campo ParentObjectID** identifica una instancia primaria específica. Si el valor de este campo es **NULL,** se debe comprobar el valor del **campo ParentObjectID** para identificar el elemento primario. Si los valores de ambos campos son **NULL,** el contador no tiene un elemento primario.
-   **ParentObjectID:** Identificador único del elemento primario. El valor de este campo o el **campo ParentName** identifica una instancia primaria específica. Si el valor de este campo es **NULL,** se debe comprobar el valor del **campo ParentName** para identificar el elemento primario.

 

 
