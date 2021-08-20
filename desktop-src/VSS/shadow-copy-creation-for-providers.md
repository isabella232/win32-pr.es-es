---
description: Creación de instantáneas para proveedores
ms.assetid: d5042945-ba81-40d0-b204-1f08d153a788
title: Creación de instantáneas para proveedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 953f9b5556b8cf0a35117d8df6756fdd52bdf033d390f0b08a7e018d1eaf5410
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121857"
---
# <a name="shadow-copy-creation-for-providers"></a>Creación de instantáneas para proveedores

## <a name="the-shadow-copy-creation-process"></a>El proceso de creación de instantáneas

Un solicitante es la aplicación que inicia la solicitud para crear una instantánea. Normalmente, el solicitante es una aplicación de copia de seguridad. Según sea necesario, VSS llamará a los proveedores implicados. La mayoría de los proveedores están interesados en tres solicitudes específicas del solicitante.

1.  El solicitante comienza la actividad de creación de instantáneas con una llamada a [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset). Esto genera un **GUID de** tipo **VSS \_ ID** que identifica de forma única este conjunto de instantáneas específico: SnapshotSetId. El proveedor no participa en este paso, pero SnapshotSetId se usa ampliamente en todos los pasos posteriores.
2.  Para cada volumen que quiera incluir en este conjunto de instantáneas, el solicitante llama a [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset). VSS determina qué proveedor se usará para crear instantáneas del volumen.
    -   Varios proveedores pueden participar en un conjunto de instantáneas. Por ejemplo, si el volumen del sistema y un volumen de datos forman parte del mismo conjunto de instantáneas, el proveedor del sistema puede actuar como proveedor de instantáneas para el volumen del sistema, mientras que un proveedor de hardware puede actuar como proveedor de instantáneas para el volumen de datos. Ambos proveedores formarán parte del mismo conjunto de instantáneas y el usuario esperaría la misma coherencia a un momento dado en ambos volúmenes.
    -   Para que se seleccione un proveedor de hardware, el proveedor de hardware debe ser capaz de admitir todos los LUN que contribuyen al volumen especificado.
    -   Todos los proveedores registrados tienen la oportunidad de indicar compatibilidad con un volumen determinado durante la creación de instantáneas. Si más de un proveedor indica compatibilidad, VSS primero tendrá como valor predeterminado los proveedores de hardware, los proveedores de software y, por último, el proveedor del sistema (si ningún otro proveedor indica compatibilidad con ese volumen).
    -   Un solicitante puede invalidar este orden predeterminado indicando explícitamente el proveedor que necesita para crear la instantánea.
    -   Si hay varios proveedores de hardware que admiten un volumen determinado, no hay ninguna garantía para el orden en el que se llamará a los proveedores de hardware.
3.  Después de una o varias llamadas a [**AddToSnapshotSet,**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)el solicitante puede solicitar la creación de la instantánea mediante el método [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) A continuación, VSS funciona con el sistema para crear la instantánea. El **método DoSnapshotSet** realiza este trabajo de forma asincrónica y el solicitante puede sondear o esperar a que se complete el proceso de creación de instantáneas.

En este diagrama se muestran las interacciones entre el solicitante, el servicio VSS, la compatibilidad del kernel de VSS, los escritores de VSS implicados y los proveedores de hardware de VSS. Consulte [Proceso de creación de instantáneas](the-shadow-copy-creation-process.md) para obtener una descripción detallada de estas interacciones.

![interacciones entre solicitantes, componentes de copia de seguridad, escritores y proveedores](images/vssimpl.png)

Una vez completado el proceso de creación de instantáneas, el solicitante puede determinar si la creación de instantáneas se ha realizado correctamente y, si no es así, determinar el origen del error.

El intervalo de tiempo entre la inmovilización y la descongelización de las aplicaciones de escritura debe minimizarse. El proveedor debe iniciar de forma asincrónica todo el trabajo de preparación relacionado con la instantánea (por ejemplo, un proveedor de hardware que usa plexos que inician la sincronización) en el método [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) y, a continuación, esperar las finalizaciones en el método [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)

Hay varias ventanas de límite de tiempo que los proveedores deben seguir. Como resultado, los proveedores bien comportados realizarán todo el procesamiento innecesario antes [**de IVssProviderCreateSnapshotSet::P reCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) y después [**de IVssProviderCreateSnapshotSet::P ostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots).

El conjunto de instantáneas se fija cuando se [**llama a DoSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) No se pueden agregar volúmenes adicionales más adelante porque los volúmenes adicionales no compartirían el mismo momento dado.

Hay un límite de 64 volúmenes en el conjunto de instantáneas. Un volumen específico puede asignarse a un LUN completo, una parte de un LUN o partes de varios LUN. La mayoría de las configuraciones tendrán un volumen por LUN, aunque es posible realizar asignaciones arbitrarias.

No hay ningún límite en el número de conjuntos de instantáneas ni en el número de conjuntos de instantáneas de un volumen original. Un proveedor puede definir límites específicos o limitar dinámicamente en función de los recursos de hardware disponibles.

### <a name="point-in-time-for-writerless-applications"></a>Un momento dado para aplicaciones sin escritor

VSS incluye compatibilidad especial que define el momento dado que es común para todos los volúmenes de un conjunto de instantáneas. Los proveedores de hardware no necesitan interfaz directa con estas tecnologías de kernel, ya que se invocan como parte del procesamiento normal de confirmación de instantáneas. Sin embargo, resulta útil comprender los mecanismos usados porque explica la definición de "punto en el tiempo" para las aplicaciones sin escritura (aplicaciones que no han expuesto una interfaz de VSS Writer y, por tanto, no participan en el proceso de creación de instantáneas de volumen).

