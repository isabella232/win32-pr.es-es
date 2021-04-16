---
description: Hay muchas razones por las que un solicitante no debe ser capaz de restaurar archivos desde un medio de copia de seguridad a su ubicación original.
ms.assetid: 2a9cfd99-5a2c-4c0c-98ff-11c745298cda
title: Trabajar con ubicaciones alternativas durante la restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1338d76f98153ccb388e86e738b408c03dd253b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696434"
---
# <a name="working-with-alternate-locations-during-restore"></a>Trabajar con ubicaciones alternativas durante la restauración

Hay muchas razones por las que un solicitante no debe ser capaz de restaurar archivos desde un medio de copia de seguridad a su ubicación original. Por ejemplo, un método o un destino de restauración puede requerir una restauración de este tipo, o la ubicación de restauración actual puede estar ocupada y sin escritura.

Para controlar estos casos, un escritor puede haber definido una [*asignación de ubicación alternativa*](vssgloss-a.md), un destino de restauración no estándar que se usará para circunstancias especiales.

El término asignación de ubicación alternativa, tal y como se usa con VSS, no se debe confundir con el término [*ruta de acceso alternativa*](vssgloss-a.md). Las asignaciones de ubicación alternativas solo se usan durante las operaciones de restauración y hacen referencia a un destino alternativo para las operaciones de restauración. Las rutas de acceso alternativas solo se usan durante las operaciones de copia de seguridad y hacen referencia a un origen alternativo del que se va a realizar la copia de seguridad.

Para usar asignaciones de ubicación alternativas durante la restauración, un solicitante haría lo siguiente (normalmente después de la generación de un evento de [**prerestauración**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) ):

1.  Mediante el uso de una instancia de la interfaz [**IVssExamineWriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtenida al recuperar un escritor almacenado, un solicitante usa el método [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) para obtener las asignaciones de ubicación alternativas de un escritor como instancias de la interfaz [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) .

    > [!Note]  
    > El solicitante usa [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), no [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). El primero devuelve las asignaciones de ubicación alternativas disponibles para que las use un solicitante. Esta última se usa para indicar las asignaciones de ubicación alternativas utilizadas realmente por un solicitante.

     

2.  La llamada a [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) devuelve una instancia de la interfaz [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) . Esta instancia contiene información de conjunto de archivos, una ruta de acceso especificada por [**IVssWMFiledesc:: GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), una especificación de archivo devuelta a través de [**IVssWMFiledesc:: GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)y una marca de recursividad obtenida de [**IVssWMFiledesc:: GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive), que coincide con uno de los conjuntos de archivos agregados (mediante [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)) a uno de los componentes

    El valor devuelto por [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) es la asignación de ubicación alternativa para este conjunto de archivos.

3.  Las asignaciones de ubicación alternativas no contienen información de componentes, por lo que será necesario comparar la información del conjunto de archivos (ruta de acceso, especificación de archivo y marca de recursividad) obtenida llamando a [**IVssExamineWriterMetadata:: GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) a la que contengan los componentes del escritor.

    Para encontrar esta información, puede recorrer en iteración los componentes del escritor y llamar a [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) para obtener una instancia de la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) y usar [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) para obtener una instancia de [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) que contiene la información del conjunto de archivos de componentes.

    Cuando la información de conjunto de archivos devuelta por la instancia de [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) obtenida de [**IVssExamineWriterMetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) y [**IVssWMComponent:: GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) coincide con la que se obtiene de la instancia de **IVssWMFiledesc** derivada de [**IVssWMFiledesc:: GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation), se ha encontrado el componente que administra los archivos con la asignación de ubicación alternativa específica.

4.  Una vez localizado el componente, el solicitante puede determinar las condiciones en las que se debe usar una asignación de ubicación alternativa haciendo lo siguiente:

    -   Examinar el método de restauración del componente, que se obtiene llamando a [**IVssExamineWriterMetadata:: GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).
    -   Comprobando si un destino de restauración invalida el método de restauración mediante una llamada a [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget).

        Si el componente que se encuentra en el documento de metadatos del escritor se [*incluyó explícitamente*](vssgloss-e.md) en la copia de seguridad, la instancia de la interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) se corresponderá con ese componente. Si el componente se [*incluyó implícitamente*](vssgloss-i.md) en la copia de seguridad, la instancia de **IVssComponent** se corresponderá con el componente que define el conjunto de componentes del que el componente del documento de metadatos del escritor es un subcomponente.

5.  Con esta información, el solicitante puede determinar cada componente en función de si necesita restaurar un determinado conjunto de archivos de un componente determinado a un destino definido por la asignación de ubicación alternativa.

6.  Cuando se usa una asignación de ubicación alternativa, el solicitante respeta el descriptor de archivo del conjunto de archivos y la marca recursiva, y utiliza la ruta de acceso proporcionada por la asignación de ubicación alternativa.

    El solicitante indica que ha usado una asignación de ubicación alternativa durante una operación de restauración mediante una llamada a la función [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) con la información de ubicación predeterminada del conjunto de archivos, el destino de restauración alternativo usado y un nombre de componente.

    Si el conjunto de archivos lo ha administrado un componente que se incluyó explícitamente en la copia de seguridad, se usará ese nombre de componente. Si el conjunto de archivos lo ha administrado un componente que se incluyó implícitamente en la copia de seguridad, el nombre utilizado será el del componente que define el conjunto de componentes del que el componente que administra el conjunto de archivos es un subcomponente.

Los escritores comprueban si los conjuntos de archivos de uno de sus componentes se restauraron en una asignación de ubicación alternativa mediante una llamada a [**IVssComponent:: GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).

 

 



