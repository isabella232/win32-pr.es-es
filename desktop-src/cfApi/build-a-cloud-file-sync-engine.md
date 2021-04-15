---
description: Obtenga información sobre cómo crear un motor de sincronización de archivos en la nube que use archivos de marcadores de posición mediante la API de archivos en la nube.
title: Compilar un motor de sincronización en la nube que admita archivos de marcadores de posición
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: 4f1330285d0c8ef0359639f2be84162f8bc2ef3b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104554746"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>Compilar un motor de sincronización en la nube que admita archivos de marcadores de posición

Un motor de sincronización es un servicio que sincroniza los archivos, normalmente entre un host remoto y un cliente local. Los motores de sincronización en Windows suelen presentar esos archivos al usuario a través del sistema de archivos de Windows y el explorador de archivos. Antes de la versión 1709 de Windows 10, la compatibilidad con el motor de sincronización en Windows se limitaba a superficies ad hoc independientes del escenario, como el panel de navegación del explorador de archivos, la bandeja del sistema de Windows y (para aplicaciones más técnicas) controladores de filtro del sistema de archivos.

La versión 1709 de Windows 10 (también denominada Fall Creators Update) presentó la *API de archivos* en la nube. Esta API es una nueva plataforma que formaliza la compatibilidad con los motores de sincronización. La API de archivos en la nube proporciona compatibilidad con los motores de sincronización de una forma que ofrece muchas ventajas nuevas a los desarrolladores y usuarios finales.

La API de Cloud files contiene las siguientes API nativas de Win32 y las API de Windows Runtime (WinRT):

* [Cloud Filter API](cloud-filter-reference.md): esta API nativa de Win32 proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos. Esta API controla la creación y administración de archivos y directorios de marcadores de posición.
* [Espacio de nombres Windows. Storage. Provider](/uwp/api/windows.storage.provider): esta API de WinRT permite a las aplicaciones configurar el proveedor de almacenamiento en la nube y registrar la raíz de sincronización con el sistema operativo.

> [!NOTE]
> La API de Cloud files no admite actualmente la implementación de motores de sincronización en la nube en aplicaciones para UWP. Los motores de sincronización en la nube deben implementarse en aplicaciones de escritorio.

## <a name="supported-features"></a>Características admitidas

La API de archivos en la nube proporciona las siguientes características para crear motores de sincronización en la nube.

### <a name="placeholder-files"></a>Archivos de marcadores de posición

* Los motores de sincronización pueden crear archivos de marcadores de posición que solo consumen 1 KB de almacenamiento para el encabezado filesystem y que se convierten automáticamente en archivos completos en condiciones de uso normales. Los archivos de marcador de posición se presentan como archivos típicos en las aplicaciones y a los usuarios finales en el shell de Windows.
* Los archivos de marcador de posición se integran verticalmente desde el kernel de Windows hasta el shell de Windows y, por lo general, la compatibilidad de aplicaciones con los archivos de marcador de posición no es un problema. Tanto si usa las API del sistema de archivos, el símbolo del sistema o una aplicación de escritorio o de UWP para tener acceso a un archivo de marcador de posición, el archivo se hidratará sin cambios de código adicionales y esa aplicación podrá usar el archivo normalmente.
* Los archivos pueden existir en tres Estados:
  * **Archivo de marcador de posición**: representación vacía del archivo y solo está disponible si el servicio de sincronización está disponible.
  * **Archivo completo**: el archivo se ha hidratado implícitamente y podría ser deshidratado por el sistema si se necesita espacio.
  * **Archivo completo anclado**: el usuario ha hidratado explícitamente el archivo a través del explorador de archivos y se garantiza que está disponible sin conexión.

