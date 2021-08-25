---
description: La desfragmentación es el proceso de mover partes de archivos en un disco para desfragmentar archivos, es decir, el proceso de mover clústeres de archivos en un disco para que estén contiguos.
ms.assetid: 27ccaab7-ec89-489b-80dc-df9beb7969bc
title: Desfragmentación de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f04c0a3c961854b7e3ecab50d67db608178393113ca259b916db9623058e2f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696295"
---
# <a name="defragmenting-files"></a>Desfragmentación de archivos

Cuando un archivo se escribe en un disco, a veces el archivo no se puede escribir en clústeres contiguos. Los clústeres no contráguos ralentizan el proceso de lectura y escritura de un archivo. Entre más separados en un disco se encuentran los clústeres no contráguos, peor es el problema, debido al tiempo que se tarda en mover el jefe de lectura y escritura de una unidad de disco duro. Un archivo con clústeres no contados *está fragmentado.* Para optimizar los archivos para un acceso rápido, se puede desfragmentar un volumen.

*La* desfragmentación es el proceso de mover partes de archivos en un disco para desfragmentar archivos, es decir, el proceso de mover clústeres de archivos en un disco para que estén contiguos. Para obtener más información, consulte las secciones siguientes:

-   [Desfragmentación de un archivo](#defragmenting-a-file)
-   [Minimizar las interacciones entre la desfragmentación y las instantáneas](#minimizing-interactions-between-defragmentation-and-shadow-copies)
-   [Archivos, secuencias y tipos de flujo admitidos para la desfragmentación](#files-streams-and-stream-types-supported-for-defragmentation)

## <a name="defragmenting-a-file"></a>Desfragmentación de un archivo

En un sistema operativo simple de tarea única, el software de desfragmentación es la única tarea y no hay ningún otro proceso desde el que leer o escribir en el disco. Sin embargo, en un sistema operativo multitarea, algunos procesos pueden leer y escribir en una unidad de disco duro mientras otro proceso desfragmenta esa unidad de disco duro. El truco es evitar las escrituras en un archivo que se está desfragmentando sin detener el proceso de escritura durante mucho tiempo. Resolver este problema no es trivial, pero es posible.

Para permitir la desfragmentación sin necesidad de conocimientos detallados de una estructura de disco del sistema de archivos, se proporciona un conjunto de tres códigos de control. Los códigos de control proporcionan la siguiente funcionalidad:

-   Permitir que las aplicaciones busquen clústeres vacíos
-   Determinar la ubicación del disco de los clústeres de archivos
-   Movimiento de clústeres en un disco

Los códigos de control también controlan de forma transparente el problema de impedir y permitir que otros procesos lean y escriban en archivos durante los movimientos.

Estas operaciones se pueden realizar sin impedir que se ejecuten otros procesos. Sin embargo, los demás procesos tienen tiempos de respuesta más lentos mientras se desfragmenta una unidad de disco.

**Para desfragmentar un archivo**

1.  Use el código de control [**FSCTL \_ GET VOLUME \_ \_ BITMAP**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_volume_bitmap) para buscar un lugar en el volumen lo suficientemente grande como para aceptar un archivo completo.
    > [!Note]  
    > Si es necesario, mueva otros archivos para crear un lugar lo suficientemente grande. Idealmente, hay suficientes clústeres sin asignar después de la primera extensión del archivo que puede mover las extensiones posteriores al espacio después de la primera extensión.

     

2.  Use el código de control [**FSCTL \_ GET RETRIEVAL \_ \_ POINTERS**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers) para obtener un mapa del diseño actual del archivo en el disco.
3.  Recorrer la [**estructura BUFFER DE \_ PUNTEROS DE \_ RECUPERACIÓN**](/windows/desktop/api/WinIoCtl/ns-winioctl-retrieval_pointers_buffer) devuelta [**por LOS \_ PUNTEROS DE \_ \_ RECUPERACIÓN DE FSCTL GET**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_retrieval_pointers).
4.  Use el código de control [**\_ FSCTL MOVE \_ FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) para mover cada clúster a medida que se avanza en la estructura.
    > [!Note]  
    > Es posible que tenga que renovar el mapa de bits o la estructura de recuperación, o ambos en momentos diferentes a medida que otros procesos escriben en el disco.

     

Dos de las operaciones que se usan en el proceso de desfragmentación requieren un identificador para un volumen. Solo los administradores pueden obtener un identificador para un volumen, por lo que solo los administradores pueden desfragmentar un volumen. Una aplicación debe comprobar los derechos de un usuario que intenta ejecutar software de desfragmentación y no debe permitir que un usuario desfragmente un volumen si el usuario no tiene los derechos adecuados.

Al usar [**CreateFile para**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) abrir un directorio durante la desfragmentación de un volumen del sistema de archivos FAT o FAT32, especifique el valor de la máscara de acceso **\_ DE** LECTURA GENÉRICA. No especifique el valor de máscara de acceso **MAXIMUM \_ ALLOWED.** Si esto se hace, se deniega el acceso al directorio.

No intente mover clústeres asignados en un sistema de archivos NTFS que se extienda más allá del tamaño de archivo redondeado del clúster, ya que el resultado es un error.

Se pueden desfragmentar puntos, mapas de bits y listas de atributos en volúmenes del sistema de archivos NTFS, abrirse para lectura y sincronización, y asignar un nombre mediante el archivo *:**nombre:* sintaxis de *tipo;* por ejemplo, *dirname*:$i 30:$INDEX \_ ALLOCATION, *mrp*::$DATA, *mrp*::$REPARSE POINT y \_ *mrp*::$ATTRIBUTE \_ LIST.

Al desfragmentar volúmenes del sistema de archivos NTFS, se permite la desfragmentación de un clúster virtual más allá del tamaño de asignación de un archivo.

## <a name="minimizing-interactions-between-defragmentation-and-shadow-copies"></a>Minimizar las interacciones entre la desfragmentación y las instantáneas

Cuando sea posible, mueva los datos en bloques alineados entre sí en incrementos de 16 kilobytes (KB). Esto reduce la sobrecarga de copia en escritura cuando se habilitan las instantáneas, ya que aumenta el espacio de instantáneas y se reduce el rendimiento cuando se producen las condiciones siguientes:

-   El tamaño del bloque de solicitud de movimiento es menor o igual que 16 KB.
-   La diferencia de movimiento no está en incrementos de 16 KB.

La diferencia de movimiento es el número de bytes entre el inicio del bloque de origen y el inicio del bloque de destino. En otras palabras, un bloque que comienza en el desplazamiento X (en disco) se puede mover a un desplazamiento inicial Y si el valor absoluto de X menos Y es un múltiplo par de 16 KB. Por lo tanto, suponiendo que los clústeres de 4 KB, se optimizará un traslado del clúster 3 al clúster 27, pero no se moverá del clúster 18 al clúster 24. Tenga en cuenta que mod(3,4) = 3 = mod(27,4). Mod 4 se elige porque cuatro clústeres de 4 KB equivalen a 16 KB cada uno. Por lo tanto, un volumen con formato a un tamaño de clúster de 16 KB dará lugar a la optimización de todos los archivos de movimiento.

Para obtener más información sobre las instantáneas, [vea Servicio de instantáneas de volumen](/windows/desktop/VSS/about-the-volume-shadow-copy-service).

## <a name="files-streams-and-stream-types-supported-for-defragmentation"></a>Archivos, secuencias y tipos de flujo admitidos para la desfragmentación

Aunque la mayoría de los archivos se pueden mover mediante el código de control [**FSCTL \_ MOVE \_ FILE,**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) no todos se pueden mover. A continuación se muestra la lista de archivos, secuencias y tipos de secuencia (también denominados códigos de tipo de atributo) admitidos por **FSCTL \_ MOVE \_ FILE**. Otros archivos, secuencias y tipos de secuencia no son compatibles con **FSCTL \_ MOVE \_ FILE**.

Tipos de secuencia compatibles con cualquier archivo o directorio.

-   ::$DATA
-   ::$ATTRIBUTE \_ LIST
-   ::$REPARSE \_ POINT
-   ::$EA
-   ::$LOGGED DE \_ UTILIDAD \_

**Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP: **::$EA y ::$LOGGED UTILITY STREAM no se admiten antes \_ \_ de Windows 8 y Windows Server 2012

Tipos de flujo admitidos para cualquier directorio.

-   ::$BITMAP
-   ::$INDEX \_ ALLOCATION

A continuación se muestra el archivo del sistema, la secuencia y los tipos de secuencia admitidos por [**FSCTL \_ MOVE \_ FILE**](/windows/win32/api/winioctl/ni-winioctl-fsctl_move_file) en el formato *"nombre_de_archivo*:*nombre_secuencia*:$*typename".*

-   $MFT::$DATA
-   $MFT::$ATTRIBUTE \_ LIST
-   $MFT::$BITMAP
-   $AttrDef::$DATA
-   $AttrDef::$ATTRIBUTE \_ LIST
-   $Secure:$SDS:$DATA
-   $Secure::$ATTRIBUTE \_ LIST
-   $Secure:$SDH:$INDEX \_ ALLOCATION
-   $Secure:$SDH:$BITMAP
-   $Secure:$SII:$INDEX \_ ALLOCATION
-   $Secure:$SII:$BITMAP
-   $UpCase::$DATA
-   $UpCase::$ATTRIBUTE \_ LIST
-   $Extend:$I 30:$INDEX \_ ALLOCATION
-   $Extend::$ATTRIBUTE \_ LIST
-   $Extend:$I 30:$BITMAP
-   $Extend \\ $UsnJrnl:$J:$DATA
-   $Extend \\ $UsnJrnl::$ATTRIBUTE \_ LIST
-   $Extend \\ $UsnJrnl:$Max:$DATA
-   $Extend \\ $Quota:$Q:$INDEX \_ ALLOCATION
-   $Extend \\ $Quota::$ATTRIBUTE \_ LIST
-   $Extend \\ $Quota:$Q:$BITMAP
-   $Extend \\ $Quota:$O:$INDEX \_ ALLOCATION
-   $Extend \\ $Quota:$O:$BITMAP
-   $Extend \\ $ObjId:$O:$INDEX \_ ALLOCATION
-   $Extend \\ $ObjId::$ATTRIBUTE \_ LIST
-   $Extend \\ $ObjId:$O:$BITMAP
-   $Extend \\ $Reparse:$R:$INDEX \_ ALLOCATION
-   $Extend \\ $Reparse::$ATTRIBUTE \_ LIST
-   $Extend \\ $Reparse:$R:$BITMAP
-   $Extend \\ $RmMetadata:$I 30:$INDEX \_ ALLOCATION
-   $Extend \\ $RmMetadata:$I 30:$BITMAP
-   $Extend \\ $RmMetadata::$ATTRIBUTE \_ LIST
-   $Extend \\ $RmMetadata \\ $Repair::$DATA
-   $Extend \\ $RmMetadata \\ $Repair::$ATTRIBUTE \_ LIST
-   $Extend $RmMetadata \\ \\ $Repair:$Config:$DATA
-   $Extend $RmMetadata \\ \\ $Txf:$I 30:$INDEX \_ ALLOCATION
-   $Extend $RmMetadata \\ \\ $Txf::$ATTRIBUTE \_ LIST
-   $Extend $RmMetadata \\ \\ $Txf:$I 30:$BITMAP
-   $Extend $RmMetadata \\ \\ $Txf:$TXF \_ DATA:$LOGGED \_ UTILITY \_ STREAM
-   $Extend $RmMetadata \\ \\ $TxfLog:$I 30:$INDEX \_ ALLOCATION
-   $Extend $RmMetadata \\ \\ $TxfLog::$ATTRIBUTE \_ LIST
-   $Extend \\ $RmMetadata \\ $TxfLog:$I 30:$BITMAP
-   $Extend $RmMetadata \\ \\ $TxfLog \\ $Tops::$DATA
-   $Extend \\ $RmMetadata $TxfLog \\ \\ $Tops::$ATTRIBUTE \_ LIST
-   $Extend $RmMetadata \\ \\ $TxfLog \\ $Tops:$T:$DATA
-   $Extend $RmMetadata \\ \\ $TxfLog \\ $TxfLog.blf::$DATA
-   $Extend \\ $RmMetadata \\ $TxfLog \\ $TxfLog.blf::$ATTRIBUTE \_ LIST

 

 
