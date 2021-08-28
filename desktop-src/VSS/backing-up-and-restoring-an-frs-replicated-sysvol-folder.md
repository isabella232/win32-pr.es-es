---
description: En este tema se explica cómo determinar si DFSR o FSR replica una carpeta SYSVOL y se explica cómo realizar una copia de seguridad y restaurar una carpeta SYSVOL replicada por FRS.
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: Copia de seguridad y restauración de una FRS-Replicated sysvol
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d841f64bab62114824847f91876ba8bbffbb0166db942c0f3cb9d010b72f106
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124605"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a>Copia de seguridad y restauración de una FRS-Replicated sysvol

La carpeta Volumen del sistema (SYSVOL) proporciona una ubicación estándar para almacenar elementos importantes [de](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) directiva de grupo objetos y scripts. Existe una copia de la carpeta SYSVOL en cada controlador de dominio de un dominio. La carpeta SYSVOL se replica mediante Sistema de archivos distribuido [Replication (DFSR)](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) o el Servicio de replicación de archivos [(FRS).](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10)) En este tema se explica cómo determinar si DFSR o FSR replica una carpeta SYSVOL y se explica cómo realizar una copia de seguridad y restaurar una carpeta SYSVOL replicada por FRS.

FRS puede copiar el contenido de SYSVOL en otros controladores de dominio del dominio. FRS supervisa la carpeta SYSVOL y, si se produce un cambio en cualquier archivo almacenado en la carpeta SYSVOL, FRS replica automáticamente el archivo cambiado en las carpetas SYSVOL de los otros controladores de dominio del dominio.

> [!Note]  
> Solo la directiva de grupo se replica mediante la replicación del contenido de la carpeta SYSVOL. El directiva de grupo contenedor se replica mediante Active Directory replicación. Para directiva de grupo funcione correctamente, tanto la plantilla de directiva de grupo como el directiva de grupo contenedor deben estar disponibles en un controlador de dominio.

 

En este tema se tratan los temas siguientes:

