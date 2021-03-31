---
description: En este tema se explica cómo determinar si DFSR o la copia de seguridad de una carpeta SYSVOL se ha replicado, y se explica cómo realizar copias de seguridad y restaurar una carpeta SYSVOL replicada por FRS.
ms.assetid: 32d8a5bd-eeb4-4db6-8129-b5cd3508a7e5
title: Copia de seguridad y restauración de una FRS-Replicated carpeta SYSVOL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea83ccbc156182a4a3b84c758cb22153f4f7110f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361044"
---
# <a name="backing-up-and-restoring-an-frs-replicated-sysvol-folder"></a>Copia de seguridad y restauración de una FRS-Replicated carpeta SYSVOL

La carpeta volumen del sistema (SYSVOL) proporciona una ubicación estándar para almacenar elementos importantes de [Directiva de grupo](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)) objetos y scripts. Existe una copia de la carpeta SYSVOL en cada controlador de dominio de un dominio. La carpeta SYSVOL se replica mediante [sistema de archivos distribuido replicación (DFSR)](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) o el servicio de [replicación de archivos (FRS)](/previous-versions/windows/it-pro/windows-server-2003/cc781582(v=ws.10)). En este tema se explica cómo determinar si DFSR o la copia de seguridad de una carpeta SYSVOL se ha replicado, y se explica cómo realizar copias de seguridad y restaurar una carpeta SYSVOL replicada por FRS.

FRS puede copiar el contenido de SYSVOL en otros controladores de dominio del dominio. FRS supervisa la carpeta SYSVOL y, si se produce un cambio en cualquier archivo almacenado en la carpeta SYSVOL, FRS replica automáticamente el archivo cambiado en las carpetas SYSVOL de los otros controladores de dominio del dominio.

> [!Note]  
> Solo la plantilla de directiva de grupo se replica mediante la replicación del contenido de la carpeta SYSVOL. El contenedor de directiva de grupo se replica a través de la replicación de Active Directory. Para que directiva de grupo funcione correctamente, tanto la plantilla de directiva de grupo como el contenedor de directiva de grupo deben estar disponibles en un controlador de dominio.

 

En este tema se tratan los siguientes temas:

