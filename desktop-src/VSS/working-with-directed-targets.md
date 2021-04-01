---
description: El mecanismo de destino dirigido permite a los escritores reasignar archivos en el momento de la restauración.
ms.assetid: c0b4ab26-2bb6-4b0f-b837-01057983b49b
title: Trabajar con destinos dirigidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bd2e15ec873b87030a2d01be69d2c3e5f95a193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082134"
---
# <a name="working-with-directed-targets"></a>Trabajar con destinos dirigidos

El mecanismo de [*destino dirigido*](vssgloss-d.md) permite a los escritores reasignar archivos en el momento de la restauración. Esto permite a los escritores hacer lo siguiente:

-   Especifique las nuevas ubicaciones de destino (análogas a la variable [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget)) del solicitante.
-   Recupere espacio en disco restaurando solo las partes necesarias de un archivo en el disco, especialmente cuando se realizó una copia de seguridad de un archivo mediante el mecanismo de [*archivos parciales*](vssgloss-p.md) .
-   Cambie el formato de archivo para satisfacer las necesidades actuales.

Cualquier archivo que se va a usar con una operación de destino dirigida debe tener un [*destino de restauración*](vssgloss-r.md) de VSS \_ RT \_ dirigido.

Una vez que se ha establecido que un solicitante puede admitir una operación de destino dirigida, un escritor (mientras se controla el evento de [**prerestauración**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ) usa [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) para la instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente al componente que administra el archivo (o el componente que define el conjunto de componentes que contiene el archivo) para definir cómo se va a reasignar el archivo en la restauración.

En el uso de [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget), los escritores especifican el nombre de archivo y la ruta de acceso utilizados para realizar una copia de seguridad del archivo, el nombre de archivo y la ruta de acceso de su destino de restauración (estos valores pueden ser los mismos que el nombre de archivo y la ruta de acceso originales) y los intervalos de archivos de origen y de destino.

Al igual que con las operaciones de archivo parcial, las listas de intervalos son pares de desplazamientos en el archivo del que se va a hacer una copia de seguridad (en bytes) y la longitud de la sección que se va a restaurar (en bytes), el desplazamiento y la longitud que se separan con dos puntosy cada par separado por una coma: *Offset1 ***:**_length1 (_* Cada valor es un entero de 64 bits en formato hexadecimal o decimal.

Si un escritor necesita usar el mecanismo de destino dirigido para que el solicitante restaure un archivo en una nueva ubicación, habría llamado a [**IVssComponent:: AddDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddirectedtarget) con el nombre de archivo y la ruta de acceso originales, y el nuevo nombre de archivo y ruta de acceso, y especificar los intervalos de destino de origen con un desplazamiento de cero y una longitud igual a la del tamaño de archivo completo.

Por ejemplo, si un escritor necesita tener un archivo 200 000, C: \\ WriterData \\ index. dat, restaurado como c: \\ WriterData \\ OldIndex. dat, la cadena de rango de origen y de destino sería "**0:204880**".

Para reasignar un archivo grande de copia de seguridad parcial, el solicitante usaría el intervalo de origen usado para hacer una copia de seguridad del archivo y un intervalo de destino que reducirá el tamaño del archivo. La información del intervalo de origen se puede obtener mediante [**IVssComponent:: GetPartialFile**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpartialfile) para la instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente al componente que administra el archivo (o el componente que define el conjunto de componentes que contiene el archivo).

Si el archivo de copia de seguridad parcial era inicialmente un archivo grande cuyo encabezado, bytes 64-512, contiene un recuento de registros y otra información actualizada con frecuencia, y cuyos datos más recientes se encuentran en los últimos 65536 bytes del archivo (bytes 0x1239E8577A a 0x1239E7577A, un escritor podría especificar una lista de intervalos de origen como la cadena "**64:448, 0x1239E8577A: 65536**".

Si el escritor desea reasignar el archivo restaurado para que contenga solo el encabezado y los datos más recientes, la lista de intervalos podría ser la cadena "**0:488488:65536**".

Antes de realizar realmente una operación de restauración, un solicitante debe comprobar si algún archivo requiere compatibilidad con destino dirigido.

Para ello, el solicitante primero recorre en iteración los escritores con componentes almacenados en su documento de componentes de copia de seguridad mediante [**IVssBackupComponents:: GetWriterComponentsCount**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponentscount) y [**Ivssbackupcomponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents).

A continuación, se usa la interfaz [**IVssBackupComponents:: GetWriterComponents**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getwritercomponents) para devolver instancias de la interfaz [**IVssWriterComponentsExt**](/windows/win32/api/vsbackup/nl-vsbackup-ivsswritercomponentsext) , que proporciona los métodos [**IVssWriterComponentsExt:: getComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponent) y [**IVssWriterComponentsExt:: GetComponentCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswritercomponents-getcomponentcount) que permiten al solicitante obtener instancias de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) .

Esto permite a un solicitante obtener candidatos de destino dirigidos mediante [**IVssComponent:: GetDirectedTargetCount**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtargetcount) y [**IVssComponent:: GetDirectedTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getdirectedtarget) para la instancia de [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) correspondiente al componente que administra el archivo (o el componente que define el conjunto de componentes que contiene el archivo).

 

 