-   [Determinar si DFSR o FRS replica la carpeta SYSVOL de un controlador de dominio](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [Copia de seguridad de una DFSR-Replicated sysvol](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [Copia de seguridad de FRS-Replicated carpeta SYSVOL en un Windows Server 2008 o Windows Server 2003](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [Documento de metadatos del escritor de FRS de ejemplo](#sample-frs-writer-metadata-document)
-   [Establecer claves del Registro para una restauración de una FRS-Replicated sysvol](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [Realizar una restauración no autenticativa de un FRS-Replicated sysvol](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [Realizar una restauración autoritativa de FRS-Replicated carpeta SYSVOL](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a>Determinar si DFSR o FRS replica la carpeta SYSVOL de un controlador de dominio

En la tabla siguiente se resume cómo determinar si [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) o FRS replica la carpeta SYSVOL de un controlador de dominio.

| Si el controlador de dominio se está ejecutando                                                                                                                  | SYSVOL se replica mediante |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Windows Server 2008 + nivel funcional de dominio de Windows Server 2008 + [SYSVOL migration](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) completed | DFSR                    |
| Windows Server 2008 + nivel funcional de dominio por debajo Windows Server 2008                                                                              | Frs                     |
| Windows Server 2003                                                                                                                                  | Frs                     |



 

Si el nivel [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) funcional del dominio es Windows Server 2008 y el dominio se ha sometido a la migración [de SYSVOL,](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) se usará para replicar la carpeta SYSVOL. Si el primer controlador de dominio del dominio se promovió directamente [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))en el nivel funcional de Windows Server 2008, DFSR se usa automáticamente para la replicación SYSVOL. En tales casos, no es necesario migrar la replicación SYSVOL de FRS a DFSR. Si el dominio se actualizó al nivel funcional de Windows Server 2008, FRS se usa para la replicación sysvol hasta que se completa el proceso de migración de FRS a DFSR. [](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) [](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx)

Para determinar si DFSR o FRS se usa en un controlador de dominio que ejecuta Windows Server 2008, compruebe el valor de la subclave del Registro **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** \\ **Parameters** \\ **SysVols** \\ **Migrating Sysvols** \\ **LocalState** . Si esta subclave del Registro existe y su valor se establece en 3 (ELIMINATED), [se usa DFSR.](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) Si la subclave no existe o si tiene un valor diferente, se usa FRS.

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a>Copia de seguridad de una DFSR-Replicated sysvol

Si [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)replica la carpeta SYSVOL, se puede usar VSS Writer de DFSR para realizar una copia de seguridad de ella. Para obtener más información sobre el escritor de VSS de DFSR, vea [Carpetas replicadas dfsr](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders).

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a>Copia de seguridad de FRS-Replicated carpeta SYSVOL en un Windows Server 2008 o Windows Server 2003

En un controlador de dominio que ejecuta Windows Server 2008 o Windows Server 2003, la infraestructura de VSS está presente y, por tanto, FRS VSS Writer se puede usar para realizar una copia de seguridad de la carpeta SYSVOL y los componentes de FRS.

El documento de metadatos del escritor de VSS de FRS proporciona información sobre la ubicación de la carpeta SYSVOL y las listas de exclusión para el escritor. En función de esta información, una aplicación de copia de seguridad de VSS (solicitante) puede hacer una copia de seguridad de la carpeta SYSVOL mediante las técnicas de copia de seguridad basadas en VSS normales.

El documento de metadatos del escritor contiene información sobre el escritor, los datos que posee el escritor y cómo restaurar los datos. Se trata de un documento de solo lectura que la aplicación de copia de seguridad puede recuperar antes de realizar una copia de seguridad. La [herramienta DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) se puede usar para ver el documento de metadatos del escritor de VSS de FRS. El [comando DiskShadow list writers](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) proporciona información sobre los escritores presentes en el sistema. Esta lista contiene información sobre el escritor de FRS en controladores de dominio que usan FRS para la replicación SYSVOL o en servidores de archivos que usan FRS para la replicación de [destinos de vínculo DFS.](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10))

En la siguiente sección documento de metadatos del escritor de FRS de ejemplo se muestra un documento de metadatos del escritor de FRS de ejemplo para un controlador de dominio que tiene la carpeta SYSVOL en D: \\ Windows \\ Sysvol. La ruta de acceso que se muestra en la sección "Archivos excluidos" será la misma que la que se obtiene al consultar la clave del Registro **SysVol** del servicio Netlogon:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NetLogon** \\ **Parameters** \\ **SysVol**

La única excepción a esta regla se produce cuando el controlador de dominio está en el estado REDIRIGIDO de [la migración SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx). En este estado, los escritores correspondientes a FRS y al servicio [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) informan de sus respectivas copias de la carpeta SYSVOL. Sin embargo, la copia del servicio [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) de la carpeta SYSVOL (normalmente una carpeta denominada SYSVOL DFSR) es la que comparte el controlador de dominio; esta ruta de acceso es la a la que hace referencia la clave del Registro \_ **SysVol.**

VSS Writer de FRS requiere un método de restauración personalizado. Esto significa que se deben realizar determinados pasos personalizados al restaurar los archivos replicados por FRS. Para obtener más información, vea Realizar una restauración no autenticativa de una FRS-Replicated sysvol.

> [!Note]  
> Las copias de seguridad de estado del sistema para los controladores de dominio de Windows no incluyen la base de datos FRS que mantiene información de estado para el servicio FRS relativa a los archivos dentro de la carpeta SYSVOL y otros conjuntos de contenido. La base de datos FRS, los registros [](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) de depuración, los archivos de área de ensayo y los archivos de la carpeta de datos existentes previamente se excluyen de una copia de seguridad del estado del sistema. La especificación frs writer de ejemplo siguiente contiene la lista de exclusión de la sección "Archivos excluidos".

 

## <a name="sample-frs-writer-metadata-document"></a>Documento de metadatos del escritor de FRS de ejemplo

A continuación se muestra un documento de metadatos del escritor de FRS de ejemplo para un controlador de dominio cuya ruta de acceso de carpeta SYSVOL es D: \\ Windows \\ Sysvol.

``` syntax
* WRITER "FRS Writer"
    - Writer ID   = {d76f5a28-3092-4589-ba48-2958fb88ce29}
    - Writer Instance ID = {07ae58e5-6977-4e34-9dfe-399bbd2cbe40}
    - Supports restore events = FALSE
    - Writer restore conditions = VSS_WRE_NEVER
    - Restore method = VSS_RME_CUSTOM
    - Requires reboot after restore = FALSE

    - Excluded files:
       - Exclude: Path = d:\windows\ntfrs\jet, Filespec = *
       - Exclude: Path = d:\Windows\debug\NtFrs, Filespec = NtFrs*
       - Exclude: Path = d:\windows\sysvol\domain\DO_NOT_REMOVE_NtFrs_PreInstall_Directory, Filespec = *
       - Exclude: Path = d:\windows\sysvol\domain\NtFrs_PreExisting___See_EventLog, Filespec = *
       - Exclude: Path = d:\windows\sysvol\staging\domain, Filespec = NTFRS_*

    - Component "FRS Writer:\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b"
       - Name: 'da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Logical Path: 'SYSVOL'
       - Full Path: '\SYSVOL\da45368c-b2d3-4cf0-bdc338a2cde15a7b'
       - Caption: ''
       - Type: VSS_CT_FILEGROUP [2]
       - Is Selectable: 'TRUE'
       - Is top level: 'TRUE'
       - Notify on backup complete: 'TRUE'
       - Components:
       - File List: Path = d:\windows\sysvol, Filespec = *
       - Affected paths by this component:
         - d:\windows\sysvol
       - Affected volumes by this component:
         - \\?\Volume{da897ba5-5840-11db-93c1-806e6f6e6963}\ [D:\]
       - Component Dependencies:
```

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a>Establecer claves del Registro para una restauración de FRS-Replicated carpeta SYSVOL

La clave del Registro **BurFlags** se usa para realizar restauraciones autoritativas o no autoritativas en miembros FRS de conjuntos de réplicas DFS o SYSVOL. La clave del Registro **BurFlags** global (en todo el equipo) contiene valores REG DWORD y se encuentra en \_ la siguiente ubicación en el Registro:

**HKEY \_ Sistema \_ LOCAL MACHINE** \\  \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters** \\ **Backup/Restore** \\ **Process at Startup**

Los valores más comunes de la clave del Registro **BurFlags** son:

-   D2, también conocido como restauración en modo no autenticativo.
-   D4, también conocido como restauración en modo autoritativo.

Hay claves del Registro **De BurFlags** globales y específicas del conjunto de réplicas. Al establecer la clave del **Registro de BurFlags** global, se reinicializan todos los conjuntos de réplicas que contiene el miembro. Esta clave global debe establecerse cuando el servidor solo contiene un conjunto de réplicas, o cuando los conjuntos de réplicas que contiene son relativamente pocos en número y de tamaño pequeño. Por ejemplo, si el servidor es un controlador de dominio que no hospeda ningún conjunto de contenido que se replique mediante FRS que no sea la carpeta SYSVOL, se puede establecer la clave del Registro **BurFlags** global.

La clave del Registro **de BurFlags** global se encuentra en la siguiente ubicación del registro:

**HKEY \_ Sistema \_ LOCAL MACHINE** \\  \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters** \\ **Backup/Restore** \\ **Process at Startup**

A diferencia de la clave **Global BurFlags,** la clave **BurFlags** específica del conjunto de réplicas permite volver a inicializar conjuntos de réplicas discretos e individuales, lo que permite que los conjuntos de replicación en buen estado se quejen intactos.

Las claves del Registro **BurFlags** específicas del conjunto de réplicas se pueden encontrar determinando el GUID de ese conjunto de réplicas concreto.

En el procedimiento siguiente se describe cómo determinar qué GUID corresponde a un conjunto de réplicas determinado y cómo configurar una restauración.

**Para determinar qué GUID corresponde a un conjunto de réplicas determinado y configurar una restauración**

1.  Detenga el servicio FRS.
2.  Para determinar el GUID que representa un conjunto de réplicas determinado:
    1.  Busque la siguiente clave en el Registro.

        **HKEY \_ Conjunto \_ de réplicas** \\ **de** parámetros de \\  \\  \\ **NtFrs** \\  \\  de Local Machine System CurrentControlSet Services

    2.  Debajo **de la** subclave Conjuntos de réplicas, hay una o varias subclaves identificadas por un GUID.
    3.  El **valor raíz del conjunto de** réplicas para cada GUID es una ruta de acceso del sistema de archivos que indica el conjunto de réplicas representado por este GUID.
    4.  Iteración por esta lista de GUID hasta que se encuentra el conjunto de réplicas deseado. Tenga en cuenta el GUID correspondiente.

3.  Busque la subclave siguiente en el Registro:

    **HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters** \\ **Cumulative Replica Sets**

4.  Debajo de esta subclave, busque el mismo GUID que se anotó en el paso 2. Debajo de la subclave GUID, cree una entrada para la **clave BurFlags.**
5.  Reinicie el servicio FRS.

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Realizar una restauración no autenticativa de un FRS-Replicated sysvol

La restauración no autenticativa es la manera más común de reinicializar la replicación SYSVOL en controladores de dominio individuales. Los controladores de dominio que se restauran de forma no autenticativa deben tener conexiones entrantes desde otros controladores de dominio en funcionamiento, que participan en la replicación de Active Directory y FRS. En un entorno de implementación grande que consta de muchos controladores de dominio, los controladores de dominio restantes se pueden recuperar mediante una restauración en modo no autenticativo en las condiciones siguientes:

-   Debe haber al menos un miembro de réplica correcto conocido (un controlador de dominio con una carpeta SYSVOL en buen estado).
-   Los demás controladores de dominio deben reinicializarse en orden de asociado de replicación directa.

En el procedimiento siguiente se describe cómo realizar una restauración no autenticativa.

**Para realizar una restauración no autoritativa**

1.  Detenga el servicio FRS.
2.  Restaure los datos de copia de seguridad en la carpeta SYSVOL.
3.  Configure la **clave del Registro BurFlags** estableciendo el valor de la siguiente clave del Registro en el valor DWORD D2.

    **HKEY \_ Sistema \_ DE MÁQUINA LOCAL** \\  \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **Parameters** \\ **Backup/Restore** \\ **Process at Startup** \\ **BurFlags**

4.  Reinicie el servicio FRS.

Cuando se reinicia el servicio FRS, se producen las siguientes acciones:

-   El valor de la clave del Registro **BurFlags** se restablece en cero.
-   Los archivos de las carpetas FRS reinicializadas se mueven a una carpeta ya existente.
-   El evento 13565 se registra en el registro de eventos de FRS para indicar que se ha iniciado una restauración no autenticativa.
    > [!Note]  
    > Los códigos de evento FRS se documentan en "Códigos de error del registro de eventos de FRS" en la página ayuda y soporte Knowledge Base en <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

-   Se ha creado la base de datos FRS.
-   El miembro realiza una combinación inicial del conjunto de réplicas desde un  asociado ascendente o desde el equipo especificado en la clave del Registro Principal del conjunto de réplicas si se ha especificado un elemento primario para los conjuntos de réplicas SYSVOL.
-   El equipo reinicializado ejecuta una replicación completa de los conjuntos de réplicas afectados cuando comienza la programación de replicación pertinente.
-   Una vez completado el proceso, se registra un evento 13516 para indicar que FRS está operativo. Si el evento no se registra, hay un problema con la configuración de FRS.

> [!Note]  
> La colocación de archivos en la [carpeta existente](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) previamente en miembros reinicializados es una medida de seguridad en FRS diseñada para evitar la pérdida accidental de datos. Los archivos destinados a la réplica que solo existen en la carpeta local preexistente y que se replicaron después de la replicación inicial se pueden copiar en la carpeta adecuada. Cuando se ha producido la replicación saliente, los archivos de la carpeta existente se pueden eliminar para liberar espacio adicional en la unidad.

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Realizar una restauración autoritativa de una FRS-Replicated sysvol

Las restauraciones autoritativa se usan como último recurso en caso de situaciones críticas, como la divergente de datos en el conjunto de contenido causado por colisiones de directorios. Por ejemplo, es posible que se necesite una restauración autoritativa para restaurar un conjunto de réplicas de FRS en el que la replicación se ha detenido por completo y se requiere una recompilación desde cero.

Si debe realizar una restauración autoritativa de la carpeta SYSVOL, tenga en cuenta que se trata de un proceso muy complicado. Las instrucciones completas que detallan las operaciones que deben realizarse para una restauración autoritativa del contenido de la carpeta SYSVOL se documentan en "Cómo recompilar el árbol SYSVOL y su contenido en un dominio" en la página ayuda y soporte técnico Knowledge Base en <https://go.microsoft.com/fwlink/p/?linkid=117780> .

Se deben cumplir los siguientes requisitos antes de realizar una restauración de FRS autoritativa:

1.  El servicio FRS debe deshabilitarse en todos los asociados de replicación de bajada (directos y transitivos) para la carpeta SYSVOL reinicializada antes de que se haya configurado la restauración autoritativa para que se produzca.
2.  Los eventos 13553 y 13516 se han registrado en el registro de eventos de FRS. Estos eventos indican que la pertenencia del conjunto de réplicas SYSVOL se ha establecido en el controlador de dominio configurado para la restauración autoritativa.
    > [!Note]  
    > Los códigos de evento FRS se documentan en "Códigos de error del registro de eventos de FRS" en la página ayuda y soporte Knowledge Base en <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

3.  El controlador de dominio configurado para la restauración autoritativa está configurado para ser autoritativo para todos los datos SYSVOL que se replicarán en los controladores de dominio restantes.
4.  Todos los demás asociados del conjunto de réplicas deben reinicializarse con una restauración no autenticativa.

 

 
