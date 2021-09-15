---
description: El Windows Registry Service admite vss writer, denominado escritor del registro, que permite a los solicitantes hacer una copia de seguridad de un registro del sistema mediante los datos almacenados en un volumen de instantáneas.
ms.assetid: 94a45b04-0bdc-4211-bed0-caeabba774af
title: Operaciones de copia de seguridad y restauración del Registro en VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db1a3022ec2fb08b07bcff8b28455ae7154e4c40
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473353"
---
# <a name="registry-backup-and-restore-operations-under-vss"></a>Operaciones de copia de seguridad y restauración del Registro en VSS

El Windows Registry Service admite vss writer, denominado escritor del registro, que permite a los solicitantes hacer una copia de seguridad de un registro del sistema mediante los datos almacenados en un volumen de instantáneas. Para obtener más información sobre el escritor del Registro, vea [In-Box VSS Writers](in-box-vss-writers.md).

El sistema de escritura del Registro realiza copias de seguridad y restauraciones locales del registro. Además, el escritor del Registro solo notifica los subárboles del sistema; no informa de los subárboles de usuario.

**Windows Server 2003:** El escritor del registro usa un archivo de repositorio intermedio (también conocido como archivo de extensión) para almacenar los datos del Registro. Además, el escritor del Registro notifica los subárboles del sistema y los subárboles de usuario.

El identificador de escritor del escritor del registro es AFBAB4A2-367D-4D15-A586-71DBB18F8485.

**Windows XP:** No hay ningún sistema de escritura del Registro. El escritor de estado de arranque notifica los datos del Registro, cuyo identificador de escritor es F2436E37-09F5-41AF-9B2A-4CA2435DBFD5.

