---
description: Para abrir un archivo de registro para leerlo, llame a PdhOpenQuery y especifique una ruta de acceso al archivo de registro.
ms.assetid: 1d8f8662-df1f-4f84-8b65-c152f79cc5c6
title: Trabajar con archivos de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2032b90036f8f58c07d8c7e80e7e7ac2b2701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667236"
---
# <a name="working-with-log-files"></a>Trabajar con archivos de registro

Para abrir un archivo de registro para leerlo, llame a [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) y especifique una ruta de acceso al archivo de registro. Para abrir un archivo de registro para escribirlo, debe llamar a [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Para cerrar un archivo de registro, llame a [**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery) o [**PdhCloseLog**](/windows/desktop/api/Pdh/nf-pdh-pdhcloselog) , en función de la función que haya usado para abrir el archivo de registro.

## <a name="reading-from-a-log-file"></a>Leer de un archivo de registro

Leer datos de rendimiento de un archivo de registro es igual que leer datos de un origen de tiempo real: se abre una consulta, se agregan contadores a la consulta y se llama a [**PdhCollectQueryData**](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata) para recopilar un ejemplo del archivo de registro. **PdhCollectQueryData** devuelve PDH \_ no hay \_ más \_ datos cuando se llega al final del archivo de registro.

Cada ejemplo del archivo de registro contiene una marca de tiempo para el momento en que se recopiló originalmente y se escribió en el archivo de registro. Para recuperar la marca de tiempo de la primera y la última muestra del archivo de registro, llame a la función [**PdhGetDataSourceTimeRange**](/windows/desktop/api/Pdh/nf-pdh-pdhgetdatasourcetimerangea) . Si desea limitar los ejemplos que lee del registro en un intervalo de tiempo específico, consulte [configuración de un intervalo de tiempo para una consulta](setting-a-time-range-for-a-query.md).

Si no sabe qué objetos y contadores de rendimiento existen en el archivo de registro, puede llamar a [**PdhEnumObjects**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectsa) para determinar la lista de objetos. Dado un objeto, puede llamar a [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa) o [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha) para recuperar una lista de las instancias y los contadores del objeto contenidos en el archivo de registro.

Si llama a [**PdhEnumObjectItems**](/windows/desktop/api/Pdh/nf-pdh-pdhenumobjectitemsa), use las listas de instancias y contadores para crear una ruta de acceso para cada combinación posible de instancia y contador. Cuando se llama a [**PdhAddCounter**](/windows/desktop/api/Pdh/nf-pdh-pdhaddcountera) para agregar el contador a la consulta, se producirá un error en la función si el archivo de registro no contiene la combinación indicada.

Si usa [**PdhExpandWildCardPath**](/windows/desktop/api/Pdh/nf-pdh-pdhexpandwildcardpatha), puede crear una ruta de acceso que contenga un carácter comodín para el nombre de instancia y el contador, por ejemplo, \\ Object ( \* ) \\ \* . La función devuelve la \_ \_ ruta de acceso no válida de PDH si el objeto no contiene una instancia. En este caso, llame a **PdhExpandWildCardPath** con un carácter comodín solo para Counter, por ejemplo, \\ Object \\ \* .

Los sistemas operativos más recientes pueden leer archivos de registro generados en sistemas operativos anteriores. sin embargo, los archivos de registro que se crearon en Windows Vista y sistemas operativos posteriores no se pueden leer en los sistemas operativos anteriores.

Para obtener un ejemplo en el que se leen los datos de un archivo de registro, vea [leer datos de rendimiento de un archivo de registro](reading-performance-data-from-a-log-file.md).

## <a name="reading-from-multiple-log-files"></a>Leer de varios archivos de registro

Si necesita crear una consulta que lea desde varios archivos de registro, llame a [**PdhBindInputDataSource**](/windows/desktop/api/Pdh/nf-pdh-pdhbindinputdatasourcea) para enlazar los archivos de registro. Después, debe usar las funciones de PDH que terminen en "H", por ejemplo, [**PdhOpenQueryH**](/windows/desktop/api/Pdh/nf-pdh-pdhopenqueryh).

## <a name="writing-to-a-log-file"></a>Escribir en un archivo de registro

Antes de escribir en un archivo de registro, llame a [**PdhOpenQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhopenquerya) para crear una consulta y especificar el origen de los datos de rendimiento, ya sea en tiempo real o en un archivo de registro. A continuación, agregue los contadores que desea consultar.

Para abrir el archivo de destino, llame a [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga). Especifique la consulta al abrir el archivo de registro. Para recopilar los datos de rendimiento y escribirlos en el archivo de registro, llame a [**PdhUpdateLog**](/windows/desktop/api/Pdh/nf-pdh-pdhupdateloga).

Si los datos del contador se escriben en un archivo de registro delimitado por comas (. csv) o delimitado por tabuladores (. TSV) y la ruta de acceso contiene una instancia de carácter comodín, la ruta de acceso se expande y solo se incluyen en el archivo de registro las instancias que existen en el momento en que se expande la ruta de acceso. Sin embargo, para los archivos de registro de tipo binario (. BLG) o SQL, el carácter comodín no se expande para que el archivo de registro contenga instancias que se crean durante el registro.

Para obtener un ejemplo en el que se escriben datos en un archivo de registro, vea [escribir datos de rendimiento en un archivo de registro](writing-performance-data-to-a-log-file.md).

## <a name="compressing-a-log-file"></a>Comprimir un archivo de registro

Puede usar la función [**PdhComputeCounterStatistics**](/windows/desktop/api/Pdh/nf-pdh-pdhcomputecounterstatistics) para comprimir un archivo de registro. Por ejemplo, lea diez registros de un archivo de registro, llame a **PdhComputeCounterStatistics** para calcular el valor medio y, a continuación, escriba el valor medio en un archivo de registro de salida.

En el tema siguiente se proporciona información adicional sobre el uso de un archivo de registro.

-   [Obtención del tamaño de un archivo de registro](getting-the-size-of-a-log-file.md)

 

 



