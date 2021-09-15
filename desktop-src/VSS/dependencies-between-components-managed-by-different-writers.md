---
description: Hay situaciones en las que los datos de un escritor dependen de los datos administrados por otro escritor. En estos casos, debe hacer una copia de seguridad o restaurar los datos de ambos escritores.
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: Dependencias entre componentes administrados por distintos escritores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba3be6a2c2f0a722c4c5f06ca95351e004e1cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473386"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>Dependencias entre componentes administrados por distintos escritores

Hay situaciones en las que los datos de un escritor dependen de los datos administrados por otro escritor. En estos casos, debe hacer una copia de seguridad o restaurar los datos de ambos escritores.

VSS controla este problema a través de la noción de una dependencia explícita de componente de escritor y la [**interfaz IVssWMDependency.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency)

Un escritor agrega una o varias dependencias al crear el documento de metadatos del escritor mediante el método [**IVssCreateWriterMetadata::AddComponentDependency.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) El sistema de escritura pasa al método el nombre y la ruta de acceso lógica del componente dependiente (que administra), así como el nombre y la ruta de acceso lógica y el identificador de clase de escritor [*(el*](vssgloss-w.md) GUID que identifica la clase) del componente del que depende.

Una vez establecida, esta dependencia informa al solicitante de que durante cualquier operación de copia de seguridad o restauración deben participar tanto el componente dependiente como los destinos de sus dependencias.

Un componente determinado puede tener varias dependencias, lo que requiere que él y todos sus destinos dependientes participen juntos en la copia de seguridad y restauración.

El componente dependiente o los destinos de sus dependencias se [](vssgloss-i.md) pueden incluir explícita o implícitamente en las operaciones de copia de seguridad o restauración. [](vssgloss-e.md)

El mecanismo de dependencia del componente de escritor explícito no debe usarse para crear una dependencia entre dos componentes del mismo sistema de escritura. Las reglas de selección pueden proporcionar la misma funcionalidad de forma más eficaz sin riesgo de dependencias circulares.

Por ejemplo, [**IVssCreateWriterMetadata::AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) podría usarse para definir la dependencia del componente writerData (con la ruta de acceso lógica "") del escritor MyWriter en el componente internetData (con una ruta de acceso lógica de "Connections") de un escritor llamado InternetConnector con un identificador de clase de escritor X. (Aunque es posible que varios escritores con el mismo identificador de clase se puedan encontrar simultáneamente en el sistema, se evitará la confusión porque la combinación de ruta de acceso lógica y nombre de componente es única en el sistema en VSS).

Un sistema de escritura agrega varias dependencias a un componente determinado simplemente llamando a [**IVssCreateWriterMetadata::AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) repetido con componentes diferentes de escritores diferentes. Para encontrar el número de otros componentes de los que depende un componente determinado, examine el **miembro cDependencies** de la estructura [**\_ COMPONENTINFO de VSS.**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo)

Un escritor o solicitante recupera instancias de la interfaz [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) con [**IVssWMComponent::GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). **IVssWMDependency** devuelve el nombre del componente, la ruta de acceso lógica y el identificador de clase del escritor que administra el componente que es el destino de la dependencia.

El mecanismo de dependencia no prescribe ningún orden de preferencia concreto entre el componente dependiente y los destinos de sus dependencias. Como se indicó anteriormente, todas las dependencias indican que cada vez que se hace una copia de seguridad o se restaura un componente determinado, también se debe realizar una copia de seguridad o restaurar los componentes de los que depende. La implementación exacta de la dependencia está a discreción de la aplicación de copia de seguridad.

Por ejemplo, en el caso anterior, el componente writerData (ruta de acceso lógica "") depende del componente InternetConnector (ruta de acceso lógica "Conexiones"). Un solicitante puede interpretar esto de cualquiera de las maneras siguientes:

-   Si el componente dependiente writerData está seleccionado (implícita o explícitamente) para la copia de seguridad o restauración, el solicitante debe seleccionar (implícita o explícitamente) el destino de su dependencia, internetData.
-   Si el destino de su dependencia, internetData, no está seleccionado para la copia de seguridad, no se debe seleccionar el componente dependiente writerData.

Sin embargo, al desarrollar compatibilidad con dependencias, los desarrolladores solicitantes deben tener en cuenta que no hay ninguna manera de que un escritor pueda determinar si uno de sus componentes es un destino de una dependencia.

## <a name="declaring-remote-dependencies"></a>Declarar dependencias remotas

