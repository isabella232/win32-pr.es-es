---
description: El valor devuelto de las funciones de PDH indica el éxito o el error de la llamada de función, que es diferente del estado de los datos del contador.
ms.assetid: 00ea5521-bc28-4a87-aba9-46c911631503
title: Comprobar códigos de estado de datos de contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7daed51ba6e8df385170b9a23b419267409ef497
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667344"
---
# <a name="checking-counter-data-status-codes"></a>Comprobar códigos de estado de datos de contador

El valor devuelto de las funciones de PDH indica el éxito o el error de la llamada de función, que es diferente del estado de los datos del contador. Compruebe siempre el miembro **CStatus** de un valor de contador devuelto en las estructuras PDH para asegurarse de que los datos devueltos son válidos antes de utilizarlos. Si el valor del miembro **CStatus** no indica que la operación se ha realizado correctamente, no use los datos. A continuación se muestran los posibles valores de estado para los contadores:



| Value                              | Significado                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PDH \_ CSTATUS \_ sin \_ equipo          | PDH no pudo conectarse al equipo especificado en la ruta de acceso del contador. Si se devuelve este estado cuando se agrega el contador, el contador no se inicializa por completo. Cada vez que se actualiza la consulta, PDH vuelve a intentar la conexión. Cuando se establece la conexión, se reanuda la recopilación de datos normal.                                                                  |
| PDH \_ CSTATUS \_ ningún \_ objeto           | Se encontró el equipo especificado, pero se encontró el objeto de rendimiento especificado en el equipo. Si se devuelve este estado cuando se agrega el contador, el contador especificado no se incluye en la consulta. Si un contador activo devuelve este estado, los datos de ese contador no son válidos. Cada vez que se solicitan los datos, PDH intenta obtener estos datos de contador. |
| PDH \_ CSTATUS \_ sin \_ instancia         | No se encontró la instancia especificada en el objeto. Si se devuelve este estado mientras se agrega el contador a la consulta, el contador se agrega correctamente a la consulta, pero no hay datos disponibles hasta que aparezca la instancia específica y se devuelva un estado correcto.                                                                                                  |
| \_CSTATUS \_ no \_ contador de PDH          | No se encontró el contador especificado en el objeto especificado. Si se devuelve este estado cuando se agrega el contador, el contador no se agrega a la consulta. Si este estado se devuelve después de la recopilación de datos, los datos de ese contador no son válidos. Cada vez que se solicitan los datos, PDH intenta obtener estos datos de contador.                                             |
| \_ \_ datos no válidos de PDH CSTATUS \_        | El contador se encontró correctamente, pero los datos devueltos no son válidos. Este error puede producirse si el valor del contador es menor que el valor anterior. (Dado que los valores de contador siempre aumentan, el valor del contador se revierte a cero cuando alcanza su valor máximo). Otra posible causa es un temporizador del sistema que no sea correcto.                                              |
| \_ \_ datos válidos de PDH CSTATUS \_          | Los datos del contador se devolvieron correctamente, pero no se han modificado desde la última vez que se leyó el contador.                                                                                                                                                                                                                                                                    |
| \_ \_ datos nuevos de PDH CSTATUS \_            | Los datos del contador se devolvieron correctamente y son diferentes de la última vez que se leyó el contador. Los \_ \_ nuevos \_ datos de PDH CSTATUS se pueden devolver en un contador de tarifas, incluso si la velocidad resultante es la misma que la del último ejemplo. Esto se debe a que el valor de datos sin procesar que se usa en la determinación de este valor de Estado ha cambiado, no la tasa calculada.                  |
| PDH \_ más \_ datos                    | El búfer proporcionado no era lo suficientemente grande como para almacenar todos los datos del contador. Asigne un búfer mayor y vuelva a ejecutar la función.                                                                                                                                                                                                                                              |
| \_elemento CSTATUS de PDH \_ \_ no \_ validado | El contador se ha agregado a la consulta, pero no se ha validado ni se ha tenido acceso a él. No hay información de estado adicional disponible en este contador.                                                                                                                                                                                                                                 |
| PDH \_ CSTATUS \_ sin \_ nombre      | No se especificó ningún nombre de contador en la consulta.                                                                                                                                                                                                                                                                                                                                      |
| \_CSTATUS \_ no \_ contador de PDH          | No se pudo encontrar el nombre de contador especificado.                                                                                                                                                                                                                                                                                                                                   |
| PDH \_ CSTATUS \_ ningún \_ objeto           | No se encontró el objeto de rendimiento especificado.                                                                                                                                                                                                                                                                                                                             |
| \_ \_ denominador de cálculo negativo de PDH \_   | Un contador tiene un valor de denominador negativo.                                                                                                                                                                                                                                                                                                                                      |
| base de tiempo negativa de cálculo de PDH \_ \_ \_      | Un contador tiene un valor de base de tiempo negativo.                                                                                                                                                                                                                                                                                                                                         |
| \_ \_ valor negativo del cálculo de PDH \_         | Un contador tiene un valor negativo.                                                                                                                                                                                                                                                                                                                                                  |
| PDH \_ CSTATUS \_ sin \_ nombre      | No se especificó ninguna ruta de contador.                                                                                                                                                                                                                                                                                                                                                   |
| \_ \_ nombre incorrecto de PDH CSTATUS \_     | El formato de la ruta de acceso del contador es incorrecto.                                                                                                                                                                                                                                                                                                                                            |



 

 

 



