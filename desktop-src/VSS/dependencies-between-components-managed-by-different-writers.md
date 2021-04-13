---
description: Hay situaciones en las que los datos de un escritor dependen de datos administrados por otro escritor. En estos casos, debe realizar una copia de seguridad o restaurar los datos de ambos escritores.
ms.assetid: 0413c289-74b7-4e83-a227-00bfb264e56e
title: Dependencias entre los componentes administrados por escritores diferentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba3be6a2c2f0a722c4c5f06ca95351e004e1cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361453"
---
# <a name="dependencies-between-components-managed-by-different-writers"></a>Dependencias entre los componentes administrados por escritores diferentes

Hay situaciones en las que los datos de un escritor dependen de datos administrados por otro escritor. En estos casos, debe realizar una copia de seguridad o restaurar los datos de ambos escritores.

VSS controla este problema a través de la noción de una dependencia de componente de escritor explícita y la interfaz [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) .

Un escritor agrega una o más dependencias al crear el documento de metadatos del escritor mediante el método [**IVssCreateWriterMetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) . El escritor pasa al método el nombre y la ruta de acceso lógica del componente dependiente (que administra), así como el nombre y la ruta de acceso lógica y el [*identificador de clase del escritor*](vssgloss-w.md) (el GUID que identifica la clase) del componente del que depende.

Una vez establecida, esta dependencia informa al solicitante de que, durante cualquier operación de copia de seguridad o restauración, debe participar el componente dependiente y los destinos de sus dependencias.

Un componente determinado puede tener varias dependencias, lo que requiere que todos los destinos dependientes participen en la copia de seguridad y se restauren juntos.

El componente dependiente y/o los destinos de sus dependencias se pueden incluir [*explícita*](vssgloss-e.md) o [*implícitamente*](vssgloss-i.md) en las operaciones de copia de seguridad o restauración.

El mecanismo de dependencia del componente de escritor explícito no debe usarse para crear una dependencia entre dos componentes en el mismo sistema de escritura. Las reglas de selección pueden proporcionar la misma funcionalidad de forma más eficaz sin riesgo de dependencias circulares.

Como ejemplo, se podría usar [**IVssCreateWriterMetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) para definir la dependencia del componente writerData (con la ruta de acceso lógica "") del escritor alwriter en el componente internetData (con una ruta de acceso lógica de "Connections") de un escritor denominado InternetConnector con un identificador de clase X del escritor. (aunque es posible que varios escritores con el mismo identificador de clase estén en el sistema simultáneamente, se evitará la confusión porque la combinación de nombre de componente y ruta de acceso lógica es única en el sistema en VSS).

Un escritor agrega varias dependencias a un componente determinado mediante una llamada a [**IVssCreateWriterMetadata:: AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) que se repite con distintos componentes de escritores distintos. El número de componentes de los que depende un componente determinado se puede encontrar examinando el miembro **cDependencies** de la [**estructura \_ COMPONENTINFO de VSS**](/windows/desktop/api/VsBackup/ns-vsbackup-vss_componentinfo) .

Un escritor o solicitante recupera las instancias de la interfaz [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) con [**IVssWMComponent:: GetDependency**](/windows/desktop/api/VsBackup/nf-vsbackup-ivsswmcomponent-getdependency). **IVssWMDependency** devuelve el nombre del componente, la ruta de acceso lógica y el ID. de clase del escritor que administra el componente que es el destino de la dependencia.

El mecanismo de dependencia no prescribe ningún orden de preferencia determinado entre el componente dependiente y los destinos de sus dependencias. Como se indicó anteriormente, todas las dependencias indican que cada vez que se realiza una copia de seguridad o se restaura un componente determinado, también se debe realizar una copia de seguridad o restauración del componente o los componentes de los que depende. La implementación exacta de la dependencia depende de la aplicación de copia de seguridad.

Por ejemplo, en el caso anterior, el componente writerData (ruta de acceso lógica "") depende del componente InternetConnector (ruta de acceso lógica "Connections"). Un solicitante puede interpretarlo de una de las siguientes maneras:

-   Si el componente dependiente, writerData, está seleccionado (implícita o explícitamente) para la copia de seguridad o la restauración, el solicitante debe seleccionar (implícita o explícitamente) el destino de su dependencia, internetData
-   Si el destino de su dependencia, internetData, no se selecciona para la copia de seguridad, no se debe seleccionar el componente dependiente, writerData.

Sin embargo, al desarrollar compatibilidad para las dependencias, los desarrolladores del solicitante deben tener en cuenta que no hay ninguna manera en que un escritor puede determinar si uno de sus componentes es un destino de una dependencia.

## <a name="declaring-remote-dependencies"></a>Declarar dependencias remotas

