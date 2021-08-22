---
description: Describe los conceptos de coherencia de lectura confirmada, aislamiento de lectura confirmada y bloqueo transaccional en NTFS transaccional.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Conceptos básicos de TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71b2ed4e906fab881fac93a686dcf3aff6e8a95fa72d785ef14320ef92c05ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950974"
---
# <a name="basic-txf-concepts"></a>Conceptos básicos de TxF

## <a name="read-isolation"></a>Aislamiento de lectura

NTFS transaccional (TxF) proporciona coherencia de lectura confirmada.

Un [*escritor de transacciones*](glossary.md) hace referencia a un identificador de archivo con transacciones abierto con cualquier permiso que no forma parte del acceso de lectura genérico, pero forma parte del acceso de escritura genérico. Un *escritor de transacciones* ve la versión más reciente de un archivo que incluye todos los cambios realizados por la misma transacción. Solo puede haber un escritor de transacciones por archivo. Los escritores sin transacciones siempre están bloqueados por un escritor de transacciones, incluso si el archivo se abre con permisos de escritura compartida.

Un [*lector de transacciones*](glossary.md) hace referencia a un identificador de archivo con transacciones abierto con cualquier permiso que forma parte del acceso de lectura genérico, pero que no forma parte del acceso de escritura genérico. Un *lector con transacciones* ve una versión confirmada del archivo que existía en el momento en que se abrió el identificador de archivo. El lector de transacciones está aislado de los efectos de los escritores de transacciones. Esto proporciona una vista coherente del archivo solo durante la vida útil del identificador de archivo y bloquea los escritores sin transacciones.

> [!Note]  
> Cuando se ha abierto un identificador para su modificación con la función [**CreateFileTransacted,**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) todas las aperturas posteriores del archivo dentro de esa transacción sean de solo lectura o no convertida por el sistema para que sea un escritor de transacciones con fines de aislamiento y otra semántica transaccional. Esto significa que, posteriormente, cuando se abre un identificador para el acceso de solo lectura, el identificador no recibe una vista del archivo antes del inicio de la transacción; recibe la vista de transacción activa del archivo.

 

Un identificador de archivo sin transacciones no ve ningún cambio realizado dentro de una transacción hasta que se confirma la transacción. El identificador de archivo sin transacciones recibe una vista aislada similar a un lector de transacciones, pero, a diferencia de un lector de transacciones, recibe la actualización del archivo cuando un escritor de transacciones confirma la transacción.

## <a name="isolation-levels"></a>Niveles de aislamiento

TxF proporciona aislamiento de lectura y confirmado. Esto significa que las actualizaciones de archivos no se ven fuera de la transacción. Además, si un archivo se abre más de una vez mientras se leen los archivos dentro de la transacción, es posible que vea resultados diferentes con cada apertura posterior. Es posible que los archivos que estaban disponibles la primera vez que se accedieron a ellos no estén disponibles (porque se eliminaron) o viceversa.

## <a name="transactional-locking"></a>Bloqueo transaccional

La creación de un escritor de transacciones en *un archivo bloquea transaccionalmente* el archivo. Después de que una transacción bloquee un archivo, otras operaciones del sistema de archivos externas a la transacción de bloqueo que intenten modificar el archivo bloqueado transaccionalmente producirán un error **con ERROR \_ SHARING \_ VIOLATION** o **ERROR \_ TRANSACTIONAL \_ CONFLICT**.

En la tabla siguiente se resume el bloqueo transaccional.



Archivo abierto actualmente por

Archivo abierto intentado por

Conseguido

Sin transacciones

Lector

Lector/escritor

Lector

Lector/escritor

Lector de transacciones

Sí

Sí

Sí

No2

Lector o escritor de transacciones

Sí

No2

Sí

No2

Lector sin transacciones

Sí

Sí

Sí

Sí

Lector o escritor sin transacciones

No1

No1

Sí

Sí

1. Error con **ERROR \_ TRANSACTIONAL \_ CONFLICT**<br/> 2. Error al compartir la **infracción \_ \_**<br/>



 

Si abre una secuencia con nombre para una modificación que usa una transacción, es necesario bloquear todo el archivo.

Además del bloqueo transaccional, se aplican las reglas típicas de uso compartido de archivos NTFS.

Debe tener en cuenta los dos modos de uso compartido de archivos siguientes en paralelo:

-   Modo de bloqueo transaccional.
-   Modos normales de uso compartido de archivos.

El modo que sea más restrictivo es el que se aplica.

 

 




