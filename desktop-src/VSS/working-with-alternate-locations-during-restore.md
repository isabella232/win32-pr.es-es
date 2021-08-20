---
description: Hay muchas razones por las que un solicitante no debe, o no, poder restaurar archivos desde medios de copia de seguridad a su ubicación original.
ms.assetid: 2a9cfd99-5a2c-4c0c-98ff-11c745298cda
title: Trabajar con ubicaciones alternativas durante la restauración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 907732c7b4b97668f1a317f9e03c3ea35bdec9618ff0e3e3c1a2f1e319eb19fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056153"
---
# <a name="working-with-alternate-locations-during-restore"></a>Trabajar con ubicaciones alternativas durante la restauración

Hay muchas razones por las que un solicitante no debe, o no, poder restaurar archivos desde medios de copia de seguridad a su ubicación original. Por ejemplo, un método de restauración o un destino pueden requerir este tipo de restauración, o la ubicación de restauración actual puede estar ocupada y no se puede escribir.

Para controlar estos casos, un escritor puede haber definido una asignación de ubicación alternativa [*,*](vssgloss-a.md)un destino de restauración no estándar que se usará para circunstancias especiales.

El término asignación de ubicación alternativa, como se usa con VSS, no debe confundirse con el término [*ruta de acceso alternativa*](vssgloss-a.md). Las asignaciones de ubicación alternativas solo se usan durante las operaciones de restauración y hacen referencia a un destino alternativo para las operaciones de restauración. Las rutas de acceso alternativas solo se usan durante las operaciones de copia de seguridad y hacen referencia a un origen alternativo del que se va a realizar una copia de seguridad.

Para usar asignaciones de ubicación alternativas durante la restauración, un solicitante haría lo siguiente (normalmente después de la generación de un [**evento PreRestore):**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore)

1.  Con una instancia de la interfaz [**IVssExbruwriterMetadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata) obtenida al recuperar un escritor almacenado, un solicitante usa el método [**IVssExbruWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) para obtener las asignaciones de ubicación alternativas de un escritor como instancias de la interfaz [**IVssWMFiledesc.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

    > [!Note]  
    > El solicitante usa [**IVssExgvWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping), no [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping). El primero devuelve esas asignaciones de ubicación alternativas disponibles para que las use un solicitante. Este último se usa para indicar las asignaciones de ubicación alternativas usadas realmente por un solicitante.

     

2.  La llamada a [**IVssExgvWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) devuelve una instancia de la [**interfaz IVssWMFiledesc.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) Esta instancia contiene información del conjunto de archivos: una ruta de acceso especificada por [**IVssWMFiledesc::GetPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getpath), una especificación de archivo devuelta a través de [**IVssWMFiledesc::GetFilespec**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getfilespec)y una marca de recursividad obtenida de [**IVssWMFiledesc::GetRecursive**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getrecursive)—matching uno de los conjuntos de archivos agregados (mediante [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)o [**IVssCreateWriterMetadata::AddFilesToFileGroup)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)a uno de los componentes administrados por el escritor.

    El valor devuelto por [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation) es la asignación de ubicación alternativa para este conjunto de archivos.

3.  Las asignaciones de ubicación alternativas no contienen información de componentes, por lo que será necesario comparar la información del conjunto de archivos (ruta de acceso, especificación de archivo y marca de recursión) obtenida mediante una llamada a [**IVssExwriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping) con la que contienen los componentes del escritor.

    Esta información se puede encontrar si se itera por los componentes del escritor y se llama a [**IVssExatingWriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) para obtener una instancia de la interfaz [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) y usar [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) para obtener una instancia [**de IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) que contiene la información del conjunto de archivos de componentes.

    Cuando la información del conjunto de archivos devuelta por la instancia de [**IVssWMFiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) obtenida de [**IVssExwriterMetadata::GetComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent) e [**IVssWMComponent::GetFile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getfile) coincide con la obtenida de la instancia **IVssWMFiledesc** derivada de [**IVssWMFiledesc::GetAlternateLocation**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmfiledesc-getalternatelocation), se ha encontrado el componente que administra los archivos con la asignación de ubicación alternativa específica.

4.  Una vez ubicado el componente, el solicitante puede determinar las condiciones en las que se debe usar una asignación de ubicación alternativa haciendo lo siguiente:

    -   Examinar el método de restauración del componente, que se obtiene mediante una llamada a [**IVssExgvWriterMetadata::GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod).
    -   Para comprobar si un destino de restauración invalida el método de restauración, llame a [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget).

        Si el componente que se encuentra [](vssgloss-e.md) en el documento de metadatos del escritor se ha incluido explícitamente en la copia de seguridad, la instancia de la [**interfaz IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) se corresponderá con ese componente. Si el componente [](vssgloss-i.md) se ha incluido implícitamente en la copia de seguridad, la instancia de **IVssComponent** se corresponderá con el componente que define el conjunto de componentes del que el componente del documento de metadatos del escritor es un subcomponente.

5.  Con esta información, el solicitante puede determinar por componente si necesita restaurar un conjunto de archivos determinado de un componente determinado en un destino definido por la asignación de ubicación alternativa.

6.  Cuando se usa una asignación de ubicación alternativa, el solicitante respeta el descriptor de archivo y la marca recursiva del conjunto de archivos y usa la ruta de acceso proporcionada por la asignación de ubicación alternativa.

    El solicitante indica que ha usado una asignación de ubicación alternativa durante una operación de restauración llamando a [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping) con la información de ubicación predeterminada del conjunto de archivos, el destino de restauración alternativo utilizado y un nombre de componente.

    Si un componente que se incluyó explícitamente en la copia de seguridad administra el conjunto de archivos, se usará ese nombre de componente. Si el conjunto de archivos lo administra un componente que se incluyó implícitamente en la copia de seguridad, el nombre utilizado será el del componente que define el conjunto de componentes del que el componente que administra el conjunto de archivos es un subcomponente.

Los escritores comprueban si los conjuntos de archivos de uno de sus componentes se restauraron en una asignación de ubicación alternativa mediante una llamada a [**IVssComponent::GetAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getalternatelocationmapping).

 

 