Una aplicación distribuida es una aplicación que se puede configurar para usar uno o varios equipos a la vez. Normalmente, la aplicación se ejecuta en uno o varios equipos del servidor de aplicaciones y se comunica con (pero puede o no ejecutarse realmente en) uno o varios equipos del servidor de bases de datos. Esta configuración se conoce a veces como una implementación de varios sistemas. A menudo, la misma aplicación también se puede configurar para ejecutarse en un único equipo que ejecuta un servidor de aplicaciones y un servidor de bases de datos. Esta configuración se denomina implementación de sistema único. En ambas configuraciones, el servidor de aplicaciones y el servidor de bases de datos tienen sus propios escritores de VSS independientes.

En una implementación de varios sistemas, si un componente administrado por el escritor de la aplicación depende de un componente remoto administrado por el escritor del servidor de bases de datos, esto se denomina dependencia remota. (En cambio, una implementación de sistema único solo tiene dependencias locales).

Como ejemplo de una implementación de varios sistemas, considere un servidor de aplicaciones que usa un servidor SQL Server base de datos como almacén de datos. Los datos específicos de la aplicación, que incluyen los elementos web, los archivos de contenido web y la metabase de IIS, residen en uno o varios equipos, denominados servidores web front-end. El almacén de SQL datos real, que incluye la base de datos Config y varias bases de datos de contenido, reside en uno o varios equipos, denominados servidores de base de datos back-end. Cada uno de los servidores web front-end contiene el mismo contenido y configuración específicos de la aplicación. Cada uno de los servidores de bases de datos back-end puede hospedar cualquiera de las bases de datos content o config. El software de la aplicación solo se ejecuta en los servidores web front-end, no en los servidores de base de datos. En esta configuración, VSS Writer de la aplicación tiene dependencias remotas en los componentes administrados por SQL writer.

Un escritor puede declarar una dependencia remota llamando al método [**AddComponentDependency,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) anteponer " \\ \\ *RemoteComputerName*", donde RemoteComputerName es el nombre del equipo donde reside el componente remoto, a la ruta de acceso lógica del parámetro \\ *wszOnLogicalPath.*  El valor de *RemoteComputerName* puede ser una dirección IP o un nombre de equipo devuelto por la [**función GetComputerNameEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa)

**Windows Server 2003:** Un escritor no puede declarar dependencias remotas hasta Windows Server 2003 con Service Pack 1 (SP1).

Para identificar una dependencia, un solicitante llama a los métodos [**GetWriterId**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)y [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname) de la [**interfaz IVssWMDependency.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) El solicitante debe examinar el nombre del componente que **GetComponentName devuelve** en el *parámetro pbstrComponentName.* Si el nombre del componente comienza por " ", el solicitante debe asumir que especifica una dependencia remota y que el primer componente que sigue a " " es el RemoteComputerName que se especificó cuando el escritor llamó \\ \\ a \\ \\ [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency).  Si el nombre del componente no comienza por " ", el solicitante debe asumir \\ \\ que especifica una dependencia local.

Si hay una dependencia remota, el solicitante debe hacer una copia de seguridad del componente remoto cuando haga una copia de seguridad del componente local. Para realizar una copia de seguridad del componente remoto, el solicitante debe tener un agente en el equipo remoto y debe iniciar la copia de seguridad en el equipo remoto.

## <a name="structuring-remote-dependencies"></a>Estructurar dependencias remotas

Es importante comprender que una dependencia no es un componente de y de sí misma. Un componente es necesario para contener la dependencia.

En los ejemplos siguientes se muestran dos maneras de estructurar un conjunto de dependencias.

``` syntax
Example 1:
    Writer 1
        Component A
            File A
            File B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")

Example 2:
    Writer 2
        Component A
            File A
            File B
        Component B
            Dependency (SQL/MSDE Writer, Component X, "\")
            Dependency (SQL/MSDE Writer, Component Y, "\")
```

En el ejemplo 1, el componente A mantiene las dependencias. Dado que solo se pueden seleccionar componentes, no archivos individuales, estructurar las dependencias del componente A de esta manera requeriría que se realizara una copia de seguridad y restauración conjunta de todo el componente, tanto los archivos como las dependencias. No se pueden realizar una copia de seguridad ni restaurarse individualmente.

En el ejemplo 2, los componentes independientes (componentes A y B) incluyen cada una de las dependencias. En este caso, los dos componentes se pueden seleccionar de forma independiente y, por tanto, realizar una copia de seguridad y restaurarse de forma independiente. La estructuración de las dependencias de esta manera proporciona a una aplicación distribuida mucha más flexibilidad a la hora de administrar sus dependencias remotas.