-   [Determinar si DFSR o FRS Replica la carpeta SYSVOL de un controlador de dominio](#determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs)
-   [Copia de seguridad de un DFSR-Replicated carpeta SYSVOL](#backing-up-a-dfsr-replicated-sysvol-folder)
-   [Copia de seguridad de un FRS-Replicated carpeta SYSVOL en un dominio de Windows Server 2008 o Windows Server 2003](#backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain)
-   [Documento de metadatos de ejemplo FRS Writer](#sample-frs-writer-metadata-document)
-   [Establecer claves del registro para una restauración de una FRS-Replicated carpeta SYSVOL](#setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder)
-   [Realizar una restauración no autoritativa de una FRS-Replicated carpeta SYSVOL](#performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder)
-   [Realización de una restauración autoritativa de un FRS-Replicated carpeta SYSVOL](#performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder)

## <a name="determining-whether-a-domain-controllers-sysvol-folder-is-replicated-by-dfsr-or-frs"></a>Determinar si DFSR o FRS Replica la carpeta SYSVOL de un controlador de dominio

En la tabla siguiente se resume cómo determinar si [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) o FRS está replicando la carpeta Sysvol de un controlador de dominio.

| Si el controlador de dominio se está ejecutando                                                                                                                  | SYSVOL replica el |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| Windows Server 2008 + nivel funcional de dominio de Windows Server 2008 + [migración de SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) completado | DFSR                    |
| Windows Server 2008 + nivel funcional del dominio bajo Windows Server 2008                                                                              | FRS                     |
| Windows Server 2003                                                                                                                                  | FRS                     |



 

Si el [nivel funcional](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10)) del dominio es Windows Server 2008 y el dominio se ha sometido a la [migración de SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx), se usará [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) para replicar la carpeta Sysvol. Si el primer controlador de dominio del dominio se promovió directamente al [nivel funcional](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))de Windows Server 2008, DFSR se utiliza automáticamente para la replicación de SYSVOL. En tales casos, no es necesario migrar la replicación de SYSVOL de FRS a DFSR. Si el dominio se ha actualizado al [nivel funcional](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754918(v=ws.10))de Windows Server 2008, se usa FRS para la replicación de SYSVOL hasta que finalice el proceso de [migración](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx) de FRS a DFSR.

Para determinar si se está usando DFSR o FRS en un controlador de dominio que ejecuta Windows Server 2008, compruebe el valor de la subclave del registro **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **DFSR** de SYSVOL \\  \\  \\ **Migrating sysvols** \\ **LocalState** Si esta subclave del registro existe y su valor se establece en 3 (eliminado), se utiliza [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) . Si la subclave no existe o tiene un valor diferente, se usa FRS.

## <a name="backing-up-a-dfsr-replicated-sysvol-folder"></a>Copia de seguridad de un DFSR-Replicated carpeta SYSVOL

Si [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr)Replica la carpeta Sysvol, el VSS Writer de DFSR se puede usar para realizar una copia de seguridad. Para obtener más información acerca de la VSS Writer de DFSR, vea [carpetas replicadas de DFSR](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders).

## <a name="backing-up-an-frs-replicated-sysvol-folder-on-a-windows-server-2008-or-windows-server-2003-domain"></a>Copia de seguridad de un FRS-Replicated carpeta SYSVOL en un dominio de Windows Server 2008 o Windows Server 2003

En un controlador de dominio que ejecuta Windows Server 2008 o Windows Server 2003, la infraestructura de VSS está presente y, por lo tanto, se puede usar la VSS Writer FRS para realizar una copia de seguridad de la carpeta SYSVOL y de los componentes FRS.

El documento de metadatos del escritor de VSS Writer FRS proporciona información sobre la ubicación de la carpeta SYSVOL y las listas de exclusión para el escritor. En función de esta información, una aplicación de copia de seguridad de VSS (solicitante) puede realizar una copia de seguridad de la carpeta SYSVOL mediante las técnicas normales de copia de seguridad basadas en VSS.

El documento de metadatos del escritor contiene información sobre el escritor, los datos que posee el escritor y cómo restaurarlos. Se trata de un documento de solo lectura que puede ser recuperado por la aplicación de copia de seguridad antes de realizar una copia de seguridad. La herramienta [DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) se puede usar para ver el documento de metadatos del escritor del VSS Writer de FRS. El comando [escritores de lista de DiskShadow](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc772172(v=ws.11)) proporciona información sobre los escritores presentes en el sistema. Esta lista contiene información acerca del escritor de FRS en controladores de dominio que usan FRS para la replicación de SYSVOL o en servidores de archivos que usan FRS para la replicación de [destinos de vínculo DFS](/previous-versions/windows/it-pro/windows-server-2003/cc782417(v=ws.10)).

En la siguiente sección del documento de metadatos de ejemplo FRS Writer se muestra un documento de metadatos de ejemplo FRS Writer para un controlador de dominio que tiene la carpeta SYSVOL en D: \\ Windows \\ SYSVOL. La ruta de acceso que se muestra en la sección "archivos excluidos" será la misma que la que se obtiene al consultar la clave del registro **SYSVOL** del servicio NetLogon:

**HKEY \_ \_Equipo local** \\ **sistema** \\ **CurrentControlSet** \\ **servicios** \\ **Netlogon** \\ **parámetros** \\ **SYSVOL**

La única excepción a esta regla se produce cuando el controlador de dominio se encuentra en el estado REDIRIGIDO de la [migración de SYSVOL](https://blogs.technet.com/filecab/archive/2008/02/08/sysvol-migration-series-part-1-introduction-to-the-sysvol-migration-process.aspx). En este estado, los escritores correspondientes a FRS y al servicio [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) notifican sus copias respectivas de la carpeta Sysvol. Sin embargo, la copia del servicio [DFSR](/windows-server/storage/dfs-replication/migrate-sysvol-to-dfsr) de la carpeta Sysvol (normalmente una carpeta denominada SYSVOL \_ DFSR) es la que comparte el controlador de dominio; esta ruta de acceso es la que hace referencia a la clave del registro **SYSVOL** .

El VSS Writer FRS requiere un método de restauración personalizado. Esto significa que se deben realizar determinados pasos personalizados al restaurar los archivos replicados por FRS. Para obtener más información, consulte realizar una restauración no autoritativa de una FRS-Replicated carpeta SYSVOL.

> [!Note]  
> Las copias de seguridad del estado del sistema de los controladores de dominio de Windows no incluyen la base de datos de FRS que mantiene información de estado del servicio FRS que pertenece a los archivos de la carpeta SYSVOL y otros conjuntos de contenido. La base de datos FRS, los registros de depuración, los archivos del área de ensayo y los archivos de la [carpeta de datos preexistentes](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) se excluyen de una copia de seguridad del estado del sistema. La siguiente especificación del escritor FRS de ejemplo contiene la lista de exclusión en la sección "archivos excluidos".

 

## <a name="sample-frs-writer-metadata-document"></a>Documento de metadatos de ejemplo FRS Writer

A continuación se muestra un documento de metadatos de ejemplo FRS Writer para un controlador de dominio cuya ruta de carpeta SYSVOL es D: \\ Windows \\ SYSVOL.

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

## <a name="setting-registry-keys-for-a-restore-of-an-frs-replicated-sysvol-folder"></a>Establecer claves del registro para una restauración de una FRS-Replicated carpeta SYSVOL

La clave del registro **BurFlags** se usa para realizar restauraciones autoritativas o no autoritativas en miembros FRS de conjuntos de réplicas DFS o SYSVOL. La clave del registro **BurFlags** global (todo el equipo) contiene \_ valores de REG DWORD y se encuentra en la siguiente ubicación del registro:

**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **parámetros** \\ **backup/restore** \\ **Process en el inicio**

Los valores más comunes para la clave del registro **BurFlags** son:

-   D2, también conocido como restauración en modo no autoritativo.
-   D4, también conocido como restauración en modo autoritativo.

Hay claves de registro de **BurFlags** globales y específicas del conjunto de réplicas. Al establecer la clave del registro **BurFlags** global se reinicializan todos los conjuntos de réplicas que contiene el miembro. Esta clave global debe establecerse cuando el servidor solo contiene un conjunto de réplicas, o cuando los conjuntos de réplicas que contiene son relativamente pocos en número y reducido en tamaño. Por ejemplo, si el servidor es un controlador de dominio que no hospeda ningún conjunto de contenido que se replique con FRS distinto de la carpeta SYSVOL, se puede establecer la clave del registro **BurFlags** global.

La clave del registro **BurFlags** global se encuentra en la siguiente ubicación del registro:

**HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **parámetros** \\ **backup/restore** \\ **Process en el inicio**

A diferencia de la clave **BurFlags** global, la clave **BurFlags** específica del conjunto de réplicas permite la reinicialización de conjuntos discretos de réplica individuales, lo que permite dejar intactos los conjuntos de replicación correctos.

Las claves del registro de **BurFlags** específicas del conjunto de réplicas se pueden encontrar determinando el GUID para ese conjunto de réplicas concreto.

En el procedimiento siguiente se describe cómo determinar qué GUID corresponde a un conjunto de réplicas determinado y se describe cómo configurar una restauración.

**Para determinar qué GUID corresponde a un conjunto de réplicas determinado y para configurar una restauración**

1.  Detenga el servicio FRS.
2.  Para determinar el GUID que representa un conjunto de réplicas determinado:
    1.  Busque la clave siguiente en el registro.

        **HKEY \_ \_Equipo local** \\ **sistema** \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **parámetros** \\ **conjuntos de réplicas**

    2.  Debajo de la subclave **conjuntos de réplicas** hay una o más subclaves identificadas por un GUID.
    3.  El valor **raíz del conjunto de réplicas** para cada GUID es una ruta de acceso del sistema de archivos que indica el conjunto de réplicas representado por este GUID.
    4.  Recorra en iteración esta lista de GUID hasta que se encuentre el conjunto de réplicas deseado. Tenga en cuenta el GUID correspondiente.

3.  Busque la siguiente subclave en el registro:

    **HKEY \_ Sistema \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **parámetros** \\ **conjuntos de réplicas acumulados**

4.  Debajo de esta subclave, busque el mismo GUID que anotó en el paso 2. Debajo de la subclave GUID, cree una entrada para la clave **BurFlags** .
5.  Reinicie el servicio FRS.

## <a name="performing-a-nonauthoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Realizar una restauración no autoritativa de una FRS-Replicated carpeta SYSVOL

La restauración no autoritativa es la forma más común de reinicializar la replicación de SYSVOL en controladores de dominio individuales. Los controladores de dominio que se restauran de forma no autoritativa deben tener conexiones entrantes de otros controladores de dominio en funcionamiento que participen en la replicación de Active Directory y FRS. En un entorno de implementación grande que consta de muchos controladores de dominio, los controladores de dominio restantes se pueden recuperar mediante una restauración en modo no autoritativa en las siguientes condiciones:

-   Debe haber al menos un miembro de la réplica válida conocida (un controlador de dominio con una carpeta SYSVOL correcta).
-   Los demás controladores de dominio se deben reinicializar en el orden de asociados de replicación directa.

En el procedimiento siguiente se describe cómo realizar una restauración no autoritativa.

**Para realizar una restauración no autoritativa**

1.  Detenga el servicio FRS.
2.  Restaure los datos de la copia de seguridad en la carpeta SYSVOL.
3.  Configure la clave del registro **BurFlags** estableciendo el valor de la siguiente clave del registro en el valor de DWORD D2.

    **HKEY \_ Sistema de \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\ **NtFrs** \\ **parámetros** \\ **backup/restore** \\ **Process en Startup** \\ **BurFlags**

4.  Reinicie el servicio FRS.

Cuando se reinicia el servicio FRS, se producen las siguientes acciones:

-   El valor de la clave del registro **BurFlags** se restablece en cero.
-   Los archivos de las carpetas FRS reinicializadas se mueven a una carpeta existente previamente.
-   El evento 13565 se registra en el registro de eventos de FRS para indicar que se ha iniciado una restauración no autoritativa.
    > [!Note]  
    > Los códigos de evento FRS se documentan en "códigos de error del registro de eventos FRS" en la Knowledge base de ayuda y soporte técnico en <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

-   Se vuelve a generar la base de datos de FRS.
-   El miembro realiza una combinación inicial del conjunto de réplicas de un asociado que precede en la cadena o del equipo que se especifica en la clave del registro **principal del conjunto de réplicas** si se ha especificado un elemento primario para conjuntos de réplicas de SYSVOL.
-   El equipo reinicializado ejecuta una replicación completa de los conjuntos de réplicas afectados cuando comienza la programación de replicación correspondiente.
-   Una vez completado el proceso, se registra un evento 13516 para indicar que FRS está operativo. Si el evento no se registra, existe un problema con la configuración de FRS.

> [!Note]  
> La colocación de los archivos en la carpeta [preexistente](/previous-versions/windows/it-pro/windows-server-2003/cc758169(v=ws.10)) en los miembros reinicializados es una protección en FRS que está diseñada para evitar la pérdida accidental de datos. Los archivos destinados a la réplica que solo existen en la carpeta local existente y que se replicaron después de la replicación inicial se pueden copiar en la carpeta adecuada. Cuando se produce la replicación de salida, se pueden eliminar los archivos de la carpeta existente previamente para liberar espacio adicional en la unidad.

 

## <a name="performing-an-authoritative-restore-of-an-frs-replicated-sysvol-folder"></a>Realización de una restauración autoritativa de un FRS-Replicated carpeta SYSVOL

Las restauraciones autoritativas se usan como último recurso en caso de situaciones críticas como la divergencia de los datos en el conjunto de contenido causados por colisiones de directorio. Por ejemplo, podría ser necesario realizar una restauración autoritativa para restaurar un conjunto de réplicas de FRS en el que se ha detenido por completo la replicación y se requiere una recompilación desde cero.

Si debe realizar una restauración autoritativa de la carpeta SYSVOL, tenga en cuenta que es un proceso muy complicado. Las instrucciones completas que detallan las operaciones que deben realizarse para una restauración autoritativa del contenido de la carpeta SYSVOL se documentan en "Cómo volver a generar el árbol SYSVOL y su contenido en un dominio" en la base de conocimiento de ayuda y soporte técnico en <https://go.microsoft.com/fwlink/p/?linkid=117780> .

Deben cumplirse los siguientes requisitos antes de realizar una restauración de FRS autoritativa:

1.  El servicio FRS debe estar deshabilitado en todos los asociados de replicación de nivel inferior (directos y transitivos) de la carpeta SYSVOL reinicializada antes de que se haya configurado la restauración autoritativa.
2.  Los eventos 13553 y 13516 se han registrado en el registro de eventos de FRS. Estos eventos indican que se ha establecido la pertenencia al conjunto de réplicas de SYSVOL en el controlador de dominio configurado para la restauración autoritativa.
    > [!Note]  
    > Los códigos de evento FRS se documentan en "códigos de error del registro de eventos FRS" en la Knowledge base de ayuda y soporte técnico en <https://go.microsoft.com/fwlink/p/?linkid=117779>

     

3.  El controlador de dominio que está configurado para la restauración autoritativa está configurado para ser autoritativo para todos los datos de SYSVOL que se van a replicar en los controladores de dominio restantes.
4.  Todos los demás asociados del conjunto de réplicas se deben reinicializar con una restauración no autoritativa.

 

 
