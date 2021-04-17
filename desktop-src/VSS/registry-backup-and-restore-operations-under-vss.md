---
description: El servicio de registro de Windows admite un VSS Writer, denominado escritor del registro, que permite a los solicitantes realizar copias de seguridad de un registro del sistema mediante los datos almacenados en un volumen de copia sombra.
ms.assetid: 94a45b04-0bdc-4211-bed0-caeabba774af
title: Operaciones de copia de seguridad y restauración del registro en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a3022ec2fb08b07bcff8b28455ae7154e4c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696979"
---
# <a name="registry-backup-and-restore-operations-under-vss"></a>Operaciones de copia de seguridad y restauración del registro en VSS

El servicio de registro de Windows admite un VSS Writer, denominado escritor del registro, que permite a los solicitantes realizar copias de seguridad de un registro del sistema mediante los datos almacenados en un volumen de copia sombra. Para obtener más información sobre el sistema de escritura del registro, consulte [escritores de VSS en la caja](in-box-vss-writers.md).

El sistema de escritura del registro realiza copias de seguridad en contexto y restauraciones del registro. Además, el escritor del registro solo informa de los subárboles del sistema; no notifica subárboles de usuario.

**Windows Server 2003:** El sistema de escritura del registro usa un archivo de repositorio intermedio (también conocido como archivo de la media) para almacenar los datos del registro. Además, el escritor del registro informa de los subárboles del sistema y de los subárboles del usuario.

El ID. de escritor del sistema de escritura del registro es AFBAB4A2-367D-4D15-A586-71DBB18F8485.

**Windows XP:** No hay ningún sistema de escritura del registro. El escritor de estado de arranque indica los datos del registro, cuyo identificador de escritor es F2436E37-09F5-41AF-9B2A-4CA2435DBFD5.

> [!Note]  
> Microsoft no proporciona soporte técnico para desarrolladores o profesionales de TI para implementar restauraciones de estado del sistema en línea en Windows (todas las versiones). Para obtener información sobre el uso de las API y los procedimientos proporcionados por Microsoft para implementar restauraciones de estado del sistema en línea, consulte los recursos de la comunidad disponibles en [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).

 

> [!Note]  
> La siguiente información solo se aplica a Windows Server 2003 y Windows XP.

 

## <a name="registry-backup-using-vss"></a>Copia de seguridad del registro mediante VSS

El sistema de escritura del registro exportará y guardará los archivos de registro activos en las ubicaciones definidas por la clave **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **hivelist**.

Los nombres de los valores de esta entrada del registro identifican el subárbol del registro que se va a guardar y los datos del valor proporcionan el archivo que contiene el archivo (el archivo de Hive). Los archivos de Hive se especifican con el siguiente formato: \\ Device \\ *HarddiskVolumeX* \\ *path* \\ *filename*.

Por ejemplo, en **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **control** \\ **hivelist**, puede ver **\\ Registry \\ Machine \\ software**  =  \\ Device \\ HarddiskVolume1 \\ Windows \\ system32 \\ config \\ software.

El sistema de escritura del registro garantiza que los archivos de Hive se guardan en el disco antes de su instantánea.

Al realizar una copia de seguridad de los subárboles del registro, un solicitante reemplazaría el \\ dispositivo \\ *HarddiskVolumeX* por la cadena de [*objeto del dispositivo*](vssgloss-d.md) de la instantánea del volumen.

> [!Note]  
> Puede convertir la \\ ruta de acceso del dispositivo \\ *HarddiskVolumeX* en una ruta de acceso de Win32 equivalente mediante la función [**QueryDosDevice**](/windows/win32/api/fileapi/nf-fileapi-querydosdevicew) . Para obtener más información, vea [obtener un nombre de archivo de un identificador de archivo](../memory/obtaining-a-file-name-from-a-file-handle.md) o [Mostrar los nombres de ruta de acceso del volumen](../fileio/displaying-volume-paths.md).

 

## <a name="registry-restore-using-non-vss-win32-apis"></a>Restauración del registro mediante las API de Win32 que no son VSS

En el caso de una restauración en línea (modo seguro o sistema operativo completo), deben conservarse las subclaves **de la \_ \_** \\  \\  \\  \\  \\  clave del registro.

