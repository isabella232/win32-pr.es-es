---
description: La tabla CounterData contiene una fila para cada contador que se recopila en un momento determinado. Habrá un gran número de estas filas.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: CounterData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253737"
---
# <a name="counterdata"></a>CounterData

La **tabla CounterData** contiene una fila para cada contador que se recopila en un momento determinado. Habrá un gran número de estas filas.

La **tabla CounterData** define los campos siguientes:

-   **GUID:** GUID para este conjunto de datos. Use esta clave para unirse a la [**tabla DisplayToID.**](displaytoid.md)
-   **CounterID:** Identifica el contador. Use esta clave para unirse a la [**tabla CounterDetails.**](counterdetails.md)
-   **RecordIndex:** Índice de ejemplo para un identificador de contador y GUID de colección específicos. El valor aumenta para cada ejemplo sucesivo en este archivo de registro.
-   **CounterDateTime:** Hora en que se inició la colección, en hora UTC.
-   **CounterValue:** Valor con formato del contador. Este valor puede ser cero para el primer registro si el contador requiere dos muestras para calcular un valor que se puede mostrar.
-   **FirstValueA:** Combine este valor de 32 bits con el valor **de FirstValueB** para crear el **miembro FirstValue** de [**PDH RAW \_ \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueA contiene** los bits de orden inferior.
-   **FirstValueB:** Combine este valor de 32 bits con el valor **de FirstValueA** para crear el **miembro FirstValue** de [**PDH RAW \_ \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueB contiene** los bits de orden alto.
-   **SecondValueA:** Combine este valor de 32 bits con el valor **de SecondValueB** para crear el **miembro SecondValue** de [**PDH RAW \_ \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueA contiene** los bits de orden bajo.
-   **SecondValueB:** Combine este valor de 32 bits con el valor **de SecondValueA** para crear el **miembro SecondValue** de [**PDH RAW \_ \_ COUNTER**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueB contiene** los bits de orden alto.

Los **campos GUID**, **CounterID** y **RecordIndex** son la clave principal de esta tabla.

 

 



