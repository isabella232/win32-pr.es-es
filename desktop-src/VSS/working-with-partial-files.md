---
description: A veces resulta útil realizar copias de seguridad y restaurar solo secciones de archivos. VSS proporciona mecanismos de archivos parciales que, si los solicitan, permiten a los escritores especificar copias de seguridad de archivos parciales y restauraciones.
ms.assetid: 02b74a4e-d69f-4eeb-866a-3399598b7035
title: Trabajar con archivos parciales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7194f01df11f6c0e368941e17ef6ab1620b17f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696430"
---
# <a name="working-with-partial-files"></a>Trabajar con archivos parciales

A veces resulta útil realizar copias de seguridad y restaurar solo secciones de archivos. VSS proporciona mecanismos de [*archivos parciales*](vssgloss-p.md) que, si los solicitan, permiten a los escritores especificar copias de seguridad de archivos parciales y restauraciones.

Las operaciones de archivos parciales suelen ser de mayor uso para los escritores que mantienen archivos muy grandes, solo una pequeña fracción de los cambios entre las operaciones de copia de seguridad. Este es el caso, a menudo resulta útil copiar solo la sección que cambió al medio de copia de seguridad. Por este motivo, las operaciones de archivos parciales normalmente se usan, pero no exclusivamente, para admitir operaciones de copia de seguridad y restauración incrementales.

Si un escritor desea implementar una operación de archivo parcial, usa [**CVssWriter:: IsPartialFileSupportEnabled**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-ispartialfilesupportenabled) para determinar si el solicitante con el que trabaja admite la operación.

Si el solicitante admite operaciones de archivo parciales y agrega el componente que administra el archivo (o el componente que define el conjunto de componentes que contiene el archivo) al documento componentes de copia de seguridad, un escritor indica qué secciones del archivo se deben guardar (normalmente al controlar un evento [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) o [*postsnapshot*](vssgloss-p.md) ) mediante una llamada a [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

Además de una ruta de acceso y un nombre de archivo, el escritor proporciona la información de metadatos opcional del intervalo a [**IVssComponent:: AddPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-addpartialfile).

La información del intervalo se proporciona como una cadena que contiene una de las siguientes opciones:

-   Pares de desplazamientos en el archivo del que se va a hacer una copia de seguridad (en bytes) y la longitud de la sección de la que se va a hacer una copia de seguridad (en bytes), el desplazamiento y la longitud separados por dos puntos, y cada par separado por una coma, por ejemplo, *Offset1 ***:**_length1 (_*_,_* * Offset2 ***:**_length2 (_.

    Cada valor es un entero de 64 bits (en formato hexadecimal o decimal) que especifica un desplazamiento de bytes y una longitud en bytes, respectivamente.

-   La ruta de acceso completa, incluido el nombre de archivo, en el sistema actual de un archivo de intervalos binarios que contiene lo siguiente:
    -   El número (expresado como un entero de 64 bits) de distintos intervalos de archivos contenidos en el archivo.
    -   Cada intervalo expresado como un par de enteros de 64 bits: el primer miembro del par es el desplazamiento en el archivo del que se realiza la copia de seguridad (en bytes) y el segundo miembro es la longitud de los datos de los que se va a hacer una copia de seguridad (en bytes).

Si un sistema de escritura usa un archivo de rangos para especificar una operación de archivo parcial, un solicitante debe garantizar que se realice una copia de seguridad de este archivo (aunque el archivo no sea necesariamente parte del conjunto de copia de seguridad predeterminado) o que la información de los intervalos se conserve en el medio de copia de seguridad de otra manera. Si no se realiza una copia de seguridad de la información del archivo de intervalos, no será posible restaurar el archivo de copia de seguridad parcial.

El escritor también puede Agregar una cadena que contiene metadatos. Estos metadatos pueden estar en un formato específico del escritor porque está diseñado para permitir que el escritor valide las restauraciones futuras.

Con esta información, un solicitante auxiliar puede realizar una copia de seguridad de archivos parcial.

Como ejemplo, considere un archivo grande cuyo encabezado (bytes 64-512) contiene un recuento de registros y otra información actualizada con frecuencia, y cuyos datos más recientes se van a encontrar en los últimos 65536 bytes del archivo, bytes 0x1239E8577A a 0x1239E7577A.

Un escritor puede especificar una lista de intervalos como la cadena "**64:448, 0x1239E8577A: 65536**".

En la restauración y antes de realizar realmente una operación de restauración, un solicitante debe comprobar si algún archivo requiere compatibilidad con archivos parciales.

Para ello, el solicitante primero recorre en iteración los escritores con componentes almacenados en su documento de componentes de copia de seguridad mediante [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) y [**Ivssbackupcomponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

La interfaz [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) se usa para devolver instancias de la interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) , que proporcionan [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) y [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount), que permiten al solicitante obtener instancias de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Esto permite que un solicitante obtenga información sobre los archivos de copia de seguridad parcial para participar en una restauración mediante [**IVssComponent:: GetPartialFileCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfilecount) y [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) para la instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente al componente que administra el archivo (o el componente que define el conjunto de componentes que contiene el archivo).

Si la operación de archivo parcial se controló mediante un archivo de rangos, ese archivo debe restaurarse antes de copiar los datos de nuevo en el disco. Puede ocurrir que el solicitante necesite volver a copiar el archivo de intervalos en una nueva ubicación en el disco. En este caso, indica que se ha hecho a través de [**IVssBackupComponents:: SetRangesFilePath**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrangesfilepath).

A continuación, el solicitante continúa para copiar los datos en las ubicaciones adecuadas del destino de restauración ya en el disco.

Un escritor (mientras se controla un evento [**Postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) ) examinando [**IVssComponent:: GetFileRestoreStatus**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getfilerestorestatus) para los archivos indicados por [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile), determina si la operación de archivo parcial se realizó correctamente. El escritor siempre debe intentar comprobar la corrección de esta restauración con la información de desplazamiento y los metadatos incluidos en el documento componentes de copia de seguridad.

Si el solicitante ha tenido que restaurar el archivo de intervalos en una nueva ubicación, VSS actualizará esta información para que la ruta de acceso devuelta por [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) sea correcta.

 

 
