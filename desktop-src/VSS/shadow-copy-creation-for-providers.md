---
description: Creación de instantáneas para proveedores
ms.assetid: d5042945-ba81-40d0-b204-1f08d153a788
title: Creación de instantáneas para proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91cc7306e7a13ef8e96ab032016a922411a70f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082478"
---
# <a name="shadow-copy-creation-for-providers"></a>Creación de instantáneas para proveedores

## <a name="the-shadow-copy-creation-process"></a>Proceso de creación de instantáneas

Un solicitante es la aplicación que inicia la solicitud para crear una instantánea. Normalmente, el solicitante es una aplicación de copia de seguridad. Según sea necesario, VSS llamará a los proveedores implicados. La mayoría de los proveedores están interesados en tres solicitudes específicas del solicitante.

1.  El solicitante comienza la actividad de creación de instantáneas con una llamada a [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset). Esto genera un **GUID** de tipo **\_ ID de VSS** que identifica de forma única este conjunto de instantáneas específico: SnapshotSetId. El proveedor no está implicado en este paso, pero el SnapshotSetId se usa en todos los pasos siguientes.
2.  Para cada volumen que desea incluir en este conjunto de instantáneas, el solicitante llama a [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). VSS determina qué proveedor se usará para realizar la instantánea del volumen.
    -   Varios proveedores pueden participar en un conjunto de instantáneas. Por ejemplo, si el volumen del sistema y un volumen de datos forman parte del mismo conjunto de instantáneas, es posible que el proveedor del sistema sirva como proveedor de instantáneas para el volumen del sistema, mientras que un proveedor de hardware puede actuar como proveedor de instantáneas para el volumen de datos. Ambos proveedores formarían parte del mismo conjunto de instantáneas y el usuario esperaría la misma coherencia a un momento dado en ambos volúmenes.
    -   Para que se seleccione un proveedor de hardware, el proveedor de hardware debe ser capaz de admitir todos los LUN que contribuyan al volumen especificado.
    -   A todos los proveedores registrados se les da la oportunidad de indicar compatibilidad con un volumen determinado durante la creación de la instantánea. Si hay más de un proveedor que indica compatibilidad, VSS usará primero los proveedores de hardware, los proveedores de software y, por último, el proveedor del sistema (si ningún otro proveedor indica compatibilidad con ese volumen).
    -   Un solicitante puede invalidar este orden predeterminado indicando explícitamente el proveedor que necesita para crear la instantánea.
    -   Si hay varios proveedores de hardware que admiten un volumen determinado, no hay ninguna garantía sobre el orden en el que se llamará a los proveedores de hardware.
3.  Después de una o varias llamadas a [**AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), el solicitante puede solicitar que se cree la instantánea con el método [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) . A continuación, VSS funciona con el sistema para crear la instantánea. El método **DoSnapshotSet** realiza este trabajo de forma asincrónica y el solicitante puede sondear o esperar a que se complete el proceso de creación de instantáneas.

En este diagrama se muestran las interacciones entre el solicitante, el servicio VSS, la compatibilidad con el kernel de VSS, cualquier Escritor VSS implicado y cualquier proveedor de hardware VSS. Vea [el proceso de creación de instantáneas](the-shadow-copy-creation-process.md) para obtener una descripción detallada de estas interacciones.

![interacciones entre el solicitante, los componentes de copia de seguridad, los escritores y los proveedores](images/vssimpl.png)

Una vez completado el proceso de creación de la instantánea, el solicitante puede determinar si la creación de la instantánea se ha realizado correctamente y, si no es así, determinar el origen del error.

Se debe minimizar el intervalo de tiempo entre la inmovilización y la reanudación de las aplicaciones del escritor. El proveedor debe iniciar de forma asincrónica todo el trabajo de preparación relacionado con la instantánea (por ejemplo, un proveedor de hardware que usa complejos que inician la sincronización) en el método [**IVssHardwareSnapshotProvider:: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) y, a continuación, esperar las finalizaciones en el método [**IVssProviderCreateSnapshotSet:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) .

Hay varias ventanas de límite de tiempo que deben seguir los proveedores. Como resultado, los proveedores con un comportamiento correcto realizarán todo el procesamiento innecesario antes de [**IVssProviderCreateSnapshotSet::P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) y después de [**IVssProviderCreateSnapshotSet::P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots).

El conjunto de instantáneas se fija cuando se llama a [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) . Los volúmenes adicionales no se pueden agregar más adelante, ya que los volúmenes adicionales no compartirán el mismo momento en el tiempo.

Hay un límite de 64 volúmenes en el conjunto de instantáneas. Un volumen específico puede asignarse a un LUN completo, a una parte de un LUN o a partes de varios LUN. La mayoría de las configuraciones tendrán un volumen por LUN, aunque es posible realizar asignaciones arbitrarias.

No hay ningún límite en el número de conjuntos de instantáneas o en el número de conjuntos de instantáneas de un volumen original. Un proveedor puede definir límites específicos o limitar de forma dinámica en función de los recursos de hardware disponibles.

### <a name="point-in-time-for-writerless-applications"></a>A un momento dado para aplicaciones no de escritura

VSS incluye una compatibilidad especial que define el momento dado que es común para todos los volúmenes de un conjunto de instantáneas. Los proveedores de hardware no necesitan interactuar directamente con estas tecnologías de kernel, ya que se invocan como parte del procesamiento normal de la confirmación de la instantánea. Sin embargo, resulta útil comprender los mecanismos que se usan, ya que explica la definición de "un momento dado" para las aplicaciones sin escritor (aplicaciones que no han expuesto una interfaz VSS Writer y, por tanto, no participan en el proceso de creación de instantáneas de volumen).

