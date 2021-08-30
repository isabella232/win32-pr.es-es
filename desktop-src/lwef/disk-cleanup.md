---
title: Crear un controlador de limpieza de disco
description: Un axioma demostrado una vez y otra vez en el mundo de los equipos es que, independientemente del tamaño de la capacidad de almacenamiento del equipo, al final se llenará.
ms.assetid: f85e0db7-fbdb-452e-90c8-672f716b5692
keywords:
- controladores de limpieza de disco
- Liberador de espacio en disco
- DataDrivenCleaner
- register,disk cleanup handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217366c4e7da2d4fc3b53b7cf32ef418916247d3
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622281"
---
# <a name="creating-a-disk-cleanup-handler"></a>Crear un controlador de limpieza de disco

Un axioma demostrado una vez y otra vez en el mundo de los equipos es que, independientemente del tamaño de la capacidad de almacenamiento del equipo, al final se llenará. Aunque el tamaño medio del disco duro de un equipo ha aumentado considerablemente con el tiempo, las aplicaciones también han crecido en consecuencia, lo que deja a los usuarios buscando formas de crear más espacio libre en disco duro. El espacio disponible también se reduce por los muchos archivos temporales que las aplicaciones crean por motivos de copia de seguridad o rendimiento. Cuando el espacio en disco es bajo, es necesario reducir la cantidad de espacio que usan las aplicaciones. El espacio en disco se puede liberar mediante diversos medios, incluidos los siguientes:

-   Eliminando archivos.
-   Comprimir archivos.
-   Mover archivos a un medio de copia de seguridad.
-   Transferir archivos a un servidor remoto.

Los archivos que son buenos candidatos para la limpieza incluyen:

-   Archivos que el usuario nunca volverá a necesitar.
-   Archivos temporales que solo existen por motivos de rendimiento.
-   Archivos que se pueden restaurar, si es necesario, desde un CD de instalación.
-   Archivos de datos que posiblemente se han reemplazado por versiones más recientes, como los archivos de copia de seguridad antiguos.
-   Archivos antiguos que no se han usado durante mucho tiempo.

La eliminación es especialmente adecuada para los archivos que el usuario nunca volverá a necesitar, por ejemplo, los archivos que se almacenan temporalmente en caché por motivos de rendimiento. La eliminación también es adecuada para los archivos que se restauran fácilmente, como los archivos de gráficos que se pueden volver a cargar desde un CD de instalación. Los archivos que el usuario podría necesitar más adelante o que serían difíciles de reconstruir son mejores candidatos para la compresión o la copia de seguridad.

Esperar que un usuario limpie manualmente el sistema de archivos no es una buena solución. Es posible que el usuario no sepa dónde se encuentran muchos de los archivos o cómo reconocer cuáles se pueden quitar de forma segura. Además, existe el riesgo de que el usuario pueda eliminar archivos esenciales.

En este tema se de abordan las siguientes facetas de la utilidad Limpieza de disco.

