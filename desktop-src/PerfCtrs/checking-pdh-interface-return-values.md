---
description: El valor devuelto de las funciones PDH indica el éxito o error de la llamada de función, que es diferente del estado de los datos del contador.
ms.assetid: 00ea5521-bc28-4a87-aba9-46c911631503
title: Comprobar códigos de estado de datos de contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34c433e1c45badd3a2211a0e53051ad40d495f63a67b0ca509ae74a5cd99972
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978885"
---
# <a name="checking-counter-data-status-codes"></a>Comprobar códigos de estado de datos de contador

El valor devuelto de las funciones PDH indica el éxito o error de la llamada de función, que es diferente del estado de los datos del contador. Compruebe siempre el **miembro CStatus** de un valor de contador devuelto en las estructuras PDH para asegurarse de que los datos devueltos son válidos antes de usarlos. Si el valor del **miembro CStatus** no indica que se ha hecho correctamente, no use los datos. Estos son los valores de estado posibles para los contadores:



| Value                              | Significado                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDH \_ CSTATUS \_ NO \_ MACHINE          | PDH no pudo conectarse al equipo especificado en la ruta de acceso del contador. Si se devuelve este estado cuando se agrega el contador, el contador no se inicializa completamente. Cada vez que se actualiza la consulta, PDH vuelve a inste a la conexión. Cuando se establece la conexión, se reanuda la recopilación de datos normal.                                                                  |
| PDH \_ CSTATUS \_ NO \_ OBJECT           | Se encontró el equipo especificado, pero el objeto de rendimiento especificado se encontró en el equipo. Si se devuelve este estado cuando se agrega el contador, el contador especificado no se incluye en la consulta. Si un contador activo devuelve este estado, los datos de ese contador no son válidos. Cada vez que se solicitan los datos, PDH intenta obtener estos datos de contador. |
| PDH \_ CSTATUS \_ NO \_ INSTANCE         | No se encontró la instancia especificada en el objeto . Si se devuelve este estado mientras se agrega el contador a la consulta, el contador se agrega correctamente a la consulta, pero no hay datos disponibles hasta que aparezca la instancia específica y se devuelva un estado correcto.                                                                                                  |
| PDH \_ CSTATUS \_ NO \_ COUNTER          | No se encontró el contador especificado en el objeto especificado. Si se devuelve este estado cuando se agrega el contador, el contador no se agrega a la consulta. Si este estado se devuelve después de la recopilación de datos, los datos de ese contador no son válidos. Cada vez que se solicitan los datos, PDH intenta obtener estos datos de contador.                                             |
| DATOS PDH \_ CSTATUS \_ NO \_ VÁLIDOS        | El contador se encontró correctamente, pero los datos devueltos no son válidos. Este error puede producirse si el valor del contador es menor que el valor anterior. (Dado que los valores de contador siempre se incrementan, el valor del contador se revierte a cero cuando alcanza su valor máximo). Otra posible causa es un temporizador del sistema que no es correcto.                                              |
| DATOS \_ VÁLIDOS DE PDH CSTATUS \_ \_          | Los datos del contador se devolvieron correctamente, pero no se modificaron desde la última vez que se leyó el contador.                                                                                                                                                                                                                                                                    |
| PDH \_ CSTATUS \_ NEW \_ DATA            | Los datos del contador se devolvieron correctamente y son diferentes de la última vez que se leyó el contador. PDH CSTATUS NEW DATA se puede devolver en un contador de velocidad incluso si la tasa resultante es la \_ misma que la del último \_ \_ ejemplo. Esto se debe a que el valor de datos sin procesar que se usa en la determinación de este valor de estado ha cambiado, no la tasa calculada.                  |
| PDH \_ MORE \_ DATA                    | El búfer proporcionado no era lo suficientemente grande como para almacenar todos los datos del contador. Asigne un búfer mayor y vuelva a ejecutar la función.                                                                                                                                                                                                                                              |
| ELEMENTO CSTATUS DE PDH \_ \_ NO \_ \_ VALIDADO | El contador se ha agregado a la consulta, pero no se ha validado ni se ha accedido a él. No hay información de estado adicional disponible en este contador.                                                                                                                                                                                                                                 |
| PDH \_ CSTATUS \_ NO \_ COUNTERNAME      | No se especificó ningún nombre de contador en la consulta.                                                                                                                                                                                                                                                                                                                                      |
| PDH \_ CSTATUS \_ NO \_ COUNTER          | No se encontró el nombre de contador especificado.                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ NO \_ OBJECT           | No se encontró el objeto de rendimiento especificado.                                                                                                                                                                                                                                                                                                                             |
| PDH \_ CALC \_ NEGATIVE \_ DENOMINATOR   | Un contador tiene un valor denominador negativo.                                                                                                                                                                                                                                                                                                                                      |
| BASE DE TIEMPO NEGATIVA DE PDH \_ CALC \_ \_      | Un contador tiene un valor de base de tiempo negativo.                                                                                                                                                                                                                                                                                                                                         |
| PDH \_ CALC \_ NEGATIVE \_ VALUE         | Un contador tiene un valor negativo.                                                                                                                                                                                                                                                                                                                                                  |
| PDH \_ CSTATUS \_ NO \_ COUNTERNAME      | No se especificó ninguna ruta de acceso de contador.                                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ BAD \_ COUNTERNAME     | El formato de ruta de acceso del contador es incorrecto.                                                                                                                                                                                                                                                                                                                                            |



 

 

 



