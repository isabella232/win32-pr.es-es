---
description: 'Más información sobre: Ejemplos de la herramienta VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Ejemplos de herramientas de VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ec0a753f2865be98cfed76cd192a73cfc785b3fcdc487f7685c9f4ae7d52e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056353"
---
# <a name="vshadow-tool-examples"></a>Ejemplos de herramientas de VShadow

En los ejemplos siguientes se muestra cómo usar la herramienta VShadow para realizar las tareas más comunes:

-   [Acceso a las propiedades de instantáneas desde un script CMD](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [Acceso a instantáneas no persistentes](#accessing-nonpersistent-shadow-copies)
-   [Copiar un archivo desde una instantánea](#copying-a-file-from-a-shadow-copy)
-   [Enumerar todos los archivos en un dispositivo de instantáneas](#enumerating-all-files-on-a-shadow-copy-device)
-   [Importar una instantánea transportable](#importing-a-transportable-shadow-copy)
-   [Incluir escritores o componentes](#including-writers-or-components)
-   [Exclusión de escritores o componentes](#excluding-writers-or-components)
-   [Interrumpir conjuntos de instantáneas mediante el método BreakSnapshotSetEx](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

Para obtener una lista completa de las opciones de línea de comandos y su uso, vea [VShadow Tool y Sample](vshadow-tool-and-sample.md).

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>Acceso a las propiedades de instantáneas desde un script CMD

Si usa la marca **opcional -script** al crear instantáneas, VShadow crea un archivo de script CMD que contiene variables de entorno relacionadas con las instantáneas recién creadas, como las siguientes:

-   Identificador del conjunto de instantáneas, que se almacena en la variable de entorno %VSHADOW \_ SET \_ ID%
-   Los identificadores de instantánea, que se almacenan en variables con el formato %VSHADOW \_ ID \_ *NNN*%, donde *NNN representa* el índice del volumen de origen en la línea de comandos VShadow.
-   Los nombres de dispositivo de instantáneas, que se almacenan en variables con el formato %VSHADOW \_ DEVICE \_ *NNN*%, donde *NNN es* el índice del volumen de origen en la línea de comandos VShadow

Puede usar el archivo CMD generado para realizar operaciones de administración limitadas en las instantáneas.

> [!Note]  
> El evento de escritor [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) se envía después de ejecutar el script **-exec.** VSS llama al método **IVssBackupComponents::BackupComplete** para indicar a los escritores que la copia de seguridad se ha completado y los escritores pueden truncar los registros en este momento. Por lo tanto, es importante comprobar que la instantánea o copia de seguridad se ha completado realmente. Si se ha producido un error en la copia de seguridad, puede cancelar el proceso de creación devolviendo un código de salida distinto de cero en el script o comando ejecutado. (Consulte la documentación del comando exit en la Windows [de la línea de comandos).](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)) Si el comando personalizado vuelve con un código de salida distinto de cero, se cancela la creación de instantáneas y no se llama a **IVssBackupComponents::BackupComplete.**

 

En el ejemplo siguiente se muestra cómo crear una instantánea persistente desde la línea de comandos y usar el script CMD para exponerla.

1.  **vshadow -p -nw -script=SETVAR1.cmd c:**
2.  **llamar a SETVAR1.cmd**
3.  **C: \\>vshadow -el=%VSHADOW \_ ID \_ 1%,c: \\ directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>Acceso a instantáneas no persistentes

Las instantáneas no persistentes se eliminan automáticamente cuando se cierra el programa que las crea (en este caso, VShadow). Para acceder al contenido de estas instantáneas, VShadow permite ejecutar un script después de crear las instantáneas, pero antes de que se cierre el programa VShadow.

En el ejemplo siguiente se muestra cómo usar la opción de línea de comandos -exec para ejecutar un script denominado "enum.cmd":

**vshadow -nw -exec=enum.cmd c:**

En el script ejecutado, también puede ejecutar el script SETVAR generado en este comando personalizado. Esto permite que el script acceda directamente al contenido de las instantáneas. Recuerde que el dispositivo de sombra se puede recuperar de la variable de entorno NNN DE VSHADOW \_ \_ DEVICE.

Este es un script enum.cmd de ejemplo:

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

Esta es la línea de comandos para ejecutar el script enum.cmd:

**vshadow -nw -exec=c: \\ enum.cmd -script=setvar1.cmd c:**

## <a name="copying-a-file-from-a-shadow-copy"></a>Copiar un archivo desde una instantánea

En el ejemplo siguiente se muestra cómo copiar un archivo desde una instantánea.

1.  **dir > c: \\somefile.txt**
2.  **vshadow -p -nw -script=SETVAR1.cmd c:**
3.  **llamar a SETVAR1.cmd**
4.  **copy %VSHADOW \_ DEVICE \_ 1 % \\somefile.txt c: \\ somefile \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>Enumerar todos los archivos en un dispositivo de instantáneas

En el ejemplo siguiente se muestra cómo enumerar todos los archivos de un dispositivo de instantáneas desde un archivo por lotes.

1.  **dir > c: \\somefile.txt**
2.  **vshadow -p -nw -script=SETVAR1.cmd c:**
3.  **llamar a SETVAR1.cmd**
4.  **para /R %VSHADOW \_ DEVICE \_ 1% \\ %%i in ( \* ) do @echo %%i**

## <a name="importing-a-transportable-shadow-copy"></a>Importar una instantánea transportable

Para crear una instantánea transportable en un equipo e importarla en otra, debe tener dos equipos conectados (a través de una configuración san) a una matriz de almacenamiento que admita instantáneas de hardware de VSS. Se debe instalar un proveedor de hardware de VSS en cada equipo.

En el ejemplo siguiente se muestra cómo crear e importar la instantánea.

1.  Cree el conjunto de instantáneas en el equipo A (el servidor de producción) escribiendo el siguiente comando después del símbolo del sistema:

    **vshadow -p -t=bc1.xml**

    Esto no expondrá ningún dispositivo de instantáneas en el equipo A.

2.  Copie el documento componentes de copia de seguridad (bc1.xml) del equipo A al equipo B.
3.  Para importar el conjunto de sombras en la máquina B, escriba el siguiente comando:

    **vshadow -i=bc1.xml**

Opcionalmente, puede exponer estas instantáneas como letras de unidad o carpetas montadas. Además, podría interrumpir el conjunto de sombras para que los nuevos volúmenes de instantáneas puedan leer y escribir.

Para automatizar el proceso de administración del conjunto de sombras, puede usar la opción de línea de comandos **-script** para generar el script CMD que contiene los IDs de instantáneas. A continuación, puede copiar el script generado junto con los componentes de copia de seguridad en el otro equipo.

En el ejemplo siguiente se muestra cómo crear, exponer y interrumpir instantáneas transportables mediante scripts CMD.

1.  Cree el conjunto de instantáneas en el equipo A (el servidor de producción) desde la línea de comandos como se muestra a continuación:

    **vshadow -p -t=bc1.xml -script=sc1.cmd**

    Especifique la **opción -script** para generar el script que contiene las definiciones de variables de entorno adecuadas. Tenga en cuenta que esto no expondrá ningún dispositivo de instantáneas en el equipo A.

2.  Copie el documento de componentes de copia de seguridad (bc1.xml) y el script generado (sc1.cmd) del equipo A al equipo B.
3.  Para importar el conjunto de sombras en la máquina B, escriba el siguiente comando:

    **vshadow -i=bc1.xml**

    Esto mostrará los dispositivos creados en el equipo B.

4.  Ejecute el script generado para establecer las variables de entorno para el conjunto de instantáneas escribiendo el nombre de archivo en el símbolo del sistema, como en el ejemplo siguiente:

    **sc1.cmd**

    Esto establecerá las variables de entorno pertinentes como se describe en Acceso a las propiedades de instantáneas desde un script CMD.

5.  Para exponer las instantáneas en el equipo B, escriba los siguientes comandos:
    1.  **rmdir /s c: \\ punto de \_ montaje**
    2.  **mkdir c: punto \\ de \_ montaje**
    3.  **vshadow –el=%VSHADOW \_ ID \_ 1%,c: \\ punto de \_ montaje**

    Esto mostrará los dispositivos de instantáneas creados en el equipo B.
6.  Para interrumpir el conjunto de instantáneas para que los volúmenes se pueden escribir, escriba el siguiente **comando: C: \\>vshadow –bw=%VSHADOW \_ SET \_ ID%**

Tenga en cuenta que también se pueden importar instantáneas transportables no persistentes, pero se eliminan automáticamente cuando se cierra el proceso **vshadow** **-i.** Para importar las instantáneas antes de que se eliminen, debe usar la opción de línea de comandos **-exec** como se describe en Acceso a instantáneas no persistentes.

## <a name="including-writers-or-components"></a>Incluir escritores o componentes

De forma predeterminada, todos los escritores participan en la creación de instantáneas. Para determinar qué escritores y componentes se incluirán en un conjunto de instantáneas, use la opción de línea de comandos **-wm** o **-wm2** como se describe en Enumerar el estado del escritor y los [metadatos](vshadow-tool-and-sample.md).

Para comprobar que se incluyen todos los componentes de un escritor, use la **marca opcional -wi** en cualquiera de los formatos siguientes:

-   **vshadow** **-wi** *WriterName*
-   **vshadow** **-wi** **"** Cadena de nombre de _escritor_*_"_*
-   **vshadow** **-wi** **{**_WriterID_*_}_*
-   **vshadow** **-wi** **{**_InstanceID_*_}_*

Para comprobar que se incluyen componentes específicos, use la **marca opcional -wi** en cualquiera de los formatos siguientes:

-   **vshadow** **-wi** *WriterName***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wi** **"** Writer Name _String_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wi** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

En los ejemplos siguientes se muestra cómo usar la **marca opcional -wi.**

-   Especificar *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow -wi="Registry Writer: \\ Registry"**

-   Especificar {*WriterID*}:

    **vshadow -wi={BE000CBE-11FE-4426-9C58-531AAA6355FC4}**

-   Especificar más de un escritor o componente:

    **vshadow -wi="Registry Writer: \\ Registry" -wi="COM+ REGDB Writer"**

## <a name="excluding-writers-or-components"></a>Exclusión de escritores o componentes

Para excluir todos los escritores, use la **marca opcional -nw** al crear la instantánea.

Para excluir todos los componentes de un escritor, use la **marca opcional -wx** en cualquiera de los formatos siguientes:

-   **vshadow** **-wx** *WriterName*
-   **vshadow** **-wx** **"** Writer Name _String_*_"_*
-   **vshadow** **-wx** **{**_WriterID_*_}_*
-   **vshadow** **-wx** **{**_InstanceID_*_}_*

Para excluir componentes específicos, use la **marca opcional -wx** en cualquiera de los formatos siguientes:

-   **vshadow** **-wx** *WriterName***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-wx** **"** Writer Name _String_*_": \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_WriterID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-wx** **{**_InstanceID_*_}: \\_*_LogicalPath_ *_\\_* _ComponentName_

En los ejemplos siguientes se muestra cómo usar la **marca opcional -wx.**

-   Especificar *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow -wx="Registry Writer: \\ Registry"**

-   Especificar {*WriterID*}:

    **vshadow -wx={BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Especificar más de un escritor o componente:

    **vshadow -wx="Registry Writer: \\ Registry" -wx="COM+ REGDB Writer"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>Interrupción de los conjuntos de instantáneas mediante el método BreakSnapshotSetEx

En los ejemplos siguientes se muestra cómo usar la opción de línea de comandos **-bex.**

-   Especificación de que el LUN de instantáneas se enmascarará desde el host:

    **vshadow** **-bex** **-mask**

-   Especificación de que el LUN de instantáneas se expone al host como un volumen de lectura y escritura:

    **vshadow** **-bex** **-rw**

-   Especificando que el LUN de instantáneas se exponga al host como un volumen de lectura y escritura, y que ninguna de las firmas de disco de los LUN de instantáneas se revertirá al de los LUN originales:

    **vshadow** **-bex** **-norevert**

 

 