-   [Utilidad Windows limpieza de disco](#the-windows-disk-cleanup-utility)
-   [Conceptos básicos de implementación](#implementation-basics)
    -   [Initialize/InitializeEx](#initializeinitializeex)
    -   [GetSpaceUsed](#getspaceused)
    -   [ShowProperties](#showproperties)
    -   [Purgar](#purge)
    -   [Desactivación](#deactivate)
-   [Registro de un controlador de limpieza de disco](#registering-a-disk-cleanup-handler)
    -   [Registro del CLSID de un controlador](#registering-a-handlers-clsid)
    -   [Registro de un controlador con el Administrador de limpieza de discos: General](#registering-a-handler-with-the-disk-cleanup-manager-general)
    -   [Registro de un controlador con el Administrador de limpieza de discos: Windows 2000 o sistemas posteriores](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
    -   [Usar el objeto DataDrivenCleaner](#using-the-datadrivencleaner-object)
    -   [Registro de ejemplo de un controlador de limpieza de disco](#example-registration-of-a-disk-cleanup-handler)

## <a name="the-windows-disk-cleanup-utility"></a>Utilidad Windows limpieza de disco

A partir de Windows 98, el sistema operativo Windows incluye Limpieza de disco, una utilidad que facilita al usuario la administración del espacio disponible en disco duro. La utilidad Limpieza de disco está diseñada para liberar tanto espacio en disco como sea posible y reducir el riesgo de que el usuario elimine accidentalmente los archivos esenciales.

La limpieza del disco se puede iniciar de tres maneras.

-   El usuario puede iniciar la limpieza de disco haciendo clic **en Iniciar**; que apunta a **Todos los programas,** **Accesorios** y Herramientas **del sistema**; y, a continuación, **hacer clic en Limpieza de disco.**
-   El sistema notifica al usuario con un cuadro de mensaje que el espacio en disco no utilizado ha alcanzado el modo crítico. El umbral de modo crítico para una unidad de más de 2,25 gigabytes (GB) es de 200 megabytes (MB). Las advertencias posteriores se dan en 80, 50 y 1 MB. El usuario tiene la opción de liberar espacio en disco manualmente o iniciar la utilidad Limpieza de disco.
-   El usuario puede hacer que Windows Asistente para tareas programadas (conocido como Asistente para mantenimiento en sistemas anteriores) ejecute la utilidad Limpieza de disco automáticamente en horas programadas.

El desafío básico inherente a la limpieza de disco es liberar tanto espacio en disco como sea posible sin eliminar los archivos esenciales. Dado que no hay ninguna manera estándar de marcar los archivos para la limpieza, ninguna aplicación única puede detectar y limpiar de forma confiable todos los archivos no esenciales. La utilidad Limpieza de disco soluciona este problema  dividiendo la operación de limpieza entre un único administrador de limpieza de disco y una colección de controladores de *limpieza de disco*.

Cuando se ejecuta la utilidad Limpieza de disco, el usuario ve el siguiente cuadro de diálogo. (Si hay más de una partición de disco o disco en el equipo, primero se pide al usuario que elija una unidad antes de que se muestre este cuadro de diálogo).

![captura de pantalla del cuadro de diálogo de limpieza](images/cleanup1.png)

El administrador de limpieza de disco forma parte del sistema operativo. Muestra el cuadro de diálogo que se muestra en la ilustración anterior, controla la entrada del usuario y administra la operación de limpieza. La selección y limpieza reales de los archivos innecesarios se realiza mediante los controladores de limpieza de disco individuales que se muestran en el cuadro de lista del administrador de limpieza de discos. El usuario tiene la opción de habilitar o deshabilitar controladores individuales activando o desactivando su casilla en la interfaz de usuario del administrador de limpieza de discos.

Cada controlador es responsable de un conjunto de archivos bien definido. Por ejemplo, el controlador seleccionado en la ilustración es responsable de limpiar los archivos de programa descargados. El controlador seleccionado en la ilustración también proporciona un **botón Ver** archivos. Al hacer clic en el botón, el usuario puede solicitar que el controlador muestre una interfaz de usuario normalmente una ventana del Explorador de Windows que permita al usuario especificar qué archivos o clases de archivos limpiar.

Aunque Windows incluye varios controladores de limpieza de disco, no están diseñados para controlar los archivos generados por otras aplicaciones. En su lugar, el administrador de limpieza de disco está diseñado para ser flexible y extensible al permitir que cualquier desarrollador implemente y registre su propio controlador de limpieza de disco. Cualquier desarrollador puede ampliar los servicios de limpieza de disco disponibles implementando y registrando un controlador de limpieza de disco.

Todas las aplicaciones que generan archivos temporales pueden y deben implementar y registrar un controlador de limpieza de disco. Esto proporciona a los usuarios una manera cómoda y confiable de administrar los archivos temporales de la aplicación. Al implementar el controlador, puede decidir qué archivos se ven afectados y determinar cómo se produce la limpieza real.

## <a name="implementation-basics"></a>Conceptos básicos de implementación

Los controladores de limpieza son objetos del Modelo de objetos componentes (COM) del servidor en proceso. Windows proporciona un objeto de controlador existente denominado DataDrivenCleaner para su uso. También puede optar por implementar un controlador usted mismo para obtener más flexibilidad. A continuación, estos objetos permiten especificar cómo seleccionar archivos, liberar espacio en disco y, en el caso de un controlador implementado, mostrar la interfaz de usuario opcional para un control más granular. En esta sección se aborda la cuestión de implementar su propio controlador. Para obtener más información sobre el uso del objeto DataDrivenCleaner, vea [Usar el objeto DataDrivenCleaner](#using-the-datadrivencleaner-object).

Un controlador de limpieza de disco debe realizar estas cinco tareas básicas.

-   Inicialice el objeto de controlador.
-   Analice el disco para determinar cuánto espacio en disco se puede liberar.
-   Muestra la interfaz de usuario para obtener comentarios de los usuarios sobre los archivos que se deben limpiar. (Opcional)
-   Realice la limpieza.
-   Apagar.

Para permitir que el administrador de limpieza de disco administre estas tareas, un controlador debe exportar [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) para Windows 98 o [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) para Windows Edition Desenrículo (Windows Me), Windows 2000 y Windows XP. Dado **que IEmptyVolumeCache2** hereda de **IEmptyVolumeCache**, agregando solo el método adicional **InitializeEx**, se requiere relativamente poco trabajo adicional para implementar ambos. A menos que el controlador esté destinado solo a uno de estos sistemas operativos, debe exportar ambas interfaces.

Para exportar estas interfaces, debe implementar estos métodos correspondientes a las cinco tareas básicas.

-   [Initialize/InitializeEx](#initializeinitializeex)
-   [GetSpaceUsed](#getspaceused)
-   [ShowProperties](#showproperties)
-   [Purgar](#purge)
-   [Desactivación](#deactivate)

### <a name="initializeinitializeex"></a>Initialize/InitializeEx

Se llama a los dos métodos de inicialización, que son bastante similares, cuando se ejecuta la utilidad Limpieza de disco. El Windows limpieza de disco 98 llama al método [**IEmptyVolumeCache::Initialize de un**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) controlador. El administrador de limpieza de discos Windows Millennium Edition (Windows Me), Windows 2000 o Windows XP, sin embargo, primero intenta llamar a [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) y solo usa **IEmptyVolumeCache::Initialize** si el controlador no expone [**IEmptyVolumeCache2.**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) El administrador de limpieza de disco pasa información al método , como la clave del Registro del controlador y el volumen de disco que se va a limpiar.

Cualquiera de los métodos puede devolver varias cadenas de presentación y establecer una o varias marcas. La diferencia principal entre los dos métodos es cómo se controla el texto mostrado en el administrador de limpieza de disco. Las tres cadenas siguientes se ven afectadas.



| String       | Propósito                                                                            | Inicialización                                                                           | InitializeEx                                                                                     |
|--------------|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| Display Name (Nombre para mostrar) | El nombre del controlador se muestra en el cuadro de lista del administrador de limpieza de disco.               | Si *ppwszDisplayName* es **NULL,** el valor predeterminado se recupera del Registro. | Una cadena localizada correctamente debe especificarse en *ppwszDisplayName* sin que se utilice ningún valor del Registro. |
| Descripción  | Texto descriptivo que se muestra debajo del cuadro de lista cuando se selecciona el nombre del controlador. | Si *ppwszDescription* es **NULL,** el valor predeterminado se recupera del Registro. | Una cadena localizada correctamente debe especificarse en *ppwszDescription,* no se usan valores del Registro. |
| Texto del botón  | Texto del botón opcional que permite a los usuarios mostrar la interfaz de usuario del controlador.        | No hay ningún parámetro disponible. Debe especificarse en el Registro.                           | Una cadena localizada correctamente debe especificarse en *ppwszBtnText* sin que se utilicen valores del Registro.     |



 

El *parámetro pdwFlags* que se encuentra en ambos métodos de inicialización reconoce el mismo conjunto de marcas. El administrador de limpieza de disco pasa dos de estas marcas al método .

-   **EVCF \_ SETTINGSMODE**

    Si el administrador de limpieza de disco se ejecuta según una programación, establece la marca **EVCF \_ SETTINGSMODE.** Si se establece esta marca, el administrador de limpieza de disco no llama a los [métodos GetSpaceUsed,](#getspaceused) [Purge](#purge) [o ShowProperties.](#showproperties) El método [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) o [**InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) del controlador debe controlar todas las tareas que normalmente realizan [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) y [**Purge.**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) Dado que no hay ninguna oportunidad para los comentarios de los usuarios, solo se deben tocar los archivos que son extremadamente seguros de limpiar. Debe omitir el parámetro *pcwszVolume* del método de inicialización y limpiar los archivos innecesarios independientemente de la unidad en la que se encuentran.

-   **EVCF \_ OUTOFDISKSPACE**

    Si se **establece la \_ marca EVCF OUTOFDISKSPACE,** la unidad de disco del usuario no tiene espacio suficiente. El controlador debe ser agresivo con la eliminación de archivos, incluso si se produce una pérdida de rendimiento. Sin embargo, obviamente, el controlador no debería eliminar archivos que provocarían un error en una aplicación o que el usuario perdiera los datos.

El controlador de limpieza de disco establece las marcas restantes y se devuelven al administrador de limpieza de disco. Para obtener más información, vea las páginas de referencia del método [**para IEmptyVolumeCache::Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) e [**IEmptyVolumeCache2::InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex).

-   EVCF \_ DONTSHOWIFZERO

    Muestre el controlador en el cuadro de lista del administrador de limpieza de disco solo si el valor devuelto por [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) indica que el controlador puede liberar espacio en disco.

-   EVCF \_ ENABLEBYDEFAULT

    Especifica que el controlador está habilitado de forma predeterminada. Se ejecutará cada vez que se lleve a cabo una limpieza de disco a menos que el usuario lo deshabilite desactivando la casilla en la lista de controladores del administrador de limpieza de discos.

-   EVCF \_ ENABLEBYDEFAULT \_ AUTO

    Especifica que el controlador se habilita automáticamente para ejecutarse durante las limpiezas programadas.

-   EVCF \_ HASSETTINGS

    Establezca esta marca si el controlador tiene una interfaz de usuario para mostrar. En respuesta, el administrador de limpieza de disco muestra un botón cuando ese controlador está seleccionado en el cuadro de lista. Si se hace clic en ese botón, el administrador de limpieza de disco llama [**a ShowProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties).

-   EVCF \_ REMOVEFROMLIST

    Elimine el nombre del controlador de la lista de controladores disponibles después de que el controlador se haya ejecutado una vez. También se elimina la información del Registro del controlador.

### <a name="getspaceused"></a>GetSpaceUsed

El administrador de limpieza de disco llama a este método para determinar cuánto espacio puede liberar un controlador de limpieza de disco. A continuación, el administrador de limpieza de discos muestra ese valor a la derecha del nombre del controlador en el cuadro de lista. Esta operación se realiza en todos los controladores registrados con el administrador de limpieza de discos cuando se inicia el administrador y antes de que se muestre la interfaz de usuario principal del administrador. Cuando se llama a [**GetSpaceUsed,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) el controlador debe examinar los archivos de los que es responsable, determinar cuáles de ellos son candidatos de limpieza y devolver la cantidad de espacio en disco que puede liberar.

Dado que el examen puede ser un proceso largo, el administrador de limpieza de disco usa el parámetro *picb* de este método para pasar un puntero a una [**interfaz IEmptyVolumeCacheCallBack.**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) El controlador usa la interfaz periódicamente durante el examen para llamar a [**IEmptyVolumeCacheCallBack::ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress), que sirve para dos propósitos.

-   Permite al administrador de limpieza de discos actualizar una barra de progreso e informar al usuario de cómo progresa el examen.
-   Notifica al controlador que detenga el examen en caso  de que se haga clic en el botón Cancelar de la ventana de progreso. Ese evento de botón no se comunica directamente al controlador; en su lugar, el administrador de limpieza de disco devuelve E ABORT la próxima vez que \_ [**GetSpaceUsed**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) llame a [**IEmptyVolumeCacheCallBack::ScanProgress**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress).

### <a name="showproperties"></a>ShowProperties

Antes de iniciar la limpieza, el controlador puede mostrar una interfaz de usuario normalmente en forma de ventana del Explorador de Windows que permite al usuario ver una lista de archivos o clases de archivos seleccionados para la limpieza por el controlador. Si el controlador establece la marca **\_ EVCF HASSETTINGS** cuando se llama a [**Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize) o [**InitializeEx,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) el usuario puede solicitar la interfaz de usuario haciendo clic en el botón que se muestra para ese propósito en el administrador de limpieza de disco. El texto del botón varía de controlador a controlador, pero "Ver archivos", "Ver páginas" y "Opciones" son etiquetas comunes.

Cuando se hace clic en el botón, el administrador de limpieza de disco llama a [**ShowProperties**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-showproperties) para solicitar al controlador que muestre la interfaz de usuario. La interfaz de usuario debe crearse como un elemento secundario de la ventana cuyo identificador se pasa en el *parámetro hwnd del método* **ShowProperties.**

### <a name="purge"></a>Purgar

El administrador de limpieza de disco llama al método [**Purge**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-purge) del controlador para establecer la limpieza en movimiento. El parámetro *picb* del método es un puntero a la interfaz [**IEmptyVolumeCacheCallBack**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecachecallback) del administrador de limpieza de discos. Al igual que con [**el método GetSpaceUsed,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-getspaceused) el controlador debe usar periódicamente la interfaz de devolución de llamada para informar de su progreso y consultar al administrador de limpieza de disco si el usuario ha hecho clic **en Cancelar**. Sin embargo, tenga en cuenta que el método **Purge** debe llamar a [**IEmptyVolumeCacheCallBack::P progress,**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-purgeprogress)no [**a ScanProgress.**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecachecallback-scanprogress)

### <a name="deactivate"></a>Desactivación

Se [**llama al método Deactivate**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-deactivate) cuando el administrador de limpieza de disco se prepara para apagarse. El controlador debe realizar las tareas de limpieza necesarias y devolver. Si no desea que el controlador se vuelva a ejecutar, establezca la marca **\_ EVCF REMOVEFROMLIST** en el parámetro *pdwFlags* del método de inicialización. Si se establece esta marca, el administrador de limpieza de disco quita el controlador de su lista y elimina las entradas del Registro del controlador. Debe volver a agregar las entradas del Registro para volver a ejecutar el controlador. Esta marca se usa normalmente para los controladores que se ejecutan una sola vez.

## <a name="registering-a-disk-cleanup-handler"></a>Registro de un controlador de limpieza de disco

Para agregar un controlador a la lista del administrador de limpieza de discos, se deben agregar ciertas claves y valores al registro Windows disco.

-   [Registro del CLSID de un controlador](#registering-a-handlers-clsid)
-   [Registro de un controlador con el Administrador de limpieza de discos: General](#registering-a-handler-with-the-disk-cleanup-manager-general)
-   [Registro de un controlador con el Administrador de limpieza de discos: Windows 2000 o sistemas posteriores](#registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems)
-   [Usar el objeto DataDrivenCleaner](#using-the-datadrivencleaner-object)
-   [Registro de ejemplo de un controlador de limpieza de disco](#example-registration-of-a-disk-cleanup-handler)

### <a name="registering-a-handlers-clsid"></a>Registro del CLSID de un controlador

Al igual que con todos los objetos COM, el GUID y el archivo DLL del objeto de controlador deben registrarse en la clave **CLSID** en **HKEY \_ CLASSES \_ ROOT**. También puede registrar un icono que se muestra junto al nombre del controlador en el cuadro de lista del administrador de limpieza de discos, pero esto es opcional. En el ejemplo siguiente se muestran las claves, los valores y los datos implicados.

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

### <a name="registering-a-handler-with-the-disk-cleanup-manager-general"></a>Registro de un controlador con el Administrador de limpieza de discos: General

Para completar el registro, un controlador debe agregar una clave que mantiene sus detalles, como se muestra aquí. En el resto de esta sección se describe el contenido de esta clave.

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

En general, el nombre de la clave que mantiene los detalles de un controlador se denomina para el tipo de archivo que controla, como Archivos de programa descargados, pero esto no es un requisito. En la tabla siguiente se detallan los valores posibles que se encuentran en esta clave.

> [!Note]  
> Solo se requiere el valor Predeterminado que especifica el identificador de clase (CLSID) del controlador. Todos los demás valores son opcionales.

 



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Predeterminado</td>
<td>REG_SZ</td>
<td>CLSID del controlador registrado en <strong>HKEY_CLASSES_ROOT</strong> \ <strong>CLSID</strong>.</td>
</tr>
<tr class="even">
<td>AdvancedButtonText</td>
<td>REG_SZ</td>
<td>Texto del botón opcional en el que los usuarios pueden hacer clic para mostrar la interfaz de usuario del controlador. El & se puede colocar delante de un carácter para asignar un método abreviado de teclado para el botón. Los controladores que exponen <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx omiten el valor AdvancedButtonText.</strong></a></td>
</tr>
<tr class="odd">
<td>CleanupString</td>
<td>REG_SZ</td>
<td>Línea de comandos que especifica un archivo ejecutable y parámetros de línea de comandos opcionales. Esta línea de comandos se ejecuta al finalizar la limpieza del disco.</td>
</tr>
<tr class="even">
<td>CSIDL</td>
<td>REG_DWORD</td>
<td>Identificador independiente del sistema de una carpeta especial que se incluirá en la búsqueda de archivos. Este valor debe especificarse como un valor numérico por ejemplo, 0x0000001c en lugar de CSIDL_LOCAL_APPDATA. Para obtener una lista de valores posibles, vea <a href="/windows/desktop/shell/csidl"><strong>CSIDL</strong></a>. Solo se puede usar un valor único.<br/> Si se especifica el valor Carpeta, la ubicación indicada por el valor CSIDL se antepone a esa información para crear una ruta de búsqueda. Por ejemplo, considere el siguiente escenario.<br/>
<ul>
<li>El valor CSIDL se especifica como 0x0000000d (CSIDL_MYMUSIC)</li>
<li>La carpeta My Música se encuentra en C:\Documents and Configuración\<em>username</em>\My Música</li>
<li>El valor De carpeta contiene &quot; Jazz\Lodos.&quot;</li>
</ul>
El resultado de ese escenario es que el controlador de limpieza de disco busca en la carpeta C:\Documents and Configuración\<em>username</em>\My Música\Jazz\Usernames. Tenga en cuenta que la barra diagonal que precede al valor carpeta se agrega si no está presente.<br/></td>
</tr>
<tr class="odd">
<td>Descripción</td>
<td>REG_SZ</td>
<td>Texto descriptivo que se muestra debajo del cuadro de lista del administrador de limpieza de discos cuando se selecciona el nombre del controlador. Aquí puede explicar lo que hace el controlador, los archivos con los que se preocupa y cualquier otra información que elucidatory para el usuario. Si el controlador no expone <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx,</strong></a> este texto se puede invalidar mediante el método <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> del controlador especificando una cadena alternativa en el parámetro <em>ppwszDescription</em> cuando se llama al método .</td>
</tr>
<tr class="even">
<td>Mostrar</td>
<td>REG_SZ</td>
<td>Nombre del controlador que se va a mostrar en el cuadro de lista del administrador de limpieza de disco. Si el controlador no expone <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx,</strong></a> este texto se puede invalidar mediante el método <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> del controlador especificando una cadena alternativa en el parámetro <em>ppwszDisplayName</em> cuando se llama al método .</td>
</tr>
<tr class="odd">
<td>Filelist</td>
<td>REG_SZ o REG_MULTI_SZ</td>
<td>Lista de archivos que busca y limpia este controlador. Puede especificar caracteres comodín mediante ? o * caracteres. Si el valor es de tipo REG_SZ, se separan varias extensiones mediante el | o : caracteres, sin espacios a ambos lados.<br/> Si la DDEVCF_REMOVEDIRS se establece en el valor Marcas, estos valores pueden especificar nombres de directorio, así como archivos.<br/></td>
</tr>
<tr class="even">
<td>Marcas</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Marcas que controlan los elementos del procedimiento de búsqueda y limpieza. Uno o varios de los valores siguientes.
<ul>
<li>DDEVCF_DOSUBDIRS (0x00000001). Buscar y quitar de forma recursiva.</li>
<li>DDEVCF_REMOVEAFTERCLEAN (0x00000002). Después de ejecutar el controlador una vez, quítelo del Registro.</li>
<li>DDEVCF_REMOVEREADONLY (0x00000004). Quite los archivos que cumplan los criterios de búsqueda incluso si son de solo lectura.</li>
<li>DDEVCF_REMOVESYSTEM (0x00000008). Quite los archivos que cumplan los criterios de búsqueda incluso si son archivos del sistema.</li>
<li>DDEVCF_REMOVEHIDDEN (0x00000010). Quite los archivos que cumplan los criterios de búsqueda incluso si son archivos ocultos.</li>
<li>DDEVCF_DONTSHOWIFZERO (0x00000020). No muestre este controlador en el administrador de limpieza de disco si ningún archivo coincide con sus criterios de búsqueda.</li>
<li>DDEVCF_REMOVEDIRS (0x00000040). Haga coincidir el valor de FileList con los directorios y quite las coincidencias y todos sus subdirectorios.</li>
<li>DDEVCF_RUNIFOUTOFDISKSPACE (0x00000080). Ejecute este controlador solo si el espacio en disco disponible ha quedado por debajo del valor crítico, determinado por el administrador de limpieza de disco que establece la marca EVCF_OUTOFDISKSPACE a través de <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize"><strong>IEmptyVolumeCache::Initialize</strong></a> o <a href="/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex"><strong>IEmptyVolumeCache2::InitializeEx</strong></a>.</li>
<li>DDEVCF_REMOVEPARENTDIR (0x00000100). Quite el directorio primario de los archivos especificados una vez que se haya ejecutado el limpiador.</li>
<li>DDEVCF_PRIVATE_LASTACCESS (0x10000000). Use el valor LastAccess, si se proporciona, para determinar qué archivos se deben limpiar. Esta marca se omite cuando se usa <a href="#using-the-datadrivencleaner-object">DataDrivenCleaner</a> siempre se usa cualquier valor de LastAccess proporcionado.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Carpeta</td>
<td>REG_SZ, REG_MULTI_SZ o REG_EXPAND_SZ</td>
<td>Carpetas o carpetas específicas para buscar elementos que coincidan con las entradas del valor FileList. Puede especificar caracteres comodín mediante ? o * caracteres. Si el valor es de tipo REG_SZ, se separan varios nombres de carpeta mediante el | carácter, sin espacios a ambos lados.<br/> Si hay un valor CSIDL presente, solo se puede especificar una carpeta en este valor. La ubicación indicada por el valor CSIDL se antepone a esa ruta de acceso de carpeta para crear una ruta de búsqueda. Para obtener un ejemplo, vea la descripción del valor CSIDL.<br/> Si este valor no está presente en Windows Vista Service Pack 1 (SP1) y versiones posteriores, el controlador de limpieza se omite y devuelve S_FALSE en la inicialización.<br/> Si este valor no está presente en la versión original de Windows Vista y versiones anteriores, se usa la carpeta raíz del volumen actual. La DDEVCF_DOSUBDIRS es necesaria en ese caso para buscar en toda la unidad. Sin ella, solo se busca en la propia carpeta raíz.<br/> Se debe especificar una unidad o unidades. Esto se puede proporcionar a través del valor CSIDL o a través de una REG_EXPAND_SZ cadena. Sin embargo, si se barrasen esas opciones, la unidad de búsqueda debe especificarse en el nombre de la carpeta. Use ?: para buscar en la carpeta de la unidad actual.<br/></td>
</tr>
<tr class="even">
<td>IconPath</td>
<td>REG_SZ o REG_EXPAND_SZ</td>
<td>Ruta de acceso al recurso del que se va a obtener un icono para usarlo en asociación con el controlador.</td>
</tr>
<tr class="odd">
<td>LastAccess</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Número de días que deben haber transcurrido desde que se tuvo acceso por última vez a un archivo o se creó un directorio para ese archivo o directorio que se debe tener en cuenta para la limpieza.</td>
</tr>
<tr class="even">
<td>Prioridad</td>
<td>REG_DWORD o REG_BINARY</td>
<td>Determina el orden en que se ejecuta el controlador con respecto a otros controladores. Cuanto mayor sea el número, más arriba en el proceso que ejecuta el controlador. No hay ningún intervalo definido que ningún número sea aceptable.</td>
</tr>
<tr class="odd">
<td>PropertyBag</td>
<td>REG_SZ</td>
<td>CLSID de un recurso que se usa para proporcionar texto localizado para el nombre para mostrar, la descripción y el texto del botón. Este recurso es útil en la situación en la que un controlador no implementa <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache"><strong>IEmptyVolumeCache</strong></a> y el controlador se ejecuta en Microsoft Windows NT o Windows XP.<br/> El administrador de limpieza de disco comprueba primero si la rutina de inicialización del controlador devolvió esas cadenas, como sería el caso cuando se implementa <a href="/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2"><strong>IEmptyVolumeCache2.</strong></a> Si no lo hace, el administrador se convierte a continuación en un bolsa de propiedades denominado en este valor. Si no se ha proporcionado ninguno, recupera el texto del Registro.<br/></td>
</tr>
<tr class="even">
<td>StateFlags</td>
<td>REG_DWORD</td>
<td>Al ejecutar el archivo ejecutable del administrador de limpieza de Cleanmgr.exe desde una línea de comandos, puede declarar <em>perfiles de limpieza</em>. Estos perfiles se componen de un subconjunto de los controladores disponibles y reciben una etiqueta numérica única. Esto le permite automatizar la ejecución de diferentes conjuntos de controladores en momentos diferentes.<br/> La línea de &quot; comandoscleanmgr.exe /sageset:<strong>nnnn</strong>, donde &quot; <strong>nnnn</strong> es una etiqueta numérica única, muestra una interfaz de usuario que permite elegir los controladores que se incluirán en ese perfil. Además de definir el perfil, el parámetro sageset también escribe un valor denominado StateFlags<strong>nnnn,</strong>donde <strong>nnnn</strong> es la etiqueta que usó en el parámetro , en todas las subclaves de <strong>VolumeCaches</strong>. Hay dos valores de datos posibles para esas entradas.
<ul>
<li>0: No ejecute este controlador cuando se ejecute este perfil.</li>
<li>2: Incluya este controlador cuando se ejecute este perfil.</li>
</ul>
<br/> Por ejemplo, supongamos que se ejecuta &quot; lacleanmgr.exe de comandos de /sageset:1234. &quot; En la interfaz de usuario que se presenta, el usuario elige Archivos de <strong>programa descargados,</strong>pero no archivos <strong>temporales de Internet.</strong> A continuación, los siguientes valores se escriben en el Registro.<br/>
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
<br/> La línea de &quot; comandoscleanmgr.exe /sagerun:<strong>nnnn</strong>, donde el valor de &quot; <strong>nnnn coincide</strong> con la etiqueta declarada con el parámetro sageset, ejecuta todos los controladores seleccionados en ese perfil.<br/> Un valor StateFlags genérico se escribe en el Registro cuando la limpieza de disco se ejecuta con normalidad. Este valor simplemente almacena el estado (activado o desactivado) del controlador la última vez que se presentó como una opción para el usuario. Hay dos valores de datos posibles para esas entradas.
<ul>
<li>0: no se seleccionó el controlador.</li>
<li>1: se seleccionó el controlador.</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="registering-a-handler-with-the-disk-cleanup-manager-windows-2000-or-later-systems"></a>Registro de un controlador con el Administrador de limpieza de discos: Windows 2000 o sistemas posteriores

Especificar texto para mostrar en el Registro puede dificultar la localización del software. Por este motivo, Windows 2000 y Windows XP admiten la interfaz [**IEmptyVolumeCache2**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2) con su método de inicialización [**preferido InitializeEx**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex). En Windows 2000 o posterior, siempre se intenta llamar a **IEmptyVolumeCache2::InitializeEx** antes de [**IEmptyVolumeCache::Initialize**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache-initialize). El sistema solo usa **Initialize** para inicializar un controlador si no se expone **IEmptyVolumeCache2.**

Con respecto al Registro, la única diferencia en Windows 2000 o posterior es que puede omitir los valores AdvancedButtonText, Display y Description cuando el controlador expone [**IEmptyVolumeCache2::InitializeEx.**](/windows/desktop/api/Emptyvc/nf-emptyvc-iemptyvolumecache2-initializeex) Esos valores, que contienen texto localizado correctamente, se proporcionan al administrador de limpieza de disco cuando llama **a InitializeEx**.

### <a name="using-the-datadrivencleaner-object"></a>Usar el objeto DataDrivenCleaner

El sistema operativo proporciona un controlador básico de limpieza de disco, denominado DataDrivenCleaner. Para usar este objeto como controlador en lugar de implementar el suyo propio, use el CLSID {C0E13E61-0CC6-11d1-BBB6-0060978B2AE6} como el valor predeterminado de la subclave del controlador en **VolumeCaches,** como se describe en Registro de un controlador con el Administrador de limpieza de [disco: General.](#registering-a-handler-with-the-disk-cleanup-manager-general)

DataDrivenCleaner no expone [**IEmptyVolumeCache2,**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)por lo que los valores Display y Description se proporcionan a través del Registro. Al declarar esas cadenas, tenga en cuenta que esto podría causar problemas de localización. El texto localizado se puede proporcionar a través del valor PropertyBag. El valor AdvancedButtonText se omite porque no hay ninguna interfaz de usuario y, por tanto, no hay ningún botón para mostrarlo, está disponible para este controlador.

### <a name="example-registration-of-a-disk-cleanup-handler"></a>Registro de ejemplo de un controlador de limpieza de disco

A continuación se muestra un registro de ejemplo para un controlador de limpieza de disco implementado por The Teléfono Company. Este controlador implementa tanto [**IEmptyVolumeCache**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache) como [**IEmptyVolumeCache2,**](/windows/desktop/api/Emptyvc/nn-emptyvc-iemptyvolumecache2)por lo que proporciona los valores AdvancedButtonText, Description y Display en caso de que se utilice en un equipo que ejecute Windows 98. El controlador combina los valores CSIDL y Folder para buscar archivos en el directorio C: Archivos de programa El directorio temporal de empresa de Teléfono y la marca \\ \\ \\ DDEVCF DOSUBDIRS se establecen para que también se busquen sus \_ subdirectorios. Solo se consideran para la limpieza los archivos con extensiones .tmp y .tpc, y se establece la marca DDEVCF PRIVATE LASTACCESS para que, de esos archivos, solo se tengan en cuenta aquellos a los que no se haya accedido durante 14 días o \_ \_ más. La marca DDEVCF DONTSHOWIFZERO también se establece para que el controlador no aparezca en la lista a menos que haya encontrado \_ candidatos de limpieza.

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

 