Esta compatibilidad del kernel de VSS con un momento dado común se distribuye entre el controlador VolSnap.sys, los sistemas de archivos y VSS.

1.  Antes de invocar la compatibilidad con el kernel de VSS, VSS ya tiene:
    1.  Determina qué volúmenes van a estar implicados en la instantánea.
    2.  Determina qué proveedor se va a usar en cada volumen.
    3.  Aplicaciones inmovilizadas que aceptan mensajes de inmovilización o descongelación.
    4.  Preparó los proveedores para la instantánea mediante una llamada a [**los métodos PreCommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) Todos los proveedores están esperando a realizar la creación real de instantáneas.
2.  A continuación, se crea el momento dado. VSS vacía simultáneamente los sistemas de archivos en todos los volúmenes que se van a copiar en la sombra.
    1.  VSS emite un comando de \_ control IOCTL VOLSNAP FLUSH AND HOLD WRITES en \_ cada volumen que vacía los sistemas de \_ \_ \_ archivos. Esa IOCTL se pasa por la pila de almacenamiento para VolSnap.sys. VolSnap.sys a continuación, contiene todos los IRP de escritura hasta el paso 4 siguiente. Cualquier sistema de archivos (por ejemplo, RAW) sin compatibilidad con esta nueva IOCTL pasa la IOCTL desconocida, donde la mantiene de nuevo VolSnap.sys. En los volúmenes NTFS, el vaciado también confirma el registro NTFS.
    2.  Esto suspende toda la actividad de metadatos NTFS/FAT; los metadatos del sistema de archivos se confirman correctamente.
    3.  Instantánea de instantáneas: VolSnap.sys hace que todos los IRP de escritura subsiguientes se ponen en cola en todos los volúmenes que se van a copiar en la sombra.
    4.  VolSnap.sys espera a que se completen todas las escrituras pendientes en los volúmenes de instantáneas. Los volúmenes ahora están en modo de inmoción con respecto a las escrituras y estaban en modo de inmoción exactamente en el mismo momento en cada volumen. No hay ninguna garantía sobre las escrituras en secciones asignadas por el usuario o escrituras emitidas entre (a) y (b) en sistemas de archivos que no implementan la IOCTL de vaciado (por ejemplo, RAW).
3.  VSS indica a cada proveedor que tome la instantánea llamando a los [**métodos IVssProviderCreateSnapshotSet::CommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) Los proveedores deben realizar toda la preparación para que se trata de una operación rápida.

    Tenga en cuenta que el sistema de E/S solo está en modo de inquiete mientras se ejecutan estos [**métodos CommitSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) Si un proveedor realiza alguna sincronización de los LUN de origen y de instantáneas, esta sincronización debe completarse antes de que se devuelva el método **CommitSnapshots del** proveedor. No se puede realizar de forma asincrónica.

4.  Inmediatamente después de que se devuelva el método [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) del último proveedor, VSS libera todos los IRP de escritura pendientes (incluidos los IRP que bloqueaban los sistemas de archivos al finalizar sus rutas de confirmación) invocando otro IRP pasado a VolSnap.sys.
5.  Si el proceso de instantánea se ha realizado correctamente, VSS ahora:
    1.  Llama [**a PostCommitSnapshots para**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) los proveedores implicados.
    2.  Llama [**a CVssWriter::OnThaw para**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onthaw) los escritores implicados.
    3.  Informa al solicitante de que se ha completado el proceso de instantáneas.

[**Los archivos PreCommitSnapshots,**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)y [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) son críticos en todo momento. Todas las E/S de aplicaciones con escritores se inmovilizan de **PreCommitSnapshots** a **PostCommitSnapshots**; los retrasos afectan a la disponibilidad de la aplicación. Toda la E/S de archivo, incluida la E/S de aplicación sin escritura, se suspende **durante CommitSnapshots.**

Los proveedores deben completar todo el trabajo crítico antes de volver de [**EndPrepareSnapshots.**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots)

-   [**CommitSnapshots debe**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) devolverse en cuestión de segundos. La **fase CommitSnapshots** se encuentra dentro de la ventana Vaciar y mantener. La compatibilidad con el kernel de VSS cancelará el vaciado y la retención que contiene la E/S si la versión posterior no se recibe en 10 segundos y VSS producirá un error en el proceso de creación de instantáneas. Otras actividades se realizarán en el sistema, por lo que un proveedor no debe confiar en tener los 10 segundos completos. El proveedor no debe llamar a las API de Win32 durante la confirmación, ya que muchas darán lugar a escrituras y bloqueos inesperados. Si el proveedor tarda más de unos segundos en completar la llamada, hay una alta probabilidad de que se producirá un error.
-   La secuencia completa de [**PreCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots) a la devolución de [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) se asigna a la ventana entre los escritores que reciben los eventos Freeze y Thaw. El valor predeterminado del sistema de escritura para esta ventana es de 60 segundos, pero un escritor puede invalidar este valor con un tiempo de espera menor. Por ejemplo, el sistema Microsoft Exchange Server escritura cambia el tiempo de espera a 20 segundos. Los proveedores no deben dedicar más de un segundo o dos en este método.

Durante [**CommitSnapshots,**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) el proveedor debe evitar las E/S de archivos que no son de paginación; esta E/S tiene una probabilidad muy alta de interbloqueo. En concreto, el proveedor no debe escribir sincrónicamente ningún registro de depuración o seguimiento.

 

 