Una aplicación distribuida es una aplicación que puede configurarse para usar uno o varios equipos a la vez. Normalmente, la aplicación se ejecuta en uno o más equipos de servidor de aplicaciones y se comunica con (pero que en realidad puede ejecutarse en) uno o más equipos de servidor de bases de datos. Esta configuración se conoce a veces como una implementación de varios sistemas. A menudo, la misma aplicación también puede configurarse para ejecutarse en un único equipo que ejecute un servidor de aplicaciones y un servidor de base de datos. Este tipo de configuración se denomina implementación de un solo sistema. En ambas configuraciones, el servidor de aplicaciones y el servidor de base de datos tienen sus propios escritores de VSS independientes.

En una implementación de varios sistemas, si un componente administrado por el sistema de escritura de la aplicación depende de un componente remoto administrado por el sistema de escritura del servidor de bases de datos, esto se denomina dependencia remota. (En cambio, una implementación de un solo sistema solo tiene dependencias locales).

Como ejemplo de una implementación de varios sistemas, considere la posibilidad de usar un servidor de aplicaciones que use un servidor de SQL Server Database como almacén de datos. Los datos específicos de la aplicación, que incluyen los elementos Web, los archivos de contenido web y la metabase de IIS, residen en uno o varios equipos, denominados servidores front-end web. El almacén de datos SQL real, que incluye la base de datos de configuración y varias bases de datos de contenido, reside en uno o varios equipos, denominados servidores de base de datos back-end. Cada uno de los servidores front-end web contiene el mismo contenido y configuración específicos de la aplicación. Cada uno de los servidores de bases de datos back-end puede hospedar cualquiera de las bases de datos de contenido o la base de datos de configuración. El software de aplicación solo se ejecuta en los servidores front-end web, no en los servidores de bases de datos. En esta configuración, el VSS Writer de la aplicación tiene dependencias remotas en los componentes administrados por el escritor SQL.