Las funciones [**MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) y [**MoveFileTransacted**](/windows/win32/api/winbase/nf-winbase-movefiletransacteda) usan esta clave del registro para almacenar información sobre los archivos a los que se ha cambiado el nombre mediante el retardo de MOVEFILE \_ \_ hasta \_ el valor de reinicio en el parámetro *dwFlags* .

Para conservar el contenido de la clave del registro **PendingFileRenameOperations** , la aplicación de copia de seguridad debe llamar a la función [**RegLoadKey**](/windows/win32/api/winreg/nf-winreg-regloadkeya) para conectar el archivo del registro que se va a restaurar en el registro activo. La aplicación de copia de seguridad puede usar las distintas funciones del registro para copiar las claves y los valores deseados en el subárbol cargado. Una vez completada la copia, se debe llamar a las funciones [**RegFlushKey**](/windows/win32/api/winreg/nf-winreg-regflushkey) y [**RegUnloadKey**](/windows/win32/api/winreg/nf-winreg-regunloadkeya) .

En el caso de una restauración sin conexión (entorno de recuperación de Windows o Windows PE), no es necesario respetar la clave del registro **PendingFileRenameOperations** .

## <a name="registry-restore-using-non-vss-win32-apis-in-windows-server-2003"></a>Restauración del registro mediante las API de Win32 que no son de VSS en Windows Server 2003

> [!Note]  
> La siguiente información solo se aplica a las operaciones de restauración relacionadas con la recuperación ante desastres (también denominada reconstrucción completa) que se realizan en Windows Server 2003.

 

Al restaurar el registro, una aplicación de copia de seguridad debe trasladar algunas de las subclaves del registro actual al registro que se va a restaurar.

Para ello, una aplicación de copia de seguridad puede llamar a **RegLoadKey** para conectar el archivo de registro que se va a restaurar en el registro activo actualmente. Después, puede usar las distintas funciones del registro para copiar las claves y los valores deseados en el subárbol cargado. Una vez completada la copia, se llama a **RegFlushKey** y **RegUnloadKey** .

Hay una clave del registro que indica a una aplicación de restauración (solicitante) las claves del registro en **HKEY \_ local \_ Machine \\ System** que no se deben sobrescribir en el momento de la restauración:

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ BackupRestore \\ KeysNotToRestore**

Parte del proceso de restauración del estado del sistema implica la restauración de un registro del que se ha realizado previamente una copia de seguridad.

Las aplicaciones de copia de seguridad deben tener especial cuidado al restaurar el subárbol del **\_ \_ \\ sistema del equipo local HKEY** porque el proceso de instalación de una versión temporal del sistema operativo Windows habrá establecido claves en el subárbol del sistema recién instalado cuyos valores deben sobrevivir a la operación de restauración.

Por ejemplo, cuando el sistema de sustitución tiene una tarjeta de interfaz de red diferente del sistema original, la restauración de las claves originales de la tarjeta anterior dará lugar a resultados imprevisibles. Esto se debe a que el servicio Plug and Play ha detectado y colocado entradas adecuadas del registro del servicio y del controlador en el registro. Estos valores se deben conservar para arrancar correctamente después de restaurar el sistema.

En esta sección se describe cómo las aplicaciones de copia de seguridad pueden detectar qué claves y archivos se conservarán al ejecutar una restauración del subárbol **\_ \_ \\ del sistema del equipo local HKEY** . En algunos casos, esto implica copiar mediante programación las claves del subárbol de instalación recién instalado en el subárbol que se va a restaurar. En otros casos, garantizar que las claves del registro de un producto no se reemplacen es tan sencilla como especificar dichas claves en el archivo de configuración INF del producto.

Las claves (y los datos clave) que se van a conservar se enumeran en el subárbol **\_ \_ \\ del sistema del equipo local HKEY** en el

**HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ BackupRestore \\ KeysNotToRestore**

Key como conjuntos de \_ cadenas reg multi \_ SZ (llamadas *cadenas de clave* en este documento).

Una aplicación de copia de seguridad (solicitante) debe examinar los valores de estas claves en el registro activo y el registro recién restaurado porque cualquier aplicación o servicio puede agregar valores en cualquier momento.