## <a name="supporting-remote-dependencies"></a>Compatibilidad con dependencias remotas

Un solicitante puede proporcionar compatibilidad total o parcial con las dependencias remotas.

Para proporcionar soporte técnico completo, el solicitante debe hacer lo siguiente en tiempo de copia de seguridad y restauración.

En el momento de la copia de seguridad, el solicitante debe iniciar la copia de seguridad en el equipo front-end (local), determinar las dependencias que existen y poner en cola trabajos de copia de seguridad adicionales para capturar las bases de datos back-end. El solicitante debe esperar hasta que se hayan completado los trabajos de copia de seguridad de back-end en el equipo remoto antes de llamar a los [**métodos IVssBackupComponents::SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) e [**IVssBackupComponents::BackupComplete.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) Si el solicitante espera hasta que se complete la copia de seguridad de los componentes de back-end antes de llamar a **BackupComplete,** se producirá una copia de seguridad recuperable más fácilmente para un escritor que implementa mejoras adicionales, como el bloqueo de topología, por ejemplo, durante la copia de seguridad. En el procedimiento siguiente se describe lo que debe hacer el solicitante:

1.  En el equipo local, el solicitante llama a los [**métodos IVssBackupComponents::InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**IVssBackupComponents::GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) [**IVssBackupComponents::P repareForBackup y**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)
2.  Una vez completada la instantánea local, pero antes de que se complete la copia de seguridad, el solicitante crea trabajos de copia de seguridad adicionales mediante el envío de una solicitud a su agente en el equipo remoto.
3.  En el equipo remoto, el agente del solicitante realiza la secuencia de copia de seguridad en cola llamando a [**InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**GatherWriterMetadata,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) [**PrepareForBackup,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) [**DoSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) [**SetBackupSucceeded y**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) [**BackupComplete.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)
4.  Cuando el agente del solicitante ha completado los trabajos en cola en el equipo remoto, el solicitante completa la secuencia de copia de seguridad llamando a [**SetBackupSucceeded y**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) [**BackupComplete.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete)

En el momento de la restauración, el solicitante debe iniciar la restauración que implica el equipo front-end (local), seleccionar los componentes y sus dependencias que se restaurarán y, a continuación, enviar el evento [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) llamando al método **IVssBackupComponents::P reRestore.** A continuación, el solicitante debe poner en cola los trabajos de restauración de back-end en el equipo remoto y llamar al método [**IVssBackupComponents::P ostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) cuando se completen las restauraciones de back-end. Este requisito proporciona al escritor de front-end más control sobre la experiencia de restauración y una mejor experiencia de usuario administrador en general. Dado que las copias de seguridad en cada uno de los sistemas no se producen en el mismo momento, el escritor de front-end tendrá que realizar alguna limpieza de los datos de back-end. En la aplicación de ejemplo que se describe en la anterior "Declaración de dependencias remotas", el escritor debe iniciar una remapping o reindexación del sitio después de que se haya completado la restauración de una de las bases de datos back-end. Para ello, el escritor debe recibir eventos en el servidor front-end. En el procedimiento siguiente se describe lo que debe hacer el solicitante:

1.  En el equipo local, el solicitante llama a [**IVssBackupComponents::InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents::SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (o [**IVssBackupComponentsEx::SetSelectedForRestoreEx)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)y [**PreRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).
2.  Una vez completada la fase [**PreRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) pero antes de que comience la fase [**PostRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) el solicitante crea trabajos de restauración adicionales mediante el envío de una solicitud a su agente en el equipo remoto.
3.  En el equipo remoto, el agente del solicitante realiza los trabajos de restauración en cola llamando a [**InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), [**PreRestore,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) [**SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) (o [**SetSelectedForRestoreEx)**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)y [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).
4.  Cuando el agente del solicitante ha completado los trabajos en cola en el equipo remoto, el solicitante completa la secuencia de restauración llamando a [**IVssBackupComponents::SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) y [**PostRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Para proporcionar compatibilidad parcial con las dependencias remotas, el solicitante debe seguir las dependencias remotas e incluirlas como parte de la copia de seguridad, pero no sería necesario ordenar los eventos en los sistemas front-end y back-end como se detalla en los dos procedimientos anteriores. Para un solicitante que implementa solo compatibilidad parcial, el solicitante debe consultar la documentación de copia de seguridad y restauración de la aplicación de escritura para comprender qué escenarios se pueden admitir.

 

 
