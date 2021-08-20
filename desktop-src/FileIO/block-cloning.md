---
description: Una operación de clonación de bloques indica al sistema de archivos que copie un intervalo de bytes de archivo en nombre de una aplicación.
ms.assetid: E18E8D79-3985-40B8-A4C5-A73A21E5C527
title: Clonación de bloques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7d94afdb9b630f501de4baee0b690715f42d057a157f31b142c231e0a03f9f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582670"
---
# <a name="block-cloning"></a>Clonación de bloques

Una *operación de clonación* de bloques indica al sistema de archivos que copie un intervalo de bytes de archivo en nombre de una aplicación. El archivo de destino puede ser igual o diferente del archivo de origen.

Un sistema de archivos administra [](clusters-and-extents.md)las asignaciones de clústeres y extensiones y puede realizar la copia modificando el número de clúster virtual (VCN) a las asignaciones de número de clúster lógico (LCN) como una operación de metadatos de bajo costo, en lugar de leer y escribir los datos de archivo subyacentes. Esto permite que la copia se complete más rápido y genera menos E/S en el almacenamiento subyacente. Además, ahora varios archivos pueden compartir clústeres lógicos después del clon de bloque, lo que ahorra capacidad al no almacenar clústeres idénticos varias veces en el disco.

Una operación de clonación de bloques no interrumpirá el aislamiento proporcionado entre los archivos. Una vez completado un clon de bloque, las escrituras en el archivo de origen no aparecen en el destino o viceversa.

La clonación de bloques solo está disponible en el [tipo de sistema de archivos ReFS](/windows/desktop/w8cookbook/resilient-file-system--refs-) a partir de Windows Server 2016.

## <a name="block-cloning-on-refs"></a>Bloquear la clonación en ReFS

ReFS en Windows Server 2016 implementa la clonación de bloques mediante la remapping de clústeres lógicos (es decir, ubicaciones físicas en un volumen) de la región de origen a la región de destino. A continuación, usa un mecanismo de asignación en escritura para garantizar el aislamiento entre esas regiones. Las regiones de origen y de destino pueden estar en los mismos archivos o en diferentes.

Esta implementación requiere que los desplazamientos de archivo inicial y final se alineen con los límites del clúster. En ReFS en Windows Server 2016, los clústeres tienen un tamaño de 4 KB de forma predeterminada, pero opcionalmente se pueden establecer en 64 KB. El tamaño del clúster es un parámetro de todo el volumen establecido en tiempo de formato.

## <a name="restrictions-and-remarks"></a>Restricciones y comentarios

-   Las regiones de origen y destino deben comenzar y finalizar en un límite de clúster.
-   La región clonada debe ser inferior a 4 GB de longitud.
-   La región de destino no debe extenderse más allá del final del archivo. Si la aplicación desea extender el destino con datos clonados, primero debe llamar a [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).
-   Si las regiones de origen y destino están en el mismo archivo, no deben superponerse. (La aplicación puede continuar dividiendo la operación de clonación de bloques en varios clones de bloque que ya no se superponen).
-   Los archivos de origen y de destino deben tener el mismo volumen ReFS.
-   Los archivos de origen y [](file-attribute-constants.md) de destino deben tener la misma configuración de Secuencias integridad (es decir, La integridad Secuencias debe estar habilitada en ambos archivos o deshabilitarse en ambos archivos).
-   Si el archivo de origen es disperso, el archivo de destino también debe serlo.
-   La operación de clonación de bloques interrumpirá los bloqueos oportunistas compartidos (también conocidos como bloqueos [oportunistas de nivel 2).](types-of-opportunistic-locks.md)
-   El volumen ReFS debe tener el formato Windows Server 2016 y, si Windows Clústeres de conmutación por error está en uso, el nivel funcional de agrupación en clústeres debe estar Windows Server 2016 o posterior en tiempo de formato.

## <a name="example"></a>Ejemplo

Supongamos que tenemos dos archivos, X e Y, donde cada archivo se compone de tres regiones distintas. Cada región de archivo se almacena en una región distinta del volumen. El sistema de archivos almacena el conocimiento de que se hace referencia a cada una de esas regiones de volumen en una región de archivo:

![antes de clonar](images/before-clone.png)

Ahora supongamos que una aplicación emite una operación de clonación de bloques del archivo X, a través de las regiones de archivo A y B, al archivo Y en el desplazamiento donde está actualmente E. Se produciría el siguiente estado del sistema de archivos:

![después de clonar](images/after-clone.png)

Los datos de las regiones A y B se duplicaron eficazmente del archivo X al archivo Y mediante la modificación de las asignaciones de VCN a LCN dentro del volumen ReFS. Las extensiones de disco de las regiones de respaldo A y B no se leyeron ni se sobrescribiron las extensiones de disco que estaban detrás de las regiones antiguas E y F durante la operación.

Los archivos X e Y ahora comparten clústeres lógicos en el disco. Esto se refleja en los recuentos de referencias que se muestran en la tabla. El uso compartido da como resultado un consumo de capacidad de volumen menor que si las regiones A y B estuvieran duplicadas en el volumen subyacente.

Ahora, supongamos que la aplicación sobrescribe la región A en el archivo X. ReFS realiza una copia duplicada de A, a la que ahora llamaremos G. ReFS luego asigna G en el archivo X y aplica la modificación. Esto asegura que el aislamiento entre los archivos se conserve. Los recuentos de referencias se actualizan correctamente:

![después de modificar la escritura](images/after-modifying-write.png)

Después de modificar la escritura, la región B todavía se comparte en el disco. Ten en cuenta que si la región A fuera mayor que un clúster, solo el clúster modificado se habría duplicado y el resto seguiría siendo compartido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**DATOS \_ DE EXTENSIONES DUPLICADAS \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-duplicate_extents_data)
</dt> <dt>

[**EXTENSIONES DUPLICADAS DE FSCTL \_ \_ EN EL \_ \_ ARCHIVO**](/windows/win32/api/winioctl/ni-winioctl-fsctl_duplicate_extents_to_file)
</dt> </dl>

 

 
