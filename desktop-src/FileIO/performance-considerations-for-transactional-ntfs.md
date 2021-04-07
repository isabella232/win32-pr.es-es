---
description: Recomendaciones para las transacciones de sistema de archivos óptimas.
ms.assetid: 847939ff-5322-4023-8ef7-9d845e80d65c
title: Consideraciones de rendimiento para NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a71f7e100e1ddd8524932a4a259a12092bddcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002608"
---
# <a name="performance-considerations-for-transactional-ntfs"></a>Consideraciones de rendimiento para NTFS transaccional

NTFS transaccional (TxF) se ha diseñado cuidadosamente para mejorar el rendimiento y, por lo general, funciona mejor que las alternativas transaccionales de uso general en escenarios similares. Sin embargo, las transacciones del sistema de archivos tienen más sobrecarga que las operaciones sin transacciones y se espera una reducción en el rendimiento de e/s en comparación con la e/s sin transacciones. Las aplicaciones críticas para el rendimiento deben realizar un ciclo de calificación de adopción de tecnología y evaluar el impacto en el rendimiento de las operaciones del sistema de archivos transaccionales.

## <a name="overview-of-txf-operations"></a>Información general de las operaciones de TxF

TxF usa el registro de *Deshacer* para registrar los cambios necesarios para volver a poner el sistema de archivos en un estado coherente, también conocido como reversión, en caso de que se produzca una anulación de transacción. Este registro de deshacer genera e/s adicional y es el origen de la sobrecarga de rendimiento de TxF en comparación con las operaciones del sistema de archivos no transaccionales.

A continuación se muestra un resumen de alto nivel de cómo funciona TxF:

-   A medida que progresa una transacción, TxF escribe los registros de *Deshacer* en su archivo de registro para cada modificación que realiza en el sistema de archivos. Si se produce una anulación, estos registros de deshacer se analizan para volver a poner el sistema de archivos en el estado en que se encontraba antes de que comenzara la transacción.
-   Un registro de deshacer de *cambio de metadatos* describe un cambio solo en los metadatos del sistema de archivos. Algunos ejemplos de esto son los movimientos, el cambio de nombre, los anexos y los cambios de atributo. En el caso de los registros de deshacer de cambio de metadatos, toda la información necesaria para deshacer el cambio está en el registro y se almacena en el archivo de registro.
-   Un registro de deshacer *sobrescritura* describe una sobrescritura de una parte de un archivo. Cuando se produce la sobrescritura de un archivo, el contenido original del archivo se almacena en un archivo de deshacer especial en un directorio oculto y el registro de deshacer sobrescritura apunta a este archivo. Cuando las actualizaciones de archivos se vacían de la caché al disco, también se debe vaciar el contenido del archivo para deshacer, por lo que una sobrescritura de archivos de transacción podría generar hasta dos operaciones de e/s aleatorias adicionales: una para leer los datos antiguos y otra para escribirla en el archivo para deshacer. Estas operaciones de e/s adicionales son un costo de rendimiento de TxF.
-   Cuando se produce una confirmación, TxF vacía primero toda la información de deshacer, luego vacía los cambios reales del archivo y, a continuación, escribe y vacía un registro de confirmación. Si no hay ningún archivo para deshacer que vaciar, la única sobrecarga adicional de TxF relativa a la e/s sin transacciones es que el registro se vacíe a sí mismo. Sin embargo, los vaciados del registro producen escrituras secuenciales grandes y eficaces para que el costo de rendimiento sea mínimo.
-   TxF está optimizado para la confirmación. Se espera que la mayoría de las transacciones se realicen correctamente y no sea necesario revertir, por lo que se espera que todos los registros de deshacer de una transacción queden sin usar. Desde el punto de vista del rendimiento, las operaciones de confirmación de TxF son rápidas y las reversiones hacen un uso intensivo de los recursos.
-   La reversión requiere más recursos que la confirmación. Durante la reversión, todos los cambios realizados en la transacción deben deshacerse. En general, la duración de la reversión puede ser aproximadamente la misma que tardó originalmente en realizar los cambios. Por ejemplo, si tardó 1 segundo en realizar todos los cambios, podría tardar aproximadamente 1 segundo en deshacerlos. En el caso de transacciones muy largas, la reversión puede crear impactos de rendimiento adicionales. Por ejemplo, se puede retrasar el tiempo de arranque del sistema si el sistema debe revertir automáticamente una transacción en caso de que el sistema deje de responder y deba realizar un reinicio no programado.

Las conclusiones de resumen sobre el rendimiento que se pueden extraer de la lista anterior son las siguientes:

-   El costo de rendimiento de TxF para las transacciones que implican sobrescrituras de archivos puede ser significativo.
-   El costo de rendimiento de TxF para las transacciones que implican solo operaciones de metadatos puede ser relativamente bajo, siempre que se usen transacciones grandes. Una transacción grande es cuando hay muchos registros de deshacer para cada registro de confirmación.

## <a name="recommendations-for-best-performance"></a>Recomendaciones para obtener el mejor rendimiento

Amortizar la sobrecarga de TxF en transacciones de mayor tamaño. Por ejemplo, si tiene *n* conjuntos de cambios para que cada cambio tenga *m* pasos y tiene la opción de hacer esto como *n* transacciones de *m* pasos cada uno o hacer todo como una sola transacción con *m* \* *N* pasos, la última opción sería más eficaz.

Tenga en cuenta el posible impacto en el arranque de transacciones de gran tamaño. Como se indicó anteriormente, la reversión puede ser lenta y retrasará el tiempo de arranque si el sistema necesita realizar reversiones automáticas como hora de arranque. Cuanto mayor sea la transacción, mayor será el retraso.

Mantenga las transacciones a las operaciones de metadatos principalmente. Este es el modo en que TxF está optimizado para y, en general, el rendimiento es aproximadamente el mismo que la e/s de archivos sin transacciones para transacciones de metadatos de gran tamaño. Ejemplos de funciones de TxF de metadatos eficientes son [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda), [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda), [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda), [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda), [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)y escrituras anexadas (llama a la función [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) cuando el puntero de archivo está al final del archivo o *EOF*). Un ejemplo de operaciones de metadatos que consumen muchos recursos son las llamadas a la función **WriteFile** cuando el puntero de archivo no está en EOF.

## <a name="summary-of-txf-performance-expectations"></a>Resumen de las expectativas de rendimiento de TxF

En el caso de las actualizaciones en contexto, las sobrescrituras en una sección de un archivo serán mucho más lentas que las de e/s de archivo sin transacciones, mientras que el rendimiento de TxF para las operaciones de metadatos del sistema de archivos (por ejemplo, crear, trasladar y anexar) es comparable a la e/s de archivos no transaccionales para transacciones grandes.

 

 



