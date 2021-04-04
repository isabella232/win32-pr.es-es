---
description: La desfragmentación es el proceso por el que se mueven partes de los archivos en un disco para desfragmentar archivos, es decir, el proceso de mover los clústeres de archivos de un disco para que sean contiguos.
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: Desfragmentar archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b2d079f58ec98f320356a477531616788f84ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908608"
---
# <a name="defragmenting-files"></a>Desfragmentar archivos

Cuando un archivo se escribe en un disco, a veces el archivo no se puede escribir en clústeres contiguos. Los clústeres no contiguos ralentizan el proceso de lectura y escritura de un archivo. Además, en un disco los clústeres no contiguos, peor es el problema, debido al tiempo que se tarda en trasladar el encabezado de lectura/escritura de una unidad de disco duro. Se *fragmenta* un archivo con clústeres no contiguos. Para optimizar los archivos para un acceso rápido, se puede desfragmentar un volumen.

La *desfragmentación* es el proceso por el que se mueven partes de los archivos en un disco para desfragmentar archivos, es decir, el proceso de mover los clústeres de archivos de un disco para que sean contiguos. Para obtener más información, consulte las secciones siguientes:

-   [Desfragmentar un archivo](#defragmenting-a-file)
-   [Minimizar las interacciones entre la desfragmentación y las instantáneas](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [Archivos, secuencias y tipos de secuencia admitidos para la desfragmentación](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a>Desfragmentar un archivo

En un sistema operativo simple con una sola tarea, el software de desfragmentación es la única tarea y no hay ningún otro proceso para leer o escribir en el disco. Sin embargo, en un sistema operativo multitarea, algunos procesos pueden leer y escribir en una unidad de disco duro mientras otro proceso está desfragmentando esa unidad de disco duro. El truco es evitar la escritura en un archivo que se está desfragmentando sin detener el proceso de escritura durante mucho tiempo. La solución de este problema no es trivial, pero es posible.

Para permitir la desfragmentación sin necesidad de conocer detalladamente la estructura del disco del sistema de archivos, se proporciona un conjunto de tres códigos de control. Los códigos de control proporcionan la siguiente funcionalidad:

-   Habilitar aplicaciones para buscar clústeres vacíos
-   Determinar la ubicación del disco de los clústeres de archivos
-   Traslado de clústeres en un disco

Los códigos de control también controlan de forma transparente el problema de inhibir y permitir que otros procesos lean y escriban archivos durante los movimientos.

Estas operaciones se pueden realizar sin impedir que otros procesos se ejecuten. Sin embargo, los demás procesos tienen tiempos de respuesta más lentos mientras se desfragmenta una unidad de disco.

**Para desfragmentar un archivo**

1.  Use el código de control de [**\_ mapa de \_ \_ bits de volumen de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) para buscar un lugar en el volumen que sea lo suficientemente grande como para aceptar un archivo completo.
    > [!Note]  
    > Si es necesario, mueva otros archivos para que sea lo suficientemente grande. Idealmente, hay suficientes clústeres sin asignar después de la primera extensión del archivo que puede trasladar las extensiones posteriores en el espacio después de la primera extensión.

     

2.  Use el código de control de los [**\_ \_ \_ punteros get de recuperación de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) para obtener un mapa del diseño actual del archivo en el disco.
3.  Recorra la estructura de búfer de los [**\_ \_ punteros de recuperación**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer) devuelta por [**FSCTL \_ obtener \_ \_ punteros de recuperación**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers).
4.  Use el código de control de [**\_ \_ archivo FSCTL Move**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) para desplazar cada clúster a medida que se recorre la estructura.
    > [!Note]  
    > Es posible que tenga que renovar el mapa de bits o la estructura de recuperación, o ambos en diferentes ocasiones a medida que otros procesos escriben en el disco.

     

Dos de las operaciones que se usan en el proceso de desfragmentación requieren un identificador a un volumen. Solo los administradores pueden obtener un identificador de un volumen, por lo que solo los administradores pueden desfragmentar un volumen. Una aplicación debe comprobar los derechos de un usuario que intenta ejecutar el software de desfragmentación y no debe permitir que un usuario desfragmente un volumen si el usuario no tiene los derechos adecuados.

Al usar [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir un directorio durante la desfragmentación de un volumen del sistema de archivos FAT o FAT32, especifique el valor de máscara de acceso de **\_ lectura genérico** . No especifique el valor de máscara de acceso **máximo \_ permitido** . Si se hace, se deniega el acceso al directorio.

No intente trasladar los clústeres asignados en un sistema de archivos NTFS que supere el tamaño de archivo redondeado del clúster, ya que el resultado es un error.

Los puntos de análisis, mapas de bits y listas de atributos de los volúmenes del sistema de archivos NTFS se pueden desfragmentar, abrir para leer y sincronizar y denominar con la sintaxis *File*:*Name*:*Type* ; por ejemplo, *dirname*: $i 30: $index \_ Allocation, *MRP*:: $DATA, *MRP*:: $REPARSE \_ Point y *MRP*:: $Attribute \_ List.

Al desfragmentar volúmenes del sistema de archivos NTFS, se permite desfragmentar un clúster virtual más allá del tamaño de asignación de un archivo.

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a>Minimizar las interacciones entre la desfragmentación y las instantáneas

Cuando sea posible, mueva los datos en bloques alineados entre sí en incrementos de 16 kilobytes (KB). Esto reduce la sobrecarga de copia por escritura cuando se habilitan las instantáneas, ya que el espacio de la instantánea aumenta y el rendimiento se reduce cuando se producen las condiciones siguientes:

-   El tamaño del bloque de solicitud de movimiento es menor o igual que 16 KB.
-   La diferencia de desplazamiento no se encuentra en incrementos de 16 KB.

La diferencia de movimiento es el número de bytes entre el inicio del bloque de origen y el inicio del bloque de destino. En otras palabras, un bloque que empieza en el desplazamiento X (en disco) se puede pasar a un desplazamiento inicial Y si el valor absoluto de X menos Y es un múltiplo par de 16 KB. Por lo tanto, suponiendo que los clústeres de 4 KB, se optimizará el traslado del clúster 3 al clúster 27, pero no se realizará un cambio del clúster 18 al clúster 24. Tenga en cuenta que mod (3, 4) = 3 = MOD (27, 4). Mod 4 se elige porque cuatro clústeres de 4 KB cada uno es equivalente a 16 KB. Por lo tanto, un volumen formateado con un tamaño de clúster de 16 KB dará como resultado la optimización de todos los archivos de movimiento.

Para obtener más información sobre las instantáneas, vea [servicio de instantáneas de volumen](/windows/desktop/VSS/about-the-volume-shadow-copy-service).

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a>Archivos, secuencias y tipos de secuencia admitidos para la desfragmentación

Aunque la mayoría de los archivos se pueden trasladar con el código de control de [**\_ \_ archivos de movimiento de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) , no todos se pueden trasladar. A continuación se muestra la lista de archivos, secuencias y tipos de secuencias (también denominados códigos de tipo de atributo) que admite el **\_ \_ archivo de movimiento de FSCTL**. Otros archivos, secuencias y tipos de secuencia no son compatibles con **el \_ \_ archivo de movimiento FSCTL**.

Tipos de secuencia compatibles con cualquier archivo o directorio.

-   :: $DATA
-   :: $ATTRIBUTE \_ lista
-   :: $REPARSE \_ punto
-   :: $EA
-   :: $LOGGED \_ secuencia de la utilidad \_

* * Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP: * *:: $EA y:: $LOGGED \_ secuencia de la utilidad \_ no se admiten antes de Windows 8 y windows Server 2012

Tipos de secuencia compatibles con cualquier directorio.

-   :: $BITMAP
-   :: $INDEX \_ asignación

A continuación se muestran los tipos de archivo, secuencia y secuencia del sistema compatibles con el [**\_ \_ archivo de movimiento de FSCTL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) en formato "*filename*:*nombredeflujo*: $*TypeName*".

-   $MFT:: $DATA
-   $MFT:: $ATTRIBUTE \_ lista
-   $MFT:: $BITMAP
-   $AttrDef:: $DATA
-   $AttrDef:: $ATTRIBUTE \_ lista
-   $Secure: $SDS: $DATA
-   $Secure:: $ATTRIBUTE \_ lista
-   $Secure: $SDH: asignación de $INDEX \_
-   $Secure: $SDH: $BITMAP
-   $Secure: $SII: asignación de $INDEX \_
-   $Secure: $SII: $BITMAP
-   $UpCase:: $DATA
-   $UpCase:: $ATTRIBUTE \_ lista
-   $Extend: $I 30: asignación de $INDEX \_
-   $Extend:: $ATTRIBUTE \_ lista
-   $Extend: $I 30: $BITMAP
-   $Extend \\ $UsnJrnl: $J: $Data
-   $Extend \\ $UsnJrnl:: $Attribute \_ List
-   $Extend \\ $UsnJrnl: $Max: $Data
-   $Extend \\ $quota: $Q: $index \_ asignación
-   $Extend \\ $quota:: $Attribute \_ List
-   $Extend \\ $quota: $Q: $Bitmap
-   $Extend \\ $quota: $O: $index \_ asignación
-   $Extend \\ $quota: $O: $Bitmap
-   $Extend \\ $ObjId: $O: $index \_ asignación
-   $Extend \\ $ObjId:: $Attribute \_ List
-   $Extend \\ $ObjId: $O: $Bitmap
-   $Extend \\ $Reparse: $R: $index \_ asignación
-   $Extend \\ $Reparse:: $Attribute \_ List
-   $Extend \\ $Reparse: $R: $Bitmap
-   $Extend \\ $RmMetadata: $I 30: $index \_ asignación
-   $Extend \\ $RmMetadata: $I 30: $Bitmap
-   $Extend \\ $RmMetadata:: $Attribute \_ List
-   $Extend \\ $RmMetadata \\ $Repair:: $Data
-   $Extend \\ $RmMetadata \\ $Repair:: $Attribute \_ List
-   $Extend \\ $RmMetadata \\ $Repair: $Config: $Data
-   $Extend \\ $RmMetadata \\ $Txf: $I 30: $index \_ asignación
-   $Extend \\ $RmMetadata \\ $TxF:: $Attribute \_ List
-   $Extend \\ $RmMetadata \\ $Txf: $I 30: $Bitmap
-   $Extend \\ $RmMetadata \\ $Txf: $TxF \_ datos: $logged \_ \_ secuencia de la utilidad
-   $Extend \\ $RmMetadata \\ $TxfLog: $I 30: $index \_ asignación
-   $Extend \\ $RmMetadata \\ $TxfLog:: $Attribute \_ List
-   $Extend \\ $RmMetadata \\ $TxfLog: $I 30: $Bitmap
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops:: $Data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $Tops:: $Attribute \_ List
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $tops: $T: $Data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. blf:: $Data
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog. blf:: $Attribute \_ List

 

 