La forma en que las aplicaciones de copia de seguridad van a interpretar las cadenas de clave se determinan mediante el carácter de terminal:

1.  Las cadenas de clave terminadas con una barra diagonal inversa (' \\ ') se interpretan como subclaves. Cuando se encuentra una subcadena de este tipo, la aplicación de copia de seguridad debe conservar todos los datos y todas las claves subordinadas.

    Por ejemplo, lo siguiente especifica que todas las claves y los datos subordinados se conservarán en una operación de restauración:

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Services \\ dmio \\ información de arranque\\**

    Para ello, esta clave y todas las claves y los datos subordinados se deben copiar del registro existente (es decir, el creado por la instalación de Windows) en el registro recién restaurado. Esto se denomina operación de *reemplazo de clave* . Esta operación reemplaza la clave correspondiente en el registro restaurado.

2.  Las cadenas de clave cuyo carácter de terminación es un asterisco (' \* ') especifica que todas las subclaves deben combinarse. Por ejemplo, la cadena de clave:

    **HKEY \_ \_Sistema de equipo local \\ \\ CurrentControlSet \\ \\ \* Services* _

    Especifica que la clave de servicios del registro existente (por ejemplo, los creados por la instalación de Windows) debe combinarse en el registro restaurado. Esto se denomina operación _key Merge * y, si existe una subclave en el subárbol existente y en el subárbol restaurado, la clave del directorio restaurado se conserva con las siguientes excepciones:

    -   Si la subclave del subárbol existente contiene un valor denominado "Start" y la subclave de la restaurada no lo hace.
    -   Si la subclave del subárbol existente y restaurado contiene un valor denominado "Start" y su valor numérico en el subárbol existente es menor.

    El valor "Start" del registro especifica cuándo se iniciará un servicio o un controlador y puede tener un valor numérico de 0-4. Cuanto menor sea el valor, más pronto se iniciará el servicio en el proceso de arranque.

    Si esta clave existe en el directorio existente y en el restaurado, debe examinar el valor de la clave de inicio en cada subárbol. Si el valor del subárbol existente es inferior al valor del directorio restaurado, se debe conservar el valor inferior.

    Una vez más, esta clave se usa para determinar si un servicio o un controlador se va a iniciar en el momento del arranque, en la hora del sistema, de forma manual, automática o deshabilitada. El valor inferior representa una hora de inicio anterior. La hora de inicio anterior debe aplicarse al nuevo registro para asegurarse de que el servicio o los controladores se inician correctamente en el siguiente arranque.

3.  Las cadenas de clave cuyo carácter de terminación no es una barra diagonal inversa ni un asterisco se interpretan como valores del registro que se van a conservar.

    Por ejemplo, la cadena de clave:

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Session Manager \\ PendingFileRenameOperations**

    El mecanismo por el que se pueden conservar las claves mediante programación implica la API del registro de Win32. Por ejemplo, un algoritmo se enumera a continuación:

    1.  Restaure el archivo de subárbol del sistema con copia de seguridad en un archivo. En este ejemplo, deje que el nombre sea System. reg.
    2.  Use **RegLoadKey** para cargar System. reg en **el \_ \_ equipo local HKEY** bajo un nombre temporal. Por ejemplo, un nombre de este tipo podría ser

        **HKEY \_ local \_ Machine \\ TMP \_ System**

    3.  Enumere los valores de la subclave **KeysNotToRestore** de ambas copias del registro y cree un superconjunto de las listas. Copie cada una de estas claves de la existente.

        **HKEY \_ \_ \\ sistema del equipo local**

        clave en el

        **HKEY \_ local \_ Machine \\ TMP \_ System**

        clave según la semántica descrita anteriormente.

    4.  Cuando haya terminado, use los puntos de entrada de **RegFlushKey**  &  **RegUnloadKey** para guardar el

        **HKEY \_ local \_ Machine \\ TMP \_ System**

        Vuelva a System. reg.

    5.  Por último, use **RegReplaceKey** para especificar que System. reg va a reemplazar el

        **HKEY \_ \_ \\ sistema del equipo local**

        archivo de Hive, sistema.

 

 
