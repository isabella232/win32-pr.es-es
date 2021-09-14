---
description: Recomendaciones para transacciones óptimas del sistema de archivos.
ms.assetid: 847939ff-5322-4023-8ef7-9d845e80d65c
title: Consideraciones de rendimiento para NTFS transaccional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a71f7e100e1ddd8524932a4a259a12092bddcb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069875"
---
# <a name="performance-considerations-for-transactional-ntfs"></a>Consideraciones de rendimiento para NTFS transaccional

NTFS transaccional (TxF) se ha diseñado cuidadosamente para mejorar el rendimiento y normalmente tendrá un mejor rendimiento que las alternativas transaccionales de uso general en escenarios similares. Sin embargo, las transacciones del sistema de archivos tienen más sobrecarga que las operaciones sin transacciones y se espera cierta reducción en el rendimiento de E/S en comparación con las operaciones de E/S sin transacciones. Las aplicaciones críticas para el rendimiento deben realizar un ciclo de calificación de adopción de tecnología, evaluando el impacto en el rendimiento de las operaciones del sistema de archivos con transacciones.

## <a name="overview-of-txf-operations"></a>Información general de las operaciones de TxF

TxF usa el registro *de* deshacer para registrar los cambios necesarios para volver a poner el sistema de archivos en un estado coherente, también conocido como reversión, en caso de que se produzca una anulación de transacción. Este registro de deshacer genera E/S adicionales y es el origen de la sobrecarga de rendimiento de TxF en comparación con las operaciones del sistema de archivos no transaccionales.

A continuación se muestra un resumen general de cómo funciona TxF:

-   A medida que avanza una transacción, TxF escribe *los* registros de deshacer en su archivo de registro para cada modificación que realiza en el sistema de archivos. Si se produce una anulación, estos registros de deshacer se analizan para volver a poner el sistema de archivos en el estado que tenía antes de que se iniciara la transacción.
-   Un *registro de deshacer* un cambio de metadatos solo describe un cambio en los metadatos del sistema de archivos. Algunos ejemplos de esto son movimientos, cambios de nombre, anexos y cambios de atributos. En el caso de los registros de deshacer cambios de metadatos, toda la información necesaria para deshacer el cambio se encuentra en el registro y se almacena en el archivo de registro.
-   Un *registro de* deshacer sobrescritura describe una sobrescritura de una parte de un archivo. Cuando se produce una sobrescritura de archivos, el contenido original del archivo se almacena en un archivo de deshacer especial en un directorio oculto y el registro de deshacer sobrescritura apunta a este archivo. Cuando las actualizaciones de archivos se vacían finalmente de la memoria caché al disco, también se debe vaciar el contenido del archivo de deshacer, por lo que una sobrescritura de archivos con transacciones podría generar hasta dos operaciones de E/S aleatorias adicionales: una para leer los datos antiguos y otra para escribirla en el archivo de deshacer. Estas operaciones de E/S adicionales son un costo de rendimiento de TxF.
-   Cuando se produce una confirmación, TxF vacía primero toda la información de deshacer, vacía los cambios reales del archivo y, a continuación, escribe y vacía un registro de confirmación. Si no hay ningún archivo de deshacer para vaciar, la única sobrecarga adicional de TxF relativa a la E/S sin transacciones es que el registro se vacía por sí mismo. Sin embargo, los vaciados de registro tienen como resultado escrituras secuenciales de gran tamaño eficaces, por lo que el costo de rendimiento es mínimo.
-   TxF está optimizado para la confirmación. Se espera que la mayoría de las transacciones se realizarán correctamente y no tengan que revertirse, por lo que se espera que todos los registros de deshacer de una transacción no se utilicen. Desde la perspectiva del rendimiento, las operaciones de confirmación de TxF son rápidas y las reversión consumen muchos recursos.
-   La reversión consume más recursos que la confirmación. Durante la reversión, todos los cambios realizados en la transacción deben no realizarse. En general, la duración de la reversión puede ser aproximadamente la misma que tardó en realizar los cambios originalmente. Por ejemplo, si se tardó 1 segundo en realizar todos los cambios, podría tardar aproximadamente 1 segundo en deshacerlos. En el caso de transacciones muy largas, la reversión puede crear impactos adicionales en el rendimiento. Por ejemplo, el tiempo de arranque del sistema se puede retrasar si el sistema debe revertir automáticamente una transacción en caso de que el sistema deje de responder y deba realizar un reinicio no programado.

Las conclusiones de resumen sobre el rendimiento que se pueden extraer de la lista anterior son las siguientes:

-   El costo de rendimiento de TxF para las transacciones que implican sobrescrituras de archivos puede ser significativo.
-   El costo de rendimiento de TxF para las transacciones que solo implican operaciones de metadatos puede ser relativamente bajo, siempre que se usen transacciones de gran tamaño. Una transacción grande es cuando hay muchos registros de deshacer para cada registro de confirmación.

## <a name="recommendations-for-best-performance"></a>Recomendaciones Para obtener el mejor rendimiento

Amortizar la sobrecarga de TxF en transacciones más grandes. Por ejemplo, si tiene *N* conjuntos de cambios  que realizar donde cada cambio tiene M pasos y tiene la opción de hacerlo como *N* transacciones de *M* pasos cada uno o hacerlo todo como una transacción única con pasos  \* *M N,* la última opción sería más eficaz.

Tenga en cuenta el posible impacto en el arranque de transacciones muy grandes. Como se indicó anteriormente, la reversión puede ser lenta y retrasará el tiempo de arranque si el sistema necesita realizar reversión automática como tiempo de arranque. Cuanto mayor sea la transacción, mayor será el retraso.

Mantenga las transacciones en operaciones principalmente de metadatos. Esto es para lo que TxF está optimizado y, en general, el rendimiento es aproximadamente el mismo que el de E/S de archivos sin transacciones para transacciones de metadatos grandes. Algunos ejemplos de funciones txF de metadatos eficaces son [**MoveFileTransacted,**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) [**SetFileAttributesTransacted,**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda) [**CopyFileTransacted,**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda) [**DeleteFileTransacted,**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)y escrituras anexadas (llamadas a la función [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile) cuando el puntero de archivo como al final del archivo o *EOF*). Un ejemplo de operaciones sin metadatos que consumen muchos recursos son las llamadas a la función **WriteFile** cuando el puntero de archivo no está en el EOF.

## <a name="summary-of-txf-performance-expectations"></a>Resumen de las expectativas de rendimiento de TxF

En el caso de las actualizaciones locales, la sobrescritura en una sección de un archivo será mucho más lenta que la E/S de archivo sin transacciones, mientras que el rendimiento de TxF para las operaciones de metadatos del sistema de archivos (por ejemplo, crear, mover y anexar) es comparable a la E/S de archivos sin transacciones para transacciones grandes.

 

 