En la imagen siguiente se muestra cómo se muestran los Estados de los archivos completos de marcador de posición, completos y anclados en el explorador de archivos.

  ![Ejemplo de tres Estados de archivo en el explorador de archivos](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>Registro de la raíz de sincronización normalizada

* El registro de una raíz de sincronización es sencillo y estandarizado. Esto incluye la creación de un nodo de marca en el panel de navegación del explorador de archivos, tal como se muestra en la siguiente captura de pantalla. Las raíces se pueden crear como entradas de nivel superior individuales o como elementos secundarios de una agrupación primaria.

  ![Ejemplo de una entrada de la raíz de sincronización en el explorador de archivos](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Integración de Shell

* Iconos de estado:
  * La API de archivos en la nube proporciona iconos de estado de hidratación automática y estandarizados que se muestran en el explorador de archivos y en el escritorio de Windows.
  * Además de los iconos de estado de Windows estándar que se usan para el estado de la hidratación, puede proporcionar iconos de estado personalizados para propiedades adicionales específicas del servicio.
  * Reemplaza las extensiones de Shell de superposición de iconos heredadas.
* Indicación de progreso:
  * Abrir un archivo de marcador de posición que tarde más de unos segundos en hidratos mostrará el progreso de la hidratación. El progreso se muestra en algunas ubicaciones en función del contexto:
    * En una ventana del cuadro de diálogo del motor de copia.
    * El progreso en línea se muestra junto al archivo en el explorador de archivos.
    * Si el archivo no se abre en la instrucción específica del usuario, se muestra una notificación del sistema para informar al usuario y proporcionar una manera de controlar la actividad de la hidratación no deseada.
* Miniaturas y metadatos:
  * Los archivos de marcadores de posición pueden tener miniaturas enriquecidas proporcionadas por el servicio y metadatos de archivos extendidos para proporcionar al usuario una experiencia de explorador de archivos sin problemas.
* Panel de navegación del explorador de archivos:
  * El registro de una raíz de sincronización con la API de archivos en la nube hace que la raíz de sincronización (con un icono y un nombre personalizado) aparezca en el panel de navegación del explorador de archivos.
* Menús contextuales del explorador de archivos:
  * Al registrar una raíz de sincronización con la API de archivos en la nube, se proporcionan automáticamente varios verbos (entradas de menú) en el menú contextual del explorador de archivos que permiten al usuario controlar el estado de la hidratación del archivo.
  * Se pueden agregar verbos adicionales a esta sección del menú contextual mediante las API compatibles con puente de escritorio.
* Control de usuario de la hidratación de archivos:
  * Los usuarios siempre tienen el control de la hidratación de archivos, incluso cuando el usuario no ha hidratado explícitamente los archivos. Se muestra una notificación del sistema interactiva para la hidratación en segundo plano para avisar al usuario y proporcionar opciones. En la imagen siguiente se muestra una notificación del sistema para un archivo Hydrating.
    ![Ejemplo de un sistema interactivo que se muestra para la hidratación de archivos en segundo plano](images/file-hydration-interactive-toast.png)
  * Si un usuario bloquea una aplicación de archivos Hydrating a través de una notificación del sistema interactiva, puede desbloquear la aplicación en la página de **descargas automáticas de archivos** en **configuración**.
    ![Captura de pantalla de la configuración de descargas de archivos automáticas](images/allow-automatic-file-downloads-setting.png)
* Enlazar operaciones del motor de copia (admitidas en Windows 10 Insider Preview compilación 19624 y versiones posteriores):
  * Los proveedores de almacenamiento en la nube pueden registrar un enlace de copia de Shell para supervisar las operaciones de archivo dentro de su raíz de sincronización.
  * El proveedor registra su enlace de copia estableciendo el valor del registro **CopyHook** en la clave del Registro raíz de sincronización en el CLSID de su objeto de servidor local com. Este objeto de servidor local implementa la interfaz [IStorageProviderCopyHook](../shell/nn-shobjidl-istorageprovidercopyhook.md) .

### <a name="desktop-bridge"></a>Puente de dispositivo de escritorio

* Los motores de sincronización que usan las API de archivos en la nube están diseñados para usar el [puente de escritorio](/windows/uwp/porting/desktop-to-uwp-root) como un requisito de implementación.

## <a name="cloud-mirror-sample"></a>Ejemplo de reflejo en la nube

El [ejemplo de reflejo](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror) en la nube muestra cómo compilar una solución que usa la API de archivos en la nube. No está diseñado para usarse como código de producción. Carece de un control de errores robusto y se escribe para que sea lo más fácil de entender posible. Se denomina reflejo en la nube porque simplemente refleja una carpeta local en el disco local. Especifique una carpeta de servidor que esté pensada para representar el servidor de archivos en la nube y una carpeta de cliente diseñada para especificar la ruta de acceso raíz de sincronización. Aparece un nodo de nivel superior en el panel de navegación del explorador de archivos denominado **TestStorageProviderDisplayName** y este nodo se asigna a la carpeta de cliente especificada.

En lo que respecta a la sincronización, estos son los elementos que debe implementar un proveedor de sincronización de archivos en la nube completamente desarrollados:

* Cuando el archivo raíz de sincronización es simplemente un marcador de posición, el servicio es responsable de copiar el contenido del archivo para la hidratación. Esto se implementa en el ejemplo.
* Cuando el archivo raíz de sincronización es un archivo completo y el contenido del archivo en el servicio en la nube cambia, el servicio es responsable de notificar al cliente de sincronización local del cambio y el cliente de sincronización local debe administrar las combinaciones según sus propias especificaciones. Esto no se implementa en el ejemplo.
* Cuando el archivo raíz de sincronización es un archivo completo y el contenido del archivo en la ruta de acceso raíz de sincronización (el cliente local) cambia, el cliente de sincronización local debe notificar al servicio en la nube y controlar las combinaciones según sus propias especificaciones. La notificación de cambio de archivo local se implementa en el ejemplo, pero no hace nada.

### <a name="use-the-sample"></a>Usar el ejemplo

1. Cree dos carpetas en la unidad de disco duro local. Uno de ellos actuará como el servidor y el otro como cliente.
2. Agregue algunos archivos a la carpeta del servidor. Asegúrese de que la carpeta de cliente está vacía.
3. Abra el ejemplo de reflejo en la nube en Visual Studio. Establezca el proyecto **CloudMirrorPackage** como proyecto de inicio y, después, compile y ejecute el ejemplo. Cuando el ejemplo lo solicite, escriba las dos rutas de acceso a las carpetas del servidor y del cliente. Después, verá una ventana de consola con información de diagnóstico.
4. Abra el explorador de archivos y confirme que ve el nodo **TestStorageProviderDisplayName** y los marcadores de posición de todos los archivos que copió en la carpeta del servidor. Para simular una aplicación que intente abrir archivos sin usar el selector, copie varias imágenes en la carpeta del servidor. Haga doble clic en una de ellas en la carpeta raíz de sincronización y confirme que está hidratada. A continuación, abra la aplicación fotos. La aplicación cargará previamente los archivos adyacentes en segundo plano para que sea más probable que el usuario no experimente retrasos al examinar las demás imágenes. Puede observar que la deshidratación en segundo plano se produce a través de notificaciones del sistema o en el explorador de archivos.
5. Haga clic con el botón derecho en un archivo en el explorador de archivos para abrir un menú contextual y confirme que ve el elemento de menú **prueba** . Al hacer clic en este elemento de menú, se mostrará un cuadro de mensaje.
6. Para detener el ejemplo, establezca el foco en la salida de la consola y presione **Ctrl + C**. Esto limpiará el registro de la raíz de sincronización para que el proveedor se desinstale. Si el ejemplo se bloquea, es posible que la raíz de sincronización permanezca registrada. Esto hará que el explorador de archivos se reinicie cada vez que haga clic en cualquier cosa, y se le pedirán las ubicaciones de cliente y servidor falsas. Si esto ocurre, desinstale la aplicación de ejemplo **CloudMirrorPackage** del equipo.

### <a name="sample-architecture"></a>Arquitectura de ejemplo

El ejemplo es deliberadamente simple. Utiliza clases estáticas para hacer que sea innecesario pasar punteros de instancia. Estas son las clases principales en el ejemplo:

* **FakeCloudProvider**: esta clase de nivel superior controla las siguientes clases de trabajo:
  * **CloudProviderRegistrar**: registra la información raíz de la sincronización con el shell de Windows.
  * **Marcadores de posición**: genera los archivos de marcador de posición en la ruta de acceso raíz de sincronización.
  * **ShellServices**: construye los proveedores de Shell de Windows para el menú contextual, las miniaturas y otros servicios.
  * **CloudProviderSyncRootWatcher**: crea una instancia de DirectoryWatcher para supervisar los cambios en la ruta de acceso raíz de sincronización y actúa en los cambios.
  * **FileCopierWithProgress**: copia los archivos de la carpeta del servidor en la carpeta cliente lentamente en fragmentos para simular su descarga desde un servidor en la nube real. Proporciona una indicación de progreso para que la interfaz de usuario del explorador de archivos y notificaciones del sistema muestre el usuario algo informativo.

Además de las clases anteriores, el ejemplo también proporciona varias clases auxiliares para solicitar al usuario carpetas y algunas utilidades. **TestExplorerCommandHandler**, **CustomStateProvider**, **ThumbnailProvider** y **UriSource** son ejemplos de proveedores de servicios de Shell.

## <a name="cloud-files-api-architecture"></a>Arquitectura de API de archivos en la nube

En el núcleo de la pila de almacenamiento de la API de archivos en la nube se encuentra un controlador de minifiltro del sistema de archivos denominado cldflt.sys. Este controlador actúa como un proxy entre las aplicaciones del usuario y el motor de sincronización. El motor de sincronización sabe cómo descargar y cargar los datos a petición, mientras que es responsabilidad de cldflt.sys trabajar con el shell para presentar archivos como si los datos de la nube estuvieran disponibles localmente.

Actualmente, Cldflt.sys solo admite volúmenes NTFS, ya que depende de algunas características únicas de NTFS.

Hay muchos controladores de minifiltro del sistema de archivos en un sistema y pueden estar activos en un volumen determinado al mismo tiempo. Los controladores que son de mayor interés para la API de archivos en la nube son los filtros del sistema de archivos antivirus.

Los controladores de minifiltro del sistema de archivos se administran y admiten en un componente especial en modo kernel denominado administrador de filtros. Entre otras muchas tareas, el administrador de filtros facilita la comunicación sin filtrar entre los filtros y los componentes de modo de usuario a través de una construcción conocida como puerto de mensajes de filtro.

## <a name="hydration-policies"></a>Directivas de hidratación

Windows admite una variedad de [directivas de hidratación principal](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary) y los modificadores de la [Directiva de hidratación secundaria](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier) . Las directivas de hidratación principales tienen este orden:

  **Always Full > Full > progresivo > parcial**

Tanto las aplicaciones como los motores de sincronización pueden definir su Directiva de hidratación principal preferida. Si no se especifica, la Directiva de hidratación predeterminada es progresiva para las aplicaciones y los motores de sincronización.

La Directiva de hidratación de un archivo en la nube se determina en el momento de apertura del archivo mediante esta fórmula:

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

Por ejemplo, supongamos que el usuario está intentando abrir un archivo PDF almacenado en la unidad de nube de Fabrikam mediante el visor de PDF de Contoso, que no especifica una directiva de hidratación preferida. La Directiva de hidratación de aplicaciones es, por lo tanto, la hidratación progresiva, en este caso de forma predeterminada. Sin embargo, dado que la unidad de nube de Fabrikam es un motor de sincronización de hidratación completo, la última Directiva de hidratación en el archivo se convierte en una hidratación completa, lo que hará que el archivo se quede completamente hidratado en el primer acceso. El mismo resultado se produce en los casos en los que el motor de sincronización admite la hidratación progresiva, pero la preferencia de la aplicación es la hidratación completa.

Tenga en cuenta que la Directiva de hidratación de archivos no se puede cambiar una vez abierto el archivo.

## <a name="compatibility-with-applications-that-use-reparse-points"></a>Compatibilidad con aplicaciones que usan puntos de análisis

La API de Cloud files implementa el sistema de marcadores de posición mediante [puntos de reanálisis](/windows/desktop/FileIO/reparse-points). Una idea equivocada común sobre los puntos de reanálisis es que son los mismos que los vínculos simbólicos. Este error de concepto se refleja ocasionalmente en las implementaciones de la aplicación y, como resultado, muchas aplicaciones existentes alcanzan errores al encontrar cualquier punto de reanálisis.

Para mitigar este problema de compatibilidad, la API de archivos en la nube oculta siempre sus puntos de análisis de todas las aplicaciones excepto los motores y procesos de sincronización cuya imagen principal reside en **% systemroot%**. Las aplicaciones que entienden los puntos de análisis correctamente pueden forzar a la plataforma a exponer los puntos de reanálisis de API de los archivos en la nube mediante [RtlSetProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) o [RtlSetThreadProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode).