---
description: Describe la coherencia de lectura confirmada, el aislamiento de lectura confirmada y los conceptos de bloqueo transaccional en NTFS transaccional.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Conceptos básicos de TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361163"
---
# <a name="basic-txf-concepts"></a>Conceptos básicos de TxF

## <a name="read-isolation"></a>Aislamiento de lectura

NTFS transaccional (TxF) proporciona coherencia de lectura confirmada.

Un [*escritor de transacciones*](glossary.md) hace referencia a un identificador de archivo de transacción abierto con cualquier permiso que no forma parte del acceso de lectura genérico, pero que forma parte del acceso de escritura genérico. Un *escritor de transacciones* ve la versión más reciente de un archivo que incluye todos los cambios realizados por la misma transacción. Solo puede haber un escritor de transacción por archivo. Los escritores sin transacciones siempre están bloqueados por un escritor de transacciones, incluso si el archivo se abre con permisos de escritura compartida.

Un [*lector de transacciones*](glossary.md) hace referencia a un identificador de archivo de transacciones abierto con cualquier permiso que forme parte del acceso de lectura genérico, pero que no forme parte del acceso de escritura genérico. Un *lector de transacciones* ve una versión confirmada del archivo que existía en el momento en que se abrió el identificador de archivo. El lector de transacciones está aislado de los efectos de los escritores de transacciones. Esto proporciona una vista coherente del archivo solo mientras dure el identificador de archivo y bloquea los escritores sin transacciones.

> [!Note]  
> Cuando se ha abierto un identificador para su modificación con la función [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) , todas las aperturas posteriores del archivo dentro de esa transacción, ya sean de solo lectura o no, las convierte el sistema para que sea un escritor de transacciones con el fin de aislamiento y otra semántica transaccional. Esto significa que, posteriormente, cuando se abre un identificador para el acceso de solo lectura, el identificador no recibe una vista del archivo antes del inicio de la transacción; recibe la vista de transacción activa del archivo.

 

Un identificador de archivo sin transacciones no ve ningún cambio realizado dentro de una transacción hasta que se confirma la transacción. El identificador de archivo sin transacciones recibe una vista aislada similar a un lector de transacciones, pero a diferencia de un lector de transacciones, recibe la actualización del archivo cuando un escritor de transacciones confirma la transacción.

## <a name="isolation-levels"></a>Niveles de aislamiento

TxF proporciona aislamiento de lectura confirmada. Esto significa que las actualizaciones de archivos no se ven fuera de la transacción. Además, si un archivo se abre más de una vez al leer archivos dentro de la transacción, puede ver resultados diferentes con cada apertura subsiguiente. Los archivos que estaban disponibles la primera vez que tuvo acceso a ellos pueden no estar disponibles (porque se eliminaron), o viceversa.

## <a name="transactional-locking"></a>Bloqueo transaccional

Al crear un escritor de transacciones en un archivo, se *bloquea* el archivo de una transacción. Una vez que un archivo está bloqueado por una transacción, otras operaciones del sistema de archivos externas a la transacción de bloqueo que intentan modificar el archivo bloqueado de forma transaccional producirán un error con **\_ \_ infracción de uso compartido de errores** o **\_ \_ conflicto transaccional de errores**.

En la tabla siguiente se resume el bloqueo transaccional.



Archivo abierto actualmente por

Intento de apertura de archivo

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

Lector/escritor de transacción

Sí

No2

Sí

No2

Lector sin transacciones

Sí

Sí

Sí

Sí

Lector/escritor sin transacciones

No1

No1

Sí

Sí

1. Error de **\_ \_ conflicto transaccional**<br/> 2. se produce un **error de \_ \_ infracción de uso compartido**<br/>



 

Si abre una secuencia con nombre para una modificación que está utilizando una transacción, se requiere que el archivo completo esté bloqueado.

Además del bloqueo transaccional, se aplican las reglas típicas de uso compartido de archivos NTFS.

En paralelo, debe tener en cuenta los dos modos de uso compartido de archivos siguientes:

-   Modo de bloqueo transaccional.
-   Modos normales de uso compartido de archivos.

El modo que sea más restrictivo es el que se aplica.

 

 