Un sistema de escritura puede declarar una dependencia remota mediante una llamada al método [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency) , anteponiendo " \\ \\ *nombreDeEquipoRemoto* \\ ", donde *nombreDeEquipoRemoto* es el nombre del equipo en el que reside el componente remoto, en la ruta de acceso lógica del parámetro *wszOnLogicalPath* . El valor de *nombreDeEquipoRemoto* puede ser una dirección IP o un nombre de equipo devuelto por la función [**GetComputerNameEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .

**Windows Server 2003:** Un escritor no puede declarar dependencias remotas hasta Windows Server 2003 con Service Pack 1 (SP1).

Para identificar una dependencia, un solicitante llama a los métodos [**GetWriterId**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getwriterid), [**GetLogicalPath**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getlogicalpath)y [**GetComponentName**](/windows/desktop/api/VsWriter/nf-vswriter-ivsswmdependency-getcomponentname) de la interfaz [**IVssWMDependency**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmdependency) . El solicitante debe examinar el nombre del componente que devuelve **GetComponentName** en el parámetro *pbstrComponentName* . Si el nombre del componente comienza por " \\ \\ ", el solicitante debe asumir que especifica una dependencia remota y que el primer componente que sigue a " \\ \\ " es el *nombreDeEquipoRemoto* que se especificó cuando el escritor llamó a [**AddComponentDependency**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponentdependency). Si el nombre del componente no comienza por " \\ \\ ", el solicitante debe suponer que especifica una dependencia local.

Si hay una dependencia remota, el solicitante debe hacer una copia de seguridad del componente remoto cuando realiza una copia de seguridad del componente local. Para realizar una copia de seguridad del componente remoto, el solicitante debe tener un agente en el equipo remoto y debe iniciar la copia de seguridad en el equipo remoto.

## <a name="structuring-remote-dependencies"></a>Estructuración de dependencias remotas

Es importante comprender que una dependencia no es un componente de sí mismo. Un componente es necesario para contener la dependencia.

En los siguientes ejemplos se muestran dos maneras de estructurar un conjunto de dependencias.

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

En el ejemplo 1, las dependencias están retenidas por el componente A. Dado que solo se pueden seleccionar los componentes, no los archivos individuales, la estructura de las dependencias de los componentes A de esta manera requeriría que todo el componente, tanto los archivos como las dependencias, siempre se debe hacer una copia de seguridad y restaurar juntos. No se puede realizar una copia de seguridad ni restaurar individualmente.

En el ejemplo 2, los componentes independientes (los componentes A y B) contienen cada una de las dependencias. En este caso, los dos componentes pueden seleccionarse de forma independiente y, por tanto, realizar una copia de seguridad y restaurarse de forma independiente. La estructura de las dependencias de este modo proporciona a una aplicación distribuida mucha más flexibilidad en la administración de sus dependencias remotas.

## <a name="supporting-remote-dependencies"></a>Compatibilidad con dependencias remotas

Un solicitante puede proporcionar compatibilidad completa o parcial para las dependencias remotas.

Para proporcionar soporte completo, el solicitante debe hacer lo siguiente en el momento de la copia de seguridad y la restauración.

En el momento de la copia de seguridad, el solicitante debe iniciar la copia de seguridad en el equipo front-end (local), determinar las dependencias que existen y poner en cola trabajos de copia de seguridad adicionales para capturar las bases de datos de back-end. El solicitante debe esperar hasta que se hayan completado los trabajos de copia de seguridad de back-end en el equipo remoto antes de llamar a los métodos [**ivssbackupcomponents:: SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) y [**Ivssbackupcomponents:: BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) . Si el solicitante espera hasta que se complete la copia de seguridad de los componentes de back-end antes de llamar a **BackupComplete**, se generará una copia de seguridad más fácil de recuperar para un escritor que implementa mejoras adicionales, como el bloqueo de topología, por ejemplo, durante la copia de seguridad. En el procedimiento siguiente se describe lo que debe hacer el solicitante:

1.  En el equipo local, el solicitante llama a los métodos [**ivssbackupcomponents:: InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**Ivssbackupcomponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**Ivssbackupcomponents::P Repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup)y [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .
2.  Una vez completada la instantánea local, pero antes de que se complete la copia de seguridad, el solicitante pone en cola los trabajos de copia de seguridad adicionales mediante el envío de una solicitud a su agente en el equipo remoto.
3.  En el equipo remoto, el agente del solicitante realiza la secuencia de copia de seguridad en cola mediante una llamada a [**InitializeForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforbackup), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup), [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded)y [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).
4.  Cuando el agente del solicitante ha completado los trabajos en cola en el equipo remoto, el solicitante completa la secuencia de copia de seguridad mediante una llamada a [**SetBackupSucceeded**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setbackupsucceeded) y [**BackupComplete**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete).

En el momento de la restauración, el solicitante debe iniciar la restauración relacionada con el equipo front-end (local), seleccionar los componentes y sus dependencias que se van a restaurar y, a continuación, enviar el evento de [**prerestauración**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) llamando al método **IVssBackupComponents::P rerestore** . Después, el solicitante debe poner en cola los trabajos de restauración de back-end en el equipo remoto y llamar al método [**IVssBackupComponents::P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) cuando se completen las restauraciones de back-end. Este requisito proporciona al escritor de front-end más control sobre la experiencia de restauración y una mejor experiencia de usuario de administrador global. Dado que las copias de seguridad en cada uno de los sistemas no se producen en el mismo momento, el escritor de front-end tendrá que realizar alguna limpieza de los datos de back-end. En la aplicación de ejemplo que se describe en la sección anterior "declarar dependencias remotas", el escritor debe iniciar una reasignación de sitio o volver a indexar después de que se haya completado una restauración de una de las bases de datos de back-end. Para ello, el escritor debe recibir eventos en el servidor front-end. En el procedimiento siguiente se describe lo que debe hacer el solicitante:

1.  En el equipo local, el solicitante llama a [**IVssBackupComponents:: InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**IVssBackupComponents:: SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore) (o [**IVssBackupComponentsEx:: SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) y [**prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore).
2.  Una vez completada la fase de [**prerestauración**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore) , pero antes de que se inicie la fase de [**postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) , el solicitante pone en cola los trabajos de restauración adicionales mediante el envío de una solicitud a su agente en el equipo remoto.
3.  En el equipo remoto, el agente del solicitante realiza los trabajos de restauración en cola mediante una llamada a [**InitializeForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore), [**GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata), [**SetSelectedForRestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setselectedforrestore), [**prerestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prerestore), [**SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) (o [**SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)) y [**postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).
4.  Cuando el agente del solicitante ha completado los trabajos en cola en el equipo remoto, el solicitante completa la secuencia de restauración mediante una llamada a [**IVssBackupComponents:: SetFileRestoreStatus**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setfilerestorestatus) y [**postrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore).

Para proporcionar compatibilidad parcial con dependencias remotas, el solicitante debe seguir las dependencias remotas e incluirlas como parte de la copia de seguridad, pero el orden de los eventos en los sistemas front-end y back-end, tal como se detalla en los dos procedimientos anteriores, no sería necesario. Para un solicitante que implementa solo compatibilidad parcial, el solicitante debe hacer referencia a la documentación de copia de seguridad o restauración de la aplicación de escritura para comprender qué escenarios se pueden admitir.

 

 
