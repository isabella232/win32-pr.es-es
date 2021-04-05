---
description: La tabla de contradatos contiene una fila por cada contador que se recopila en un momento determinado. Habrá un gran número de estas filas.
ms.assetid: 1253a9c7-b440-4ff2-b68c-c52b9b42a58b
title: Datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4604ce9886a6c4e3caa847dcf41a2d50b46d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909745"
---
# <a name="counterdata"></a>Datos

La tabla de **contradatos** contiene una fila por cada contador que se recopila en un momento determinado. Habrá un gran número de estas filas.

La tabla de **contradatos** define los campos siguientes:

-   **GUID:** GUID para este conjunto de datos. Use esta clave para combinar con la tabla [**DisplayToID**](displaytoid.md) .
-   **CounterID:** Identifica el contador. Use esta clave para combinar con la tabla de [**detalles**](counterdetails.md) .
-   **RecordIndex:** Índice de ejemplo de un identificador de contador específico y un GUID de colección. El valor aumenta para cada ejemplo sucesivo de este archivo de registro.
-   **Contradatetime:** La hora en que se inició la colección, en hora UTC.
-   **Contravalor:** Valor con formato del contador. Este valor puede ser cero para el primer registro si el contador requiere dos muestras para calcular un valor que se puede mostrar.
-   **FirstValueA:** Combine este valor de 32 bits con el valor de **FirstValueB** para crear el miembro **FirstValue** del [**\_ \_ contador sin formato de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueA** contiene los bits de orden inferior.
-   **FirstValueB:** Combine este valor de 32 bits con el valor de **FirstValueA** para crear el miembro **FirstValue** del [**\_ \_ contador sin formato de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **FirstValueB** contiene los bits de orden superior.
-   **SecondValueA:** Combine este valor de 32 bits con el valor de **SecondValueB** para crear el miembro **SecondValue** del [**\_ \_ contador sin formato de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueA** contiene los bits de orden inferior.
-   **SecondValueB:** Combine este valor de 32 bits con el valor de **SecondValueA** para crear el miembro **SecondValue** del [**\_ \_ contador sin formato de PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter). **SecondValueB** contiene los bits de orden superior.

Los campos **GUID**, **CounterID** y **RecordIndex** forman la clave principal de esta tabla.

 

 