> [!Note]  
> Microsoft no proporciona soporte técnico para desarrolladores ni profesionales de TI para implementar restauraciones de estado del sistema en línea Windows (todas las versiones). Para obtener información sobre el uso de api y procedimientos proporcionados por Microsoft para implementar restauraciones de estado del sistema en línea, vea los recursos de la comunidad disponibles en [MSDN Community Center](https://msdn.microsoft.com/community/default.aspx).

 

> [!Note]  
> La siguiente información solo se aplica a Windows Server 2003 y Windows XP.

 

## <a name="registry-backup-using-vss"></a>Copia de seguridad del Registro mediante VSS

El escritor del Registro exportará y guardará los archivos del Registro activos en las ubicaciones definidas por la clave **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **hivelist**.

Los nombres de los valores de esta entrada del Registro identifican el subárbol del Registro que se va a guardar y los datos del valor proporcionan el archivo que contiene el archivo (el archivo de Hive). Los archivos de Hive se especifican con el formato siguiente: Device \\ \\ *HarddiskVolumeX* \\ *path* \\ *filename*.

Por ejemplo, en **HKEY \_ LOCAL \_ MACHINE** System CurrentControlSet Control hivelist , es posible que vea \\  \\  \\  \\ REGISTRY **\\ MACHINE \\ \\ SOFTWARE**  =  \\ Device \\ HarddiskVolume1 \\ Windows \\ System32 \\ config \\ SOFTWARE.

El sistema de escritura del Registro garantiza que los archivos de Hive se guardan en el disco antes de su instantánea.

Al hacer una copia de seguridad de los subárboles del Registro, un solicitante reemplazaría \\ Device \\ *HarddiskVolumeX* [](vssgloss-d.md) por la cadena de objeto de dispositivo de la instantánea del volumen.

> [!Note]  
> Puede convertir la ruta \\ de \\ *acceso Device HarddiskVolumeX* en una ruta de acceso win32 equivalente mediante la función [**QueryDosDevice.**](/windows/win32/api/fileapi/nf-fileapi-querydosdevicew) Para obtener más información, vea [Obtener un nombre de archivo a partir de](../memory/obtaining-a-file-name-from-a-file-handle.md) un identificador de archivo o Mostrar nombres de ruta de acceso de [volumen.](../fileio/displaying-volume-paths.md)

 

## <a name="registry-restore-using-non-vss-win32-apis"></a>Restauración del Registro mediante API win32 que no son de VSS

Para una restauración en línea (modo seguro o sistema operativo completo), se deben conservar las subclaves de la clave del Registro **HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Control** \\ **Session Manager** \\ **PendingFileRenameOperations.**

Las [**funciones MoveFileEx**](/windows/win32/api/winbase/nf-winbase-movefileexa) y [**MoveFileTransacted**](/windows/win32/api/winbase/nf-winbase-movefiletransacteda) usan esta clave del Registro para almacenar información sobre los archivos cuyo nombre se ha cambiado mediante el valor MOVEFILE DELAY UNTIL REBOOT del \_ parámetro \_ \_ *dwFlags.*

Para conservar el contenido de la clave del Registro **PendingFileRenameOperations,** la aplicación de copia de seguridad debe llamar a la [**función RegLoadKey**](/windows/win32/api/winreg/nf-winreg-regloadkeya) para conectar el archivo del Registro que se va a restaurar en el registro activo. A continuación, la aplicación de copia de seguridad puede usar las distintas funciones del Registro para copiar las claves y los valores deseados en el subárbol cargado. Una vez completada la copia, se debe llamar a las funciones [**RegFlushKey**](/windows/win32/api/winreg/nf-winreg-regflushkey) y [**RegUnloadKey.**](/windows/win32/api/winreg/nf-winreg-regunloadkeya)

Para una restauración sin conexión (Windows Recovery Environment o Windows PE), no es necesario respetar la clave del Registro **PendingFileRenameOperations.**

## <a name="registry-restore-using-non-vss-win32-apis-in-windows-server-2003"></a>Restauración del Registro mediante API Win32 que no son de VSS en Windows Server 2003

> [!Note]  
> La siguiente información solo se aplica a las operaciones de restauración relacionadas con la recuperación ante desastres (también conocidas como recuperación sin sistema operativo) que se realizan en Windows Server 2003.

 

Al restaurar el registro, una aplicación de copia de seguridad debe mover algunas de las subclaves del registro actual al registro que se va a restaurar.

Para ello, una aplicación de copia de seguridad puede llamar a **RegLoadKey** para conectar el archivo del Registro que se va a restaurar en el registro actualmente activo. A continuación, puede usar las distintas funciones del Registro para copiar las claves y los valores deseados en el subárbol cargado. Una vez completada la copia, se llama a **RegFlushKey** **y RegUnloadKey.**

Hay una clave del Registro que indica a una aplicación de restauración (solicitante) las claves del Registro en **HKEY \_ LOCAL MACHINE \_ \\ SYSTEM** que no deben sobrescribirse en el momento de la restauración:

**HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ BackupRestore \\ KeysNotToRestore**

Parte del proceso de restauración del estado del sistema implica la restauración de un registro de copia de seguridad previamente.

Las aplicaciones de copia de seguridad deben tener especial cuidado al restaurar el subárbol **HKEY \_ LOCAL MACHINE \_ \\ SYSTEM** porque el proceso de instalación de una versión temporal del sistema operativo Windows tendrá claves establecidas en el subárbol del sistema recién instalado cuyos valores deben sobrevivir a la operación de restauración.

Por ejemplo, cuando el sistema de reemplazo tiene una tarjeta de interfaz de red diferente del sistema original, la restauración de las claves originales de la tarjeta anterior dará lugar a resultados impredecibles. Esto se debe a que Plug and Play servicio ha detectado y colocado entradas del registro de controlador y de servicio adecuadas en el registro. Estos valores deben conservarse para arrancar correctamente después de la restauración del sistema.

En esta sección se describe cómo las aplicaciones de copia de seguridad pueden detectar qué claves y archivos se conservarán al ejecutar una restauración del subárbol **HKEY \_ LOCAL MACHINE \_ \\ SYSTEM.** En algunos casos, esto implicará copiar mediante programación las claves del subárbol de instalación recién instalado en el subárbol que se va a restaurar. En otros casos, asegurarse de que no se reemplazan las claves del Registro de un producto es tan sencillo como especificar dichas claves en el archivo de configuración INF del producto.

Las claves (y los datos de clave) que se van a conservar se enumeran en el subárbol **HKEY \_ LOCAL MACHINE \_ \\ SYSTEM** en el

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ BackupRestore \\ KeysNotToRestore**

key como conjuntos de cadenas REG \_ MULTI \_ SZ *(denominadas cadenas de clave* en este documento).

Una aplicación de copia de seguridad (solicitante) debe examinar los valores de estas claves en el registro activo y en el registro recién restaurado, ya que cualquier aplicación o servicio puede agregar valores en cualquier momento.

La forma en que las aplicaciones de copia de seguridad interpretan las cadenas de clave viene determinada por su carácter terminal:

1.  Las cadenas de clave terminadas con una barra diagonal inversa (' \\ ') se interpretan como subclaves. Cuando se encuentra una subcadena de este tipo, la aplicación de copia de seguridad debe conservar todos los datos y todas las claves subordinadas.

    Por ejemplo, lo siguiente especifica que todas las claves y datos subordinados se conservarán en una operación de restauración:

    **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Services \\ dmio boot \\ info\\**

    Con este fin, esta clave y todos los datos y claves subordinadas deben copiarse del registro existente (es decir, el que creó la instalación de Windows) en el registro recién restaurado. Esto se denomina operación *de reemplazo de* clave. Esta operación reemplaza la clave correspondiente en el Registro restaurado.

2.  Las cadenas de clave cuyo carácter de terminación es un asterisco (' ') especifica que se deben combinar todas \* las subclaves. Por ejemplo, la cadena de clave:

    **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Services\\\***

    especifica que la clave de servicios del registro existente (por ejemplo, las creadas por la instalación de Windows) debe combinarse en el registro restaurado. Esto se denomina *operación* de combinación de claves y, si existe una subclave tanto en el subárbol existente como en el subárbol restaurado, la clave del directorio restaurado se conserva con las siguientes excepciones:

    -   Si la subclave del subclave existente contiene un valor denominado "start" y la subclave de la restaurada no.
    -   Si la subclave del subárbol existente y restaurado contiene un valor denominado "start" y su valor numérico en el subárbol existente es menor.

    El valor "start" del Registro especifica cuándo se iniciará un servicio o controlador y puede tener un valor numérico entre 0 y 4. Cuanto menor es el valor, antes del proceso de arranque se iniciará el servicio.

    Si esta clave existe en el directorio existente y en el directorio restaurado, debe examinar el valor de la clave de inicio en cada subárbol. Si el valor del subárbol existente es inferior al valor del directorio restaurado, se debe conservar el valor inferior.

    Una vez más, esta clave se usa para determinar si un servicio o controlador se debe iniciar en tiempo de arranque, en tiempo del sistema, manualmente, automáticamente o deshabilitarse. El valor inferior representa una hora de inicio anterior. La hora de inicio anterior debe aplicarse al nuevo registro para asegurarse de que el servicio o los controladores se inician correctamente en el siguiente arranque.

3.  Las cadenas de clave cuyo carácter de terminación no es una barra diagonal inversa ni un asterisco se interpretan como valores del Registro que se van a conservar.

    Por ejemplo, la cadena de clave:

    **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Session Manager \\ PendingFileRenameOperations**

    El mecanismo por el que se pueden conservar las claves mediante programación implica la API del registro win32. Por ejemplo, a continuación se enumera un algoritmo:

    1.  Restaure el archivo de Hive del sistema de copia de seguridad en un archivo. En este ejemplo, deje que el nombre sea System.reg.
    2.  Use **RegLoadKey para** cargar System.reg en **HKEY LOCAL \_ \_ MACHINE** con un nombre temporal. Por ejemplo, un nombre de este tipo podría ser

        **HKEY \_ LOCAL \_ MACHINE \\ TMP \_ SYSTEM**

    3.  Enumerar los valores de la subclave **KeysNotToRestore** de ambas copias del Registro y crear un superconjunto de las listas. Copie cada una de estas claves de la existente.

        **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM**

        clave en el

        **HKEY \_ LOCAL \_ MACHINE \\ TMP \_ SYSTEM**

        clave según la semántica descrita anteriormente.

    4.  Cuando haya terminado, **use los puntos de entrada RegFlushKey**  &  **RegUnloadKey** para guardar

        **HKEY \_ LOCAL \_ MACHINE \\ TMP \_ SYSTEM**

        vuelva a la clave a System.reg.

    5.  Por último, **use RegReplaceKey para** especificar que System.reg va a reemplazar a .

        **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM**

        archivo hive, SYSTEM.

 

 