Esta compatibilidad con el kernel de VSS para un momento dado se distribuye entre el VolSnap.sys controlador, los sistemas de archivos y VSS.

1.  Antes de que se invoque la compatibilidad con el kernel de VSS, VSS ya ha:
    1.  Determine qué volúmenes van a participar en la instantánea.
    2.  Determina qué proveedor se va a usar en cada volumen.
    3.  Aplicaciones inmovilizadas que aceptan mensajes de inmovilización/reanudación.
    4.  Se han preparado los proveedores para la instantánea mediante una llamada a los métodos [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) . Ahora todos los proveedores están esperando para realizar la creación de instantáneas real.
2.  A continuación, se crea el momento dado. VSS vacía los sistemas de archivos de forma simultánea en todos los volúmenes de los que se van a realizar instantáneas.
    1.  VSS emite un \_ \_ \_ \_ \_ comando de control de escritura de los archivos de escritura de ioctl VOLSNAP y en cada volumen que vacía los sistemas de archivos. Ese IOCTL se pasa a la pila de almacenamiento hacia VolSnap.sys. A continuación, VolSnap.sys contiene todas las IRP de escritura hasta el paso 4 a continuación. Cualquier sistema de archivos (como RAW) sin soporte técnico para este nuevo IOCTL pasa el IOCTL desconocido hacia abajo, donde se vuelve a almacenar en VolSnap.sys. En volúmenes NTFS, el vaciado también confirma el registro de NTFS.
    2.  Esto suspende toda la actividad de metadatos de NTFS/FAT; los metadatos del sistema de archivos se confirman correctamente.
    3.  Instantánea: VolSnap.sys hace que todos los IRP de escritura posteriores se coqueuen en todos los volúmenes de los que se va a realizar la instantánea.
    4.  VolSnap.sys espera a que se completen todas las escrituras pendientes en los volúmenes de instantáneas. Los volúmenes están ahora inactivos con respecto a las escrituras y estaban inactivos exactamente en el mismo momento en cada volumen. No hay ninguna garantía sobre las escrituras en secciones asignadas por el usuario o escrituras emitidas entre (a) y (b) en sistemas de archivos que no implementan el IOCTL de vaciado (por ejemplo, sin formato).
3.  VSS indica a cada proveedor que realice la instantánea mediante una llamada a los métodos [**IVssProviderCreateSnapshotSet:: CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . Los proveedores deben tener toda la preparación para que se realice una operación rápida.

    Tenga en cuenta que el sistema de e/s solo está inactivo mientras se ejecutan estos métodos [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . Si un proveedor realiza cualquier sincronización de los LUN de origen y de instantáneas, esta sincronización se debe completar antes de que se devuelva el método **CommitSnapshots** del proveedor. No se puede realizar de forma asincrónica.

4.  Inmediatamente después de que el método [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) del último proveedor vuelva, VSS libera todas las IRP de escritura pendientes (incluidas las IRP que estaban bloqueando los sistemas de archivos al concluir sus rutas de confirmación) mediante la invocación de otro IRP pasado a VolSnap.sys.
5.  Si el proceso de instantáneas se realizó correctamente, entonces VSS ahora:
    1.  Llama a [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) para los proveedores implicados.
    2.  Llama a [**CVssWriter:: Alcongelar**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) para los escritores implicados.
    3.  Informa al solicitante de que se ha completado el proceso de instantáneas.

[**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots), a [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) son siempre críticos. Todas las e/s de las aplicaciones con escritores se inmovilizan de **PreCommitSnapshots** a **PostCommitSnapshots**. los retrasos afectan a la disponibilidad de la aplicación. Toda la e/s de archivos, incluida la e/s de aplicación no escritor, se suspende durante **CommitSnapshots**.

Los proveedores deben completar todo el trabajo crítico en cuanto al tiempo antes de devolver desde [**EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots).

-   [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) debe devolverse en cuestión de segundos. La fase **CommitSnapshots** se encuentra en la ventana vaciar y mantener. La compatibilidad con el kernel de VSS cancelará el vaciado y la suspensión que contiene la e/s si la versión posterior no se recibe en 10 segundos y VSS producirá un error en el proceso de creación de la instantánea. Se producirán otras actividades en el sistema, por lo que un proveedor no debe confiar en tener un máximo de 10 segundos. El proveedor no debe llamar a las API de Win32 durante la confirmación, ya que muchos darán lugar a Escrituras y bloqueos inesperados. Si el proveedor tarda más de unos segundos en completar la llamada, hay una alta probabilidad de que se produzca un error.
-   La secuencia completa de [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) al valor devuelto de [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) se asigna a la ventana entre escritores que reciben los eventos Freeze y procongele. El valor predeterminado del escritor para esta ventana es de 60 segundos, pero un escritor puede invalidar este valor con un tiempo de espera menor. Por ejemplo, el escritor de Microsoft Exchange Server cambia el tiempo de espera a 20 segundos. Los proveedores no deben gastar más de un segundo o dos en este método.

Durante la [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) , el proveedor debe evitar cualquier e/s de archivo que no sea de paginación. Esta e/s tiene una probabilidad muy alta de interbloqueos. En concreto, el proveedor no debe escribir sincrónicamente ningún registro de depuración o de seguimiento.

 

 



