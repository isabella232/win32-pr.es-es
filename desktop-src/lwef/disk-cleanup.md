---
title: Crear un controlador de limpieza de disco
description: Una vez que se ha comprobado un axioma de tiempo y de nuevo en el mundo de los equipos es que, con independencia del tamaño de la capacidad de almacenamiento del equipo, se rellenará finalmente.
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- Controladores de liberador de espacio en disco
- Liberador de espacio en disco
- DataDrivenCleaner
- registro, controladores de liberador de espacio en disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30584439ae2c38ae8a9b7106dae96f69eea5df37
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105695780"
---
# <a name="creating-a-disk-cleanup-handler"></a>Crear un controlador de limpieza de disco

Una vez que se ha comprobado un axioma de tiempo y de nuevo en el mundo de los equipos es que, con independencia del tamaño de la capacidad de almacenamiento del equipo, se rellenará finalmente. Aunque el tamaño medio del disco duro de un equipo ha aumentado drásticamente con el tiempo, las aplicaciones también han crecido en consecuencia, lo que permite a los usuarios buscar maneras de crear más espacio libre en el disco duro. El espacio disponible también se reduce mediante el número de archivos temporales que crean las aplicaciones por motivos de rendimiento o de copia de seguridad. Cuando el espacio en disco es bajo, se necesita para reducir la cantidad de espacio que usan las aplicaciones. El espacio en disco se puede liberar mediante una variedad de medias, entre las que se incluyen las siguientes:

-   Eliminando archivos.
-   Comprimir archivos.
-   Mover archivos a un medio de copia de seguridad.
-   Transferir archivos a un servidor remoto.

Los archivos que son buenos candidatos para la limpieza incluyen:

-   Archivos que el usuario nunca volverá a necesitar.
-   Archivos temporales que solo existen por motivos de rendimiento.
-   Archivos que se pueden restaurar, si es necesario, desde un CD de instalación.
-   Archivos de datos que se han sustituido por versiones más recientes, como archivos de copia de seguridad antiguos.
-   Archivos más antiguos que no se han usado en un período de tiempo prolongado.

La eliminación es especialmente adecuada para los archivos que el usuario nunca necesitará de nuevo; por ejemplo, los archivos que se almacenan temporalmente en caché por motivos de rendimiento. La eliminación también es adecuada para los archivos que se restauran fácilmente, como los archivos de gráficos que se pueden volver a cargar desde un CD de instalación. Los archivos que el usuario podría necesitar posteriormente o que serían difíciles de reconstruir son más candidatos para la compresión o la copia de seguridad.

Esperar que un usuario Limpie manualmente el sistema de archivos no es una buena solución. Es posible que el usuario no sepa dónde se encuentran muchos de los archivos o cómo reconocer cuáles se pueden quitar de forma segura. Además, existe el riesgo de que el usuario pueda eliminar archivos esenciales.

En este tema se describen las siguientes aspectos de la utilidad liberador de espacio en disco.

