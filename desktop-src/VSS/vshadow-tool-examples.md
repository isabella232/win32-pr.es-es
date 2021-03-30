---
description: 'Más información sobre: ejemplos de herramientas de VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Ejemplos de la herramienta VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65fd2bfa1c390b1bd5310cd80f02e029dbf935f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809829"
---
# <a name="vshadow-tool-examples"></a>Ejemplos de la herramienta VShadow

En los siguientes ejemplos se muestra cómo usar la herramienta VShadow para realizar las tareas más comunes:

-   [Obtener acceso a las propiedades de instantánea desde un script CMD](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [Obtener acceso a instantáneas no persistentes](#accessing-nonpersistent-shadow-copies)
-   [Copiar un archivo de una instantánea](#copying-a-file-from-a-shadow-copy)
-   [Enumerar todos los archivos de un dispositivo de instantánea](#enumerating-all-files-on-a-shadow-copy-device)
-   [Importar una instantánea transportable](#importing-a-transportable-shadow-copy)
-   [Incluir escritores o componentes](#including-writers-or-components)
-   [Exclusión de escritores o componentes](#excluding-writers-or-components)
-   [Romper conjuntos de instantáneas mediante el método BreakSnapshotSetEx](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

Para obtener una lista completa de las opciones de línea de comandos y su uso, vea [herramienta y ejemplo de VShadow](vshadow-tool-and-sample.md).

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>Obtener acceso a las propiedades de instantánea desde un script CMD

Si usa la marca opcional **-script** al crear instantáneas, VShadow crea un archivo de script cmd que contiene variables de entorno relacionadas con las instantáneas recién creadas, como las siguientes:

-   El identificador del conjunto de instantáneas, que se almacena en la \_ variable de entorno% VSHADOW set \_ ID%
-   Los identificadores de instantánea, que se almacenan en variables con el formato% VSHADOW \_ ID \_ *nnn*%, donde *nnn* representa el índice del volumen de origen en la línea de comandos de VSHADOW
-   Los nombres de los dispositivos de instantáneas, que se almacenan en variables de la forma% VSHADOW \_ dispositivo \_ *nnn*%, donde *nnn* es el índice del volumen de origen en la línea de comandos de VSHADOW

Puede usar el archivo CMD generado para realizar operaciones de administración limitadas en las instantáneas.

> [!Note]  
> El evento [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) Writer se envía después de ejecutar el script **-exec** . VSS llama al método **IVssBackupComponents:: BackupComplete** para indicar a los escritores que la copia de seguridad se ha completado y los escritores pueden truncar los registros en este momento. Por lo tanto, es importante comprobar que la instantánea o copia de seguridad se completó realmente. Si se produjo un error en la copia de seguridad, puede cancelar el proceso de creación devolviendo un código de salida distinto de cero en el script o comando ejecutado. (Consulte la documentación del comando exit en la referencia de la [línea de comandos de Windows](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11))). Si el comando personalizado devuelve un código de salida distinto de cero, se cancela la creación de la instantánea y no se llamará a **IVssBackupComponents:: BackupComplete** .

 

En el ejemplo siguiente se muestra cómo crear una instantánea persistente desde la línea de comandos y usar el script CMD para exponerla.

1.  **vshadow-p-NW-script = SETVAR1. cmd c:**
2.  **llamar a SETVAR1. cmd**
3.  **C: \\>vshadow-el =% vshadow \_ ID. \_ 1%, c: \\ directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>Obtener acceso a instantáneas no persistentes

Las instantáneas no persistentes se eliminan automáticamente cuando se cierra el programa que las crea (en este caso, VShadow). Para tener acceso al contenido de estas instantáneas, VShadow le permite ejecutar un script una vez creadas las instantáneas, pero antes de que se cierre el programa VShadow.

En el ejemplo siguiente se muestra cómo usar la opción de línea de comandos-Exec para ejecutar un script denominado "enum. cmd":

**vshadow-NW-exec = enum. cmd c:**

En el script ejecutado, también puede ejecutar el script SETVAR generado en este comando personalizado. Esto permite que el script tenga acceso directamente al contenido de las instantáneas. Recuerde que el dispositivo de instantáneas se puede recuperar de la variable de entorno VSHADOW del \_ dispositivo \_ nnn.

Este es un ejemplo de script enum. cmd:

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

Esta es la línea de comandos para ejecutar el script enum. cmd:

**vshadow-NW-exec = c: \\ enum. cmd-script = setvar1. cmd c:**

## <a name="copying-a-file-from-a-shadow-copy"></a>Copiar un archivo de una instantánea

En el ejemplo siguiente se muestra cómo copiar un archivo de una instantánea.

1.  **DIR > c: \\somefile.txt**
2.  **vshadow-p-NW-script = SETVAR1. cmd c:**
3.  **llamar a SETVAR1. cmd**
4.  **copia% VSHADOW \_ dispositivo \_ 1% \\somefile.txt c: \\ somefile \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>Enumerar todos los archivos de un dispositivo de instantánea

En el ejemplo siguiente se muestra cómo enumerar todos los archivos de un dispositivo de instantáneas desde un archivo por lotes.

1.  **DIR > c: \\somefile.txt**
2.  **vshadow-p-NW-script = SETVAR1. cmd c:**
3.  **llamar a SETVAR1. cmd**
4.  **en el caso de/R% VSHADOW \_ dispositivo \_ 1% \\ %% i en ( \* ) haga @echo %% i**

## <a name="importing-a-transportable-shadow-copy"></a>Importar una instantánea transportable

Para crear una instantánea transportable en un equipo e importarlo en otro equipo, debe tener dos equipos conectados (a través de una configuración de SAN) a una matriz de almacenamiento que admita instantáneas de hardware de VSS. Debe haber un proveedor de hardware de VSS instalado en cada equipo.

En el ejemplo siguiente se muestra cómo crear e importar la instantánea.

1.  Cree el conjunto de instantáneas en el equipo A (el servidor de producción) escribiendo el siguiente comando después del símbolo del sistema:

    **vshadow-p-t =bc1.xml**

    Esto no expondrá ningún dispositivo de instantáneas en el equipo A.

2.  Copie el documento componentes de copia de seguridad (bc1.xml) del equipo a al equipo B.
3.  Para importar el conjunto de instantáneas en el equipo B, escriba el siguiente comando:

    **vshadow-i =bc1.xml**

Opcionalmente, puede exponer estas instantáneas como Letras de unidad o carpetas montadas. Además, podría romper el conjunto de instantáneas para convertir los nuevos volúmenes de instantáneas en lectura-escritura.

Para automatizar el proceso de administración del conjunto de instantáneas, puede usar la opción de línea de comandos **-script** para generar el script cmd que contiene los identificadores de instantánea. Después, puede copiar el script generado junto con los componentes de copia de seguridad en el otro equipo.

En el ejemplo siguiente se muestra cómo crear, exponer e interrumpir las instantáneas transportables mediante scripts de CMD.

1.  Cree el conjunto de instantáneas en el equipo A (el servidor de producción) desde la línea de comandos como se indica a continuación:

    **vshadow-p-t =bc1.xml-script = SC1. cmd**

    Especifique la opción **-script** para generar el script que contiene las definiciones de variables de entorno adecuadas. Tenga en cuenta que esto no expondrá ningún dispositivo de instantáneas en el equipo A.

2.  Copie el documento componentes de copia de seguridad (bc1.xml) y el script generado (SC1. cmd) del equipo a al equipo B.
3.  Para importar el conjunto de instantáneas en el equipo B, escriba el siguiente comando:

    **vshadow-i =bc1.xml**

    Esto hará que se muestren los dispositivos creados en el equipo B.

4.  Ejecute el script generado para establecer las variables de entorno para el conjunto de instantáneas. para ello, escriba el nombre de archivo en el símbolo del sistema como se muestra en el ejemplo siguiente:

    **SC1. cmd**

    Esto establecerá las variables de entorno pertinentes, tal como se describe en el apartado sobre propiedades de instantáneas de acceso de un script CMD.

5.  Exponga las instantáneas en el equipo B escribiendo los siguientes comandos:
    1.  **rmdir/s c: \\ punto de montaje \_**
    2.  **mkdir c: \\ punto de montaje \_**
    3.  **vshadow – el =% VSHADOW \_ ID. \_ 1%, c \\ : \_ punto de montaje**

    Esto mostrará los dispositivos de instantáneas creados en el equipo B.
6.  Divida el conjunto de instantáneas para que los volúmenes puedan escribirse escribiendo el comando siguiente:**C: \\>vshadow – BW =% vshadow \_ set \_ ID%**

Tenga en cuenta que las instantáneas transportables no persistentes también se pueden importar, pero se eliminan automáticamente cuando finaliza el proceso **vshadow** **-i** . Para importar las instantáneas antes de que se eliminen, debe usar la opción de línea de comandos **-exec** tal y como se describe en acceso a instantáneas no persistentes.

## <a name="including-writers-or-components"></a>Incluir escritores o componentes

De forma predeterminada, todos los escritores participan en la creación de instantáneas. Para determinar qué escritores y componentes se incluirán en un conjunto de instantáneas, use la opción de línea de comandos **-WM** o **-wm2** tal como se describe en [enumeración del estado y los metadatos del escritor](vshadow-tool-and-sample.md).

Para comprobar que se incluyen todos los componentes de un escritor, use la marca opcional **-Wi** en cualquiera de los siguientes formatos:

-   **vshadow** **-Wi** *WriterName*
-   **vshadow** **-Wi** **"**_cadena de nombre de escritor_*_"_*
-   **vshadow** **-Wi** **{**_WriterID_*_}_*
-   **vshadow** **-Wi** **{**_InstanceID_*_}_*

Para comprobar que se incluyen determinados componentes, use la marca opcional **-Wi** en cualquiera de los siguientes formatos:

-   **vshadow** **-Wi** *WriterName ***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-Wi** **"**_cadena de nombre de escritor_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-Wi** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-Wi** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

En los siguientes ejemplos se muestra cómo usar la marca opcional **-Wi** .

-   Especificación de *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow-Wi = "escritor del registro: \\ registro"**

-   Especificación de {*WriterID*}:

    **vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Especificando más de un escritor o componente:

    **vshadow-Wi = "escritor del registro: \\ registro"-Wi = "com+ REGDB Writer"**

## <a name="excluding-writers-or-components"></a>Exclusión de escritores o componentes

Para excluir todos los escritores, use la marca opcional **-NW** al crear la instantánea.

Para excluir todos los componentes de un escritor, use la marca opcional **-WX** en cualquiera de los siguientes formatos:

-   **vshadow** **-WX** *WriterName*
-   **vshadow** **-WX** **"**_cadena de nombre de escritor_*_"_*
-   **vshadow** **-WX** **{**_WriterID_*_}_*
-   **vshadow** **-WX** **{**_InstanceID_*_}_*

Para excluir componentes específicos, use la marca opcional **-WX** en cualquiera de los siguientes formatos:

-   **vshadow** **-WX** *WriterName ***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-WX** **"**_cadena de nombre de escritor_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-WX** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-WX** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

En los siguientes ejemplos se muestra cómo usar la marca opcional **-WX** .

-   Especificación de *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow-WX = "escritor del registro: \\ registro"**

-   Especificación de {*WriterID*}:

    **vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Especificando más de un escritor o componente:

    **vshadow-WX = "escritor del registro: \\ registro"-WX = "escritor de REGDB de com+"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>Romper conjuntos de instantáneas mediante el método BreakSnapshotSetEx

En los siguientes ejemplos se muestra cómo usar la opción de línea de comandos **-BEX** .

-   Especificar que el LUN de instantánea se enmascarará desde el host:

    **vshadow** **-BEX** **-Mask**

-   Especificar que el LUN de instantánea se exponga al host como un volumen de lectura/escritura:

    **vshadow** **-BEX** **-RW**

-   Especificar que el LUN de instantánea se exponga al host como un volumen de lectura y escritura, y que ninguna de las firmas de disco de los LUN de instantáneas se revertirá a la de los LUN originales:

    **vshadow** **-BEX** **-norevert**

 

 
