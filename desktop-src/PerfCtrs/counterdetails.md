---
description: En la tabla de detalles se describe un contador específico de un equipo determinado.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: Detalles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001984"
---
# <a name="counterdetails"></a>Detalles

En la tabla de **detalles** se describe un contador específico de un equipo determinado.

En la tabla de **detalles** se definen los campos siguientes:

-   **CounterID:** Un identificador único en la base de datos que se asigna a una cadena de texto de nombre de contador específico. Este campo es la clave principal de esta tabla.
-   **MachineName:** Nombre del equipo que registró este conjunto de datos.
-   **Objectname:** Nombre del objeto de rendimiento.
-   **Nombre:** Nombre del contador.
-   **Contratipo:** El tipo de contador. Para obtener una lista de los tipos de contador y sus fórmulas, vea la sección tipos de contador del [Kit de implementación de Windows Server 2003](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).
-   **DefaultScale:** Escalado predeterminado que se va a aplicar a los datos de contador de rendimiento sin procesar.
-   **NombreDeInstancia:** Nombre de la instancia de contador.
-   **InstanceIndex:** Número de índice de la instancia de contador.
-   **ParentName:** Algunos contadores están asociados lógicamente a otros y se conocen como elementos primarios. Por ejemplo, el elemento primario de un subproceso es un proceso y el primario de un controlador de disco lógico es una unidad física. Este campo contiene el nombre del elemento primario. El valor de este campo o el campo **iddeobjetoprincipal** identifica una instancia primaria específica. Si el valor de este campo es **null**, se debe comprobar el valor del campo **iddeobjetoprincipal** para identificar el elemento primario. Si los valores de los dos campos son **null**, el contador no tiene un elemento primario.
-   **Iddeobjetoprincipal:** Identificador único del elemento primario. El valor de este campo o del campo **ParentName** identifica una instancia primaria específica. Si el valor de este campo es **null**, se debe comprobar el valor del campo **ParentName** para identificar el elemento primario.

 

 