-   [La utilidad liberador de espacio en disco de Windows](#the-windows-disk-cleanup-utility)
-   [Aspectos básicos de la implementación](#implementation-basics)
    -   [Initialize/InitializeEx](#initializeinitializeex)
    -   [GetSpaceUsed](#getspaceused)
    -   [ShowProperties (](#showproperties)
    -   [Purgar](#purge)
    -   [Desactivación](#deactivate)
-   [Registrar un controlador de limpieza de disco](#registering-a-disk-cleanup-handler)
    -   [Registrar el CLSID de un controlador](#registering-a-handlers-clsid)
    -   [Registro de un controlador con el administrador de liberador de espacio en disco: General](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [Registro de un controlador con el administrador de liberador de espacio en disco: Windows 2000 o sistemas posteriores](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [Usar el objeto DataDrivenCleaner](#using-the-datadrivencleaner-object)
    -   [Ejemplo de registro de un controlador de limpieza de disco](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>La utilidad liberador de espacio en disco de Windows

A partir de Windows 98, el sistema operativo Windows incluye el liberador de espacio en disco, una utilidad que facilita enormemente que el usuario administre el espacio disponible en el disco duro. La utilidad liberador de espacio en disco está diseñada para liberar tanto espacio en disco como sea posible y reducir el riesgo de que el usuario elimine los archivos esenciales de forma accidental.

El liberador de espacio en disco se puede iniciar de tres maneras.

-   El usuario puede iniciar el liberador de espacio en disco haciendo clic en **Inicio**; seleccionar **todos los programas**, **accesorios** y **herramientas del sistema**; y, a continuación, en **liberador de espacio en disco**.
-   El sistema notifica al usuario con un cuadro de mensaje que indica que el espacio en disco sin usar ha alcanzado el modo crítico. El umbral de modo crítico para una unidad superior a 2,25 gigabytes (GB) es de 200 megabytes (MB). Las advertencias posteriores se proporcionan en 80, 50 y 1 MB. El usuario tiene la opción de liberar espacio en disco manualmente o iniciar la utilidad de limpieza de disco.
-   El usuario puede hacer que el Asistente para tareas programadas de Windows (conocido como asistente para mantenimiento en sistemas anteriores) ejecute la utilidad liberador de espacio en disco automáticamente a las horas programadas.

El desafío básico inherente al liberador de espacio en disco es liberar tanto espacio en disco como sea posible sin eliminar archivos esenciales. Dado que no hay ninguna manera estándar de marcar archivos para la limpieza, ninguna aplicación puede detectar y limpiar de forma confiable todos los archivos no esenciales. La utilidad liberador de espacio en disco soluciona este problema dividiendo la operación de limpieza entre un único *Administrador de limpieza de disco* y una colección de controladores de limpieza de *disco*.

Cuando se ejecuta la utilidad liberador de espacio en disco, el usuario ve el siguiente cuadro de diálogo. (Si existe más de un disco o partición de disco en el equipo, primero se solicita al usuario que elija una unidad antes de que se muestre este cuadro de diálogo).

![captura de pantalla del cuadro de diálogo limpiar](images/cleanup1.png)

El administrador de liberador de espacio en disco forma parte del sistema operativo. Muestra el cuadro de diálogo que se muestra en la ilustración anterior, controla la entrada del usuario y administra la operación de limpieza. La selección real y la limpieza de archivos innecesarios se realizan mediante los controladores de limpieza de disco individuales que se muestran en el cuadro de lista del administrador de limpieza de disco. El usuario tiene la opción de habilitar o deshabilitar controladores individuales activando o desactivando su casilla en la interfaz de usuario del administrador de liberador de espacio en disco.

Cada controlador es responsable de un conjunto bien definido de archivos. Por ejemplo, el controlador seleccionado en la ilustración es responsable de limpiar los archivos de programa descargados. El controlador seleccionado en la ilustración también proporciona un botón **ver archivos** . Al hacer clic en el botón, el usuario puede solicitar que el controlador muestre una interfaz de usuario normalmente una ventana del explorador de Windows que permita al usuario especificar qué archivos o clases de archivos se van a limpiar.

Aunque Windows incluye varios controladores de limpieza de disco, no están diseñados para administrar archivos generados por otras aplicaciones. En su lugar, el administrador de liberador de espacio en disco está diseñado para ser flexible y extensible, ya que permite a cualquier desarrollador implementar y registrar su propio controlador de limpieza de disco. Cualquier desarrollador puede ampliar los servicios de liberador de espacio en disco disponibles implementando y registrando un controlador de limpieza de disco.

Todas las aplicaciones que generan archivos temporales pueden y deben implementar y registrar un controlador de limpieza de disco. Esto proporciona a los usuarios una forma cómoda y confiable de administrar los archivos temporales de la aplicación. Al implementar el controlador, puede decidir qué archivos se ven afectados y determinar cómo se produce la limpieza real.

## <a name="implementation-basics"></a>Aspectos básicos de la implementación

Los controladores de limpieza son objetos del modelo de objetos componentes (COM) de servidor en proceso. Windows proporciona un objeto de controlador existente denominado DataDrivenCleaner para su uso. También puede optar por implementar un controlador para obtener una mayor flexibilidad. Estos objetos permiten especificar cómo seleccionar archivos, espacio libre en disco y, en el caso de un controlador implementado, Mostrar la interfaz de usuario opcional para un control más granular. En esta sección se aborda la cuestión de implementar su propio controlador. Para obtener más información sobre el uso del objeto DataDrivenCleaner, consulte [uso del objeto DataDrivenCleaner](#using-the-datadrivencleaner-object).

Un controlador de limpieza de disco debe realizar estas cinco tareas básicas.

-   Inicialice el objeto de controlador.
-   Examine el disco para determinar cuánto espacio en disco se puede liberar.
-   Mostrar la interfaz de usuario para obtener comentarios sobre los archivos que se van a limpiar. (Opcional)
-   Realice la limpieza.
-   Apaga.

Para permitir que el administrador de liberador de espacio en disco administre estas tareas, un controlador debe exportar [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) para Windows 98 o [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) para Windows Millennium Edition (Windows Me), Windows 2000 y Windows XP. Dado que **IEmptyVolumeCache2** hereda de **IEmptyVolumeCache**, agregando solo el método adicional **InitializeEx**, se requiere relativamente poco trabajo adicional para implementar ambos. A menos que el controlador esté destinado solo a uno de estos sistemas operativos, debe exportar ambas interfaces.

Para exportar estas interfaces, debe implementar estos métodos correspondientes a las cinco tareas básicas.

-   [Initialize/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [ShowProperties (](#showproperties)
-   [Purgar](#purge)
-   [Desactivación](#deactivate)

### <a name="initializeinitializeex"></a>Initialize/InitializeEx

Los dos métodos de inicialización, que son bastante similares, se llaman cuando se ejecuta la utilidad liberador de espacio en disco. El administrador de limpieza de disco 98 de Windows llama al método [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) de un controlador. Windows Millennium Edition (Windows me), Windows 2000 o Windows XP Disk Cleanup Manager, sin embargo, primero intenta llamar a [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) y solo usa **IEmptyVolumeCache:: Initialize** si el controlador no expone [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) . El administrador de liberador de espacio en disco pasa información al método, como la clave del registro del controlador y el volumen del disco que se va a limpiar.

Cualquiera de los métodos puede devolver varias cadenas de presentación y establecer una o varias marcas. La principal diferencia entre los dos métodos es la forma en que se trata el texto que se muestra en el administrador de liberador de espacio en disco. Las siguientes tres cadenas se ven afectadas.



| String       | Propósito                                                                            | Inicialización                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Display Name (Nombre para mostrar) | El nombre del controlador mostrado en el cuadro de lista del administrador de liberador de espacio en disco.               | Si *ppwszDisplayName* es **null**, el valor predeterminado se recupera del registro. | Se debe especificar una cadena localizada correctamente en *ppwszDisplayName* no se usan valores de registro. |
| Descripción  | Texto descriptivo que se muestra debajo del cuadro de lista cuando se selecciona el nombre del controlador. | Si *ppwszDescription* es **null**, el valor predeterminado se recupera del registro. | Se debe especificar una cadena localizada correctamente en *ppwszDescription* no se usan valores de registro. |
| Texto del botón  | Texto del botón opcional que permite a los usuarios Mostrar la interfaz de usuario del controlador.        | Ningún parámetro está disponible. Debe especificarse en el registro.                           | Se debe especificar una cadena localizada correctamente en *ppwszBtnText* no se usan valores de registro.     |



 

El parámetro *pdwFlags* que se encuentra en ambos métodos de inicialización reconoce el mismo conjunto de marcas. El administrador de limpieza de disco pasa dos de estas marcas al método.

-   **EVCF \_ SETTINGSMODE**

    Si el administrador de liberador de espacio en disco se ejecuta según una programación, establece la marca **EVCF \_ SETTINGSMODE** . Si se establece esta marca, el administrador de liberador de espacio en disco no llama a los métodos [GetSpaceUsed](#getspaceused), [Purge](#purge)ni [showProperties (](#showproperties) . El método [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) o [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) del controlador debe administrar todas las tareas realizadas normalmente por [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) y [**Purge**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge). Dado que no hay ninguna oportunidad para los comentarios de los usuarios, solo se deben tocar los archivos que son extremadamente seguros de limpiar. Debe omitir el parámetro *pcwszVolume* del método de inicialización y limpiar los archivos innecesarios independientemente de la unidad en la que se encuentren.

-   **EVCF \_ OUTOFDISKSPACE**

    Si se establece la marca **EVCF \_ OUTOFDISKSPACE** , la unidad de disco del usuario es muy poco importante de espacio. El controlador debe ser agresivo para eliminar archivos, incluso si se produce una pérdida de rendimiento. Sin embargo, obviamente el controlador no debe eliminar los archivos que podrían provocar errores en una aplicación o que el usuario pierda datos.

El controlador de limpieza de disco establece las marcas restantes y se devuelven al administrador de liberador de espacio en disco. Para obtener más información, vea las páginas de referencia de métodos para [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) y [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex).

-   EVCF \_ DONTSHOWIFZERO

    Muestre el controlador en el cuadro de lista del administrador de liberador de espacio en disco solo si el valor devuelto por [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) indica que el controlador puede liberar espacio en disco.

-   EVCF \_ ENABLEBYDEFAULT

    Especifica que el controlador está habilitado de forma predeterminada. Se ejecutará cada vez que se produzca un limpieza de disco, a menos que el usuario lo deshabilite desactivando la casilla de la lista de controladores del administrador de limpieza de disco.

-   EVCF \_ ENABLEBYDEFAULT \_ auto

    Especifica que el controlador se habilita automáticamente para ejecutarse durante las limpiezas programadas.

-   EVCF \_ HASSETTINGS

    Establezca esta marca si el controlador tiene una interfaz de usuario para mostrar. En respuesta, el administrador de liberador de espacio en disco muestra un botón cuando se selecciona ese controlador en el cuadro de lista. Si se hace clic en ese botón, el administrador de liberador de espacio en disco llama a [**showProperties (**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties).

-   EVCF \_ REMOVEFROMLIST

    Elimine el nombre del controlador de la lista de controladores disponibles después de que el controlador se haya ejecutado una vez. La información del registro del controlador también se elimina.

### <a name="getspaceused"></a>GetSpaceUsed

El administrador de liberador de espacio en disco llama a este método para determinar la cantidad de espacio que un controlador de limpieza de disco puede liberar potencialmente. A continuación, el administrador de limpieza de disco muestra ese valor a la derecha del nombre del controlador en el cuadro de lista. Esta operación se realiza en todos los controladores registrados con el administrador de liberador de espacio en disco cuando se inicia el administrador y antes de que se muestre la interfaz de usuario principal del administrador. Cuando se llama a [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) , el controlador debe examinar los archivos de los que es responsable, determinar cuáles son candidatos de limpieza y devolver la cantidad de espacio en disco que puede liberar.

Dado que el análisis puede ser un proceso largo, el administrador de liberador de espacio en disco usa el parámetro *picb* de este método para pasar un puntero a una interfaz [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) . El controlador usa la interfaz periódicamente durante el examen para llamar a [**IEmptyVolumeCacheCallBack:: ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress), que sirve para dos propósitos.

-   Permite que el administrador de liberador de espacio en disco actualice una barra de progreso, lo que informa al usuario de cómo progresa el examen.
-   Notifica al controlador que detenga el examen en caso de que se haga clic en el botón **Cancelar** de la ventana de progreso. Ese evento de botón no se comunica directamente con el controlador; en su lugar, el administrador de liberador de espacio en disco devuelve E \_ Abort la próxima vez que [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) llame a [**IEmptyVolumeCacheCallBack:: ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="showproperties"></a>ShowProperties (

Antes de iniciar la limpieza, el controlador puede mostrar una interfaz de usuario normalmente en forma de ventana del explorador de Windows que permite al usuario ver una lista de archivos o clases de archivos seleccionados para su limpieza por el controlador. Si el controlador establece la marca **EVCF \_ HASSETTINGS** cuando se llama a [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) o [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) , el usuario puede solicitar la interfaz de usuario haciendo clic en el botón que se muestra para ese propósito en el administrador de liberador de espacio en disco. El texto del botón varía entre el controlador y el controlador, pero "ver archivos", "ver páginas" y "opciones" son etiquetas comunes.

Cuando se hace clic en el botón, el administrador de liberador de espacio en disco llama a [**showProperties (**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) para solicitar al controlador que muestre la interfaz de usuario. La interfaz de usuario debe crearse como un elemento secundario de la ventana cuyo identificador se pasa en el parámetro *hWnd* del método **showProperties (** .

### <a name="purge"></a>Purgar

El administrador de liberador de espacio en disco llama al método [**Purge**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) del controlador para establecer la limpieza en movimiento. El parámetro *picb* del método es un puntero a la interfaz [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) del administrador de limpieza de disco. Al igual que con el método [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) , el controlador debe usar la interfaz de devolución de llamada periódicamente para informar del progreso y consultar el administrador del liberador de espacio en disco si el usuario ha hecho clic en **Cancelar**. Sin embargo, tenga en cuenta que el método **Purge** debe llamar a [**IEmptyVolumeCacheCallBack::P urgeprogress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress), no a [**ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="deactivate"></a>Desactivación

Se llama al método [**Deactivate**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) cuando se está preparando el cierre del liberador de espacio en disco. El controlador debe realizar cualquier tarea de limpieza necesaria y devolver. Si no desea que el controlador se ejecute de nuevo, establezca la marca **EVCF \_ REMOVEFROMLIST** en el parámetro *pdwFlags* del método de inicialización. Si se establece esta marca, el administrador de liberador de espacio en disco quita el controlador de la lista y elimina las entradas del registro del controlador. Debe volver a agregar las entradas del registro para volver a ejecutar el controlador. Esta marca se usa normalmente para los controladores que se ejecutan una sola vez.

## <a name="registering-a-disk-cleanup-handler"></a>Registrar un controlador de limpieza de disco

Para agregar un controlador a la lista del administrador de liberadores de espacio en disco, deben agregarse ciertas claves y valores al registro de Windows.

-   [Registrar el CLSID de un controlador](#registering-a-handlers-clsid)
-   [Registro de un controlador con el administrador de liberador de espacio en disco: General](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [Registro de un controlador con el administrador de liberador de espacio en disco: Windows 2000 o sistemas posteriores](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [Usar el objeto DataDrivenCleaner](#using-the-datadrivencleaner-object)
-   [Ejemplo de registro de un controlador de limpieza de disco](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>Registrar el CLSID de un controlador

Al igual que con todos los objetos COM, el GUID y el archivo DLL del objeto controlador deben estar registrados bajo la clave **CLSID** en **\_ las clases HKEY \_ raíz**. También puede registrar un icono que se muestra junto al nombre del controlador en el cuadro de lista del administrador de liberador de espacio en disco, pero es opcional. En el ejemplo siguiente se muestran las claves, los valores y los datos implicados.

```
HKEY_CLASSES_ROOT
   CLSID
      Handler's GUID
         DefaultIcon
            (Default) = Handler's Icon Path, Icon Index
         InprocServer32
            (Default) = Handler's DLL path
            ThreadingModel = Apartment
```

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>Registro de un controlador con el administrador de liberador de espacio en disco: General

Para completar el registro, un controlador debe agregar una clave que contenga sus detalles, tal como se muestra aquí. En el resto de esta sección se describe el contenido de esta clave.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Handler's Key
```

En general, el nombre de la clave que contiene los detalles de un controlador se denomina para el tipo de archivo que controla, como **archivos de programa descargados**, pero esto no es un requisito. En la siguiente tabla se detallan los posibles valores que se encuentran en esta clave.

> [!Note]  
> Solo se requiere el valor predeterminado que especifica el identificador de clase (CLSID) del controlador, todos los demás valores son opcionales.

 



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Tipo</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Valor predeterminado</td>
<td>REG_SZ</td>
<td>CLSID del controlador tal como está registrado en <strong>HKEY_CLASSES_ROOT</strong> \ <strong>CLSID</strong>.</td>
</tr>
<tr class="even">
<td>AdvancedButtonText</td>
<td>REG_SZ</td>
<td>Texto del botón opcional en el que los usuarios pueden hacer clic para mostrar la interfaz de usuario del controlador. El carácter & se puede colocar delante de un carácter para asignar un método abreviado de teclado para el botón. Los controladores que exponen <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a>omiten el valor AdvancedButtonText.</td>
</tr>
<tr class="odd">
<td>CleanupString</td>
<td>REG_SZ</td>
<td>Línea de comandos que especifica un archivo ejecutable y parámetros de línea de comandos opcionales. Esta línea de comandos se ejecuta al finalizar el liberador de espacio en disco.</td>
</tr>
<tr class="even">
<td>CSIDL</td>
<td>REG_DWORD</td>
<td>Identificador independiente del sistema para una carpeta especial que se va a incluir en la búsqueda de archivos. Este valor debe especificarse como un valor numérico para la instancia, 0X0000001C en lugar de CSIDL_LOCAL_APPDATA. Para obtener una lista de los valores posibles, vea <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>. Solo se puede usar un valor único.<br/> Si se especifica el valor de la carpeta, la ubicación indicada por el valor CSIDL se antepone a esa información para crear una ruta de búsqueda. Por ejemplo, considere el siguiente escenario.<br/>
<ul>
<li>El valor CSIDL se especifica como 0x0000000d (CSIDL_MYMUSIC)</li>
<li>La carpeta mi música se encuentra en C:\Documents and Settings \<em>nombreDeUsuario</em>\Mis Music.</li>
<li>El valor de la carpeta contiene &quot; Jazz\Singers&quot;</li>
</ul>
El resultado de ese escenario es que el controlador de liberador de espacio en disco busca en la carpeta C:\Documents and Settings \<em>nombreDeUsuario</em>\Mis Music\Jazz\Singers Tenga en cuenta que la barra diagonal que precede al valor de carpeta se agrega si no está presente.<br/></td>
</tr>
<tr class="odd">
<td>Descripción</td>
<td>REG_SZ</td>
<td>Texto descriptivo que se muestra debajo del cuadro de lista del administrador de limpieza de disco cuando se selecciona el nombre del controlador. Aquí puede explicar lo que hace el controlador, los archivos con los que se preocupa y cualquier otra información que elucidatory al usuario. Si el controlador no expone <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a> , este texto se puede invalidar mediante el método <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache:: Initialize</strong></a> del controlador especificando una cadena alternativa en el parámetro <em>ppwszDescription</em> cuando se llama al método.</td>
</tr>
<tr class="even">
<td>Pantalla</td>
<td>REG_SZ</td>
<td>Nombre del controlador que se va a mostrar en el cuadro de lista del administrador de liberadores de espacio en disco. Si el controlador no expone <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a> , este texto se puede invalidar mediante el método <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache:: Initialize</strong></a> del controlador especificando una cadena alternativa en el parámetro <em>ppwszDisplayName</em> cuando se llama al método.</td>
</tr>
<tr class="odd">
<td>FileList</td>
<td>REG_SZ o REG_MULTI_SZ</td>
<td>Una lista de archivos buscados y limpiados por este controlador. Puede especificar caracteres comodín mediante el carácter? o * caracteres. Si el valor es de tipo REG_SZ, varias extensiones se separan mediante el | o: caracteres, sin espacios en cada lado.<br/> Si se establece la marca de DDEVCF_REMOVEDIRS en el valor Flags, estos valores pueden especificar nombres de directorio y archivos.<br/></td>
</tr>
<tr class="even">
<td>Marcas</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Marcas que controlan los elementos del procedimiento de búsqueda y limpieza. Uno o varios de los valores siguientes.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Busque y quite de forma recursiva.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Después de que el controlador se ejecute una vez, quítelo del registro.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Quite los archivos que cumplan los criterios de búsqueda, incluso si son de solo lectura.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Quite los archivos que cumplan los criterios de búsqueda, incluso si son archivos del sistema.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Quite los archivos que cumplan los criterios de búsqueda, incluso si son archivos ocultos.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). No muestre este controlador en el administrador de liberador de espacio en disco si no hay archivos que coincidan con sus criterios de búsqueda.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Haga coincidir el valor de FileList con los directorios y quite las coincidencias y todos sus subdirectorios.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Ejecute este controlador solo si el espacio en disco disponible ha descendido por debajo del valor crítico, determinado por el administrador de limpieza de disco estableciendo la marca de EVCF_OUTOFDISKSPACE a través de <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache:: Initialize</strong></a> o <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2:: InitializeEx</strong></a>.</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Quite el directorio principal de los archivos especificados una vez que se haya ejecutado el limpiador.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Use el valor LastAccess, si se proporciona, para determinar qué archivos se deben limpiar. Esta marca se omite cuando se usa <a href="#using-the-datadrivencleaner-object">DataDrivenCleaner</a> siempre que se use cualquier valor LastAccess proporcionado.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Carpeta</td>
<td>REG_SZ, REG_MULTI_SZ o REG_EXPAND_SZ</td>
<td>Carpeta o carpetas específicas para buscar elementos que coincidan con las entradas del valor FileList. Puede especificar caracteres comodín mediante el carácter? o * caracteres. Si el valor es de tipo REG_SZ, varios nombres de carpeta se separan mediante el | carácter, sin espacios en cada lado del mismo.<br/> Si hay un valor CSIDL, solo se puede especificar una carpeta en este valor. La ubicación indicada por el valor CSIDL se antepone a la ruta de acceso de la carpeta para crear una ruta de búsqueda. Para obtener un ejemplo, vea la descripción del valor CSIDL.<br/> Si este valor está ausente en Windows Vista Service Pack 1 (SP1) y versiones posteriores, el controlador de limpieza se omite y devuelve S_FALSE en la inicialización.<br/> Si este valor está ausente en la versión original de Windows Vista y versiones anteriores, se usa la carpeta raíz del volumen actual. En ese caso, se necesita la marca DDEVCF_DOSUBDIRS para buscar en toda la unidad. Sin él, solo se busca en la carpeta raíz.<br/> Se debe especificar una o más unidades de disco. Esto puede proporcionarse a través del valor CSIDL o a través de una cadena de REG_EXPAND_SZ. Sin embargo, con estas opciones, la unidad de búsqueda debe especificarse en el nombre de la carpeta. Use?: para buscar la carpeta en la unidad actual.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ o REG_EXPAND_SZ</td>
<td>Ruta de acceso al recurso del que se va a obtener un icono que se va a usar en la asociación con el controlador.</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD o REG_BINARY</td>
<td>El número de días que debe haber transcurrido desde la última vez que se obtuvo acceso al archivo o se creó un directorio para el archivo o directorio que se va a considerar para la limpieza.</td>
</tr>
<tr class="even">
<td>Prioridad</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Determina el orden en que se ejecuta el controlador con respecto a otros controladores. Cuanto mayor sea el número, antes en el proceso en el que se ejecuta el controlador. No hay ningún intervalo definido que sea aceptable.</td>
</tr>
<tr class="odd">
<td>PropertyBag</td>
<td>REG_SZ</td>
<td>El CLSID de un recurso que se usa para proporcionar el texto localizado para el nombre para mostrar, la descripción y el texto del botón. Este recurso es útil en la situación en la que un controlador no implementa <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> y el controlador se ejecuta en Microsoft Windows NT o Windows XP.<br/> En primer lugar, el administrador de liberador de espacio en disco comprueba si la rutina de inicialización del controlador devolvió esas cadenas, como sería el caso cuando se implementa <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2</strong></a> . En el siguiente error, el administrador vuelve a un contenedor de propiedades denominado en este valor. Si no se ha proporcionado ninguno, recupera el texto del registro.<br/></td>
</tr>
<tr class="even">
<td>StateFlags</td>
<td>REG_DWORD</td>
<td>Al ejecutar el archivo ejecutable del administrador de limpieza de disco Cleanmgr.exe desde una línea de comandos, puede declarar <em>perfiles</em>de limpieza. Estos perfiles se componen de un subconjunto de los controladores disponibles y se les asigna una etiqueta numérica única. Esto le permite automatizar la ejecución de distintos conjuntos de controladores en momentos diferentes.<br/> La línea de comandos &quot;cleanmgr.exe/sageset:<strong>nnnn</strong> &quot; , donde <strong>nnnn</strong> es una etiqueta numérica única, muestra una interfaz de usuario que le permite elegir los controladores que se van a incluir en el perfil. Además de definir el perfil, el parámetro sageset también escribe un valor denominado StateFlags<strong>nnnn</strong>, donde <strong>nnnn</strong> es la etiqueta usada en el parámetro, en todas las subclaves de <strong>VolumeCaches</strong>. Existen dos posibles valores de datos para esas entradas.
<ul>
<li>0: no ejecute este controlador cuando se ejecute este perfil.</li>
<li>2: incluir este controlador cuando se ejecute este perfil.</li>
</ul>
<br/> Por ejemplo, supongamos que se ejecuta la línea de comandos &quot;cleanmgr.exe/sageset: 1234 &quot; . En la interfaz de usuario que se presenta, el usuario elige <strong>los archivos de programa descargados</strong>, pero no elige <strong>archivos temporales de Internet</strong>. Los valores siguientes se escriben en el registro.<br/>
<pre data-space="preserve"><code>HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     Downloaded Program Files
                        StateFlags1234 = 0x00000002
                     Internet Cache Files
                        StateFlags1234 = 0x00000000</code></pre>
<br/> La línea &quot; de comandoscleanmgr.exe/sagerun:<strong>nnnn</strong> &quot; , donde el valor de <strong>nnnn</strong> coincide con la etiqueta declarada con el parámetro sageset, ejecuta todos los controladores seleccionados en ese perfil.<br/> Un valor de StateFlags genérico se escribe en el registro cuando el liberador de espacio en disco se ejecuta con normalidad. Este valor simplemente almacena el estado (comprobado o desactivado) del controlador la última vez que se presentó como una opción al usuario. Existen dos posibles valores de datos para esas entradas.
<ul>
<li>0: no se seleccionó el controlador.</li>
<li>1: se seleccionó el controlador.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>Registro de un controlador con el administrador de liberador de espacio en disco: Windows 2000 o sistemas posteriores

La especificación del texto para mostrar en el registro puede dificultar la localización del software. Por esta razón, Windows 2000 y Windows XP admiten la interfaz [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) con su método de inicialización preferido [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex). En Windows 2000 o posterior, siempre se realiza un intento de llamar a **IEmptyVolumeCache2:: InitializeEx** antes de [**IEmptyVolumeCache:: Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize). El sistema solo usa **Initialize** para inicializar un controlador si no se expone **IEmptyVolumeCache2** .

En lo que respecta al registro, la única diferencia en Windows 2000 o posterior es que se pueden omitir los valores AdvancedButtonText, display y Description cuando el controlador expone [**IEmptyVolumeCache2:: InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) . Estos valores, que contienen texto localizado correctamente, se proporcionan al administrador de liberador de espacio en disco cuando llama a **InitializeEx**.

### <a name="using-the-datadrivencleaner-object"></a>Usar el objeto DataDrivenCleaner

El sistema operativo proporciona un controlador de limpieza de disco básico, denominado DataDrivenCleaner. Para usar este objeto como un controlador en lugar de implementar el suyo propio, use el CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} como valor predeterminado de la subclave del controlador en **VolumeCaches** , como se describe en [registrar un controlador con el administrador de liberador de espacio en disco: General](#registering-a-handler-with-the-disk-cleanup-manager-general).

DataDrivenCleaner no expone [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2), por lo que los valores de presentación y descripción se proporcionan a través del registro. Al declarar esas cadenas, tenga en cuenta que esto podría causar problemas de localización. El texto localizado se puede proporcionar a través del valor PropertyBag. El valor de AdvancedButtonText se omite porque no hay ninguna interfaz de usuario y, por lo tanto, no hay ningún botón que lo muestre, está disponible para este controlador.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Ejemplo de registro de un controlador de limpieza de disco

A continuación se muestra un registro de ejemplo para un controlador de limpieza de disco implementado por la compañía telefónica. Este controlador implementa [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) y [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2), por lo que proporciona AdvancedButtonText, Description y valores para mostrar en caso de que se use en un equipo que ejecute Windows 98. El controlador combina los valores CSIDL y Folder para buscar archivos en el directorio C: \\ archivos de programa \\ del directorio Temp de la compañía telefónica \\ y la \_ marca DDEVCF DOSUBDIRS está establecida para que se busquen también en sus subdirectorios. Solo se tienen en cuenta los archivos con extensiones. tmp y. tpc para la limpieza, y la \_ marca DDEVCF Private \_ LASTACCESS se establece de modo que, a partir de esos archivos, solo se tengan en cuenta aquellos a los que no se haya accedido durante 14 días o más. \_También se establece la marca DDEVCF DONTSHOWIFZERO para que el controlador no aparezca en la lista a menos que haya detectado candidatos de limpieza.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  VolumeCaches
                     The Phone Company Files
                        (Default) = {the CLSID GUID}
                        AdvancedButtonText = &View Files
                        CleanupString = c:\tpc.exe
                        CSIDL = 0x00000026
                        Description = Old temporary files.
                        Display = The Phone Company Files
                        FileList = *.tmp|*.tpc
                        Flags = 0x10000021
                        Folder = \The Phone Company\Temp
                        IconPath = c:\Program Files\The Phone Company\tpc.dll,2
                        LastAccess = 0x0000000e
                        Priority = 200
                        PropertyBag = {Property Bag CLSID GUID}
```

 

