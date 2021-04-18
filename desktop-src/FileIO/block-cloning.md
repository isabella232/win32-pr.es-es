---
description: Una operación de clonación de bloques indica al sistema de archivos que copie un intervalo de bytes de archivo en nombre de una aplicación.
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: Clonación de bloques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33aa1c1eee693b6ed4b502aedc6da6176ece3e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546702"
---
# <a name="block-cloning"></a>Clonación de bloques

Una operación de *clonación de bloques* indica al sistema de archivos que copie un intervalo de bytes de archivo en nombre de una aplicación. El archivo de destino puede ser el mismo que el archivo de origen, o distinto de él.

Un sistema de archivos administra las asignaciones de [clústeres y extensiones](clusters-and-extents.md), y puede ser capaz de realizar la copia modificando el número de clúster virtual (VCN) en las asignaciones de número de clúster lógico (LCN) como una operación de metadatos de bajo costo, en lugar de leer y escribir los datos de archivo subyacentes. Esto permite que la copia se complete más rápido y genera menos e/s en el almacenamiento subyacente. Además, es posible que varios archivos compartan ahora clústeres lógicos después del clon de bloque, lo que ahorra capacidad al no almacenar clústeres idénticos varias veces en el disco.

Una operación de clonación de bloques no interrumpe el aislamiento proporcionado entre los archivos. Una vez que se completa un clon de bloque, las operaciones de escritura en el archivo de código fuente no aparecen en el destino, o viceversa.

La clonación de bloques solo está disponible en el tipo de [sistema de archivos ReFS](/windows/desktop/w8cookbook/resilient-file-system--refs-) a partir de Windows Server 2016.

## <a name="block-cloning-on-refs"></a>Bloquear la clonación en ReFS

ReFS en Windows Server 2016 implementa la clonación de bloques mediante la reasignación de los clústeres lógicos (es decir, las ubicaciones físicas en un volumen) de la región de origen a la región de destino. A continuación, usa un mecanismo de asignación de escritura para garantizar el aislamiento entre esas regiones. Las regiones de origen y de destino pueden estar en el mismo archivo o en archivos distintos.

Esta implementación requiere que los desplazamientos de archivo inicial y final se alineen con los límites del clúster. En ReFS en Windows Server 2016, los clústeres tienen un tamaño de 4 KB de forma predeterminada, pero se pueden establecer opcionalmente en 64 KB. El tamaño del clúster es un conjunto de parámetros en todo el volumen en el momento del formato.

## <a name="restrictions-and-remarks"></a>Restricciones y comentarios

-   Las regiones de origen y de destino deben comenzar y finalizar en un límite de clúster.
-   La región clonada debe ser inferior a 4 GB de longitud.
-   La región de destino no debe extenderse más allá del final del archivo. Si la aplicación desea extender el destino con datos clonados, primero debe llamar a [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).
-   Si las regiones de origen y destino están en el mismo archivo, no deben superponerse. (Es posible que la aplicación pueda continuar dividiendo la operación de clonación de bloques en varios clones de bloques que ya no se superpongan).
-   Los archivos de origen y de destino deben tener el mismo volumen ReFS.
-   Los archivos de origen y de destino deben tener la misma configuración de [**flujos de integridad**](file-attribute-constants.md) (es decir, los flujos de integridad deben estar habilitados en ambos archivos o deshabilitados en ambos archivos).
-   Si el archivo de origen es disperso, el archivo de destino también debe serlo.
-   La operación de clonación de bloques interrumpirá los bloqueos oportunistas compartidos (también conocidos como [bloqueos oportunistas de nivel 2](types-of-opportunistic-locks.md)).
-   El volumen ReFS debe tener el formato Windows Server 2016 y, si el clúster de conmutación por error de Windows está en uso, el nivel funcional de la agrupación en clústeres debe ser Windows Server 2016 o posterior en el momento del formato.

## <a name="example"></a>Ejemplo

Supongamos que tenemos dos archivos, X e y, donde cada archivo se compone de tres regiones distintas. Cada región de archivo se almacena en una región distinta del volumen. El sistema de archivos almacena la información a la que se hace referencia en una región de archivo a cada una de esas regiones de volumen:

![antes del clon](images/before-clone.png)

Ahora Supongamos que una aplicación emite una operación de clonación de bloques desde el archivo X, a través de las regiones del archivo a y B, al archivo Y en el desplazamiento donde E actualmente es. El siguiente estado del sistema de archivos daría como resultado:

![después del clon](images/after-clone.png)

Los datos de las regiones A y B se duplicaban de forma eficaz desde el archivo X al archivo Y modificando las asignaciones VCN a LCN en el volumen ReFS. No se leyeron las regiones de respaldo de las regiones A y B, ni las extensiones de disco que respaldan las regiones antiguas E y F sobrescribieron durante la operación.

Los archivos X e Y ahora comparten clústeres lógicos en el disco. Esto se refleja en los recuentos de referencias que se muestran en la tabla. El uso compartido da como resultado un consumo de menor capacidad de volumen que si las regiones A y B estuvieran duplicadas en el volumen subyacente.

Ahora, supongamos que la aplicación sobrescribe la región A en el archivo X. ReFS realiza una copia duplicada de un, que ahora llamaremos a G. ReFS y luego asigna G al archivo X y aplica la modificación. Esto asegura que el aislamiento entre los archivos se conserve. Los recuentos de referencias se actualizan correctamente:

![después de modificar la escritura](images/after-modifying-write.png)

Después de modificar la escritura, la región B todavía se comparte en el disco. Ten en cuenta que si la región A fuera mayor que un clúster, solo el clúster modificado se habría duplicado y el resto seguiría siendo compartido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**datos de extensiones DUPLICAdas \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[**\_elementos duplicados \_ \_ de extensiones de FSCTL en el \_ archivo**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
