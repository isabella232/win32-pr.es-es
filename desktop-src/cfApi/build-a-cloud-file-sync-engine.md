---
description: Aprenda a crear un motor de sincronización de archivos en la nube que use archivos de marcador de posición mediante la API de archivos en la nube.
title: Compilación de un motor de sincronización en la nube que admita archivos de marcador de posición
ms.topic: article
ms.date: 11/12/2020
ms.openlocfilehash: d7d1efae4a56e6f52473002953730fb9f1f9459f1ed8dc82e0ba75ddebf05dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551582"
---
# <a name="build-a-cloud-sync-engine-that-supports-placeholder-files"></a>Compilación de un motor de sincronización en la nube que admita archivos de marcador de posición

Un motor de sincronización es un servicio que sincroniza archivos, normalmente entre un host remoto y un cliente local. Los motores de sincronización Windows suelen presentar esos archivos al usuario a través del sistema de archivos Windows y Explorador de archivos. Antes de Windows 10, versión 1709, la compatibilidad del motor de sincronización en Windows se limitaba a superficies ad hoc independientes del escenario, como el panel de navegación de Explorador de archivos, la bandeja del sistema de Windows y los controladores de filtro del sistema de archivos (para aplicaciones más técnicas).

Windows 10 versión 1709 (también denominada Fall Creators Update) introdujo la *API de archivos en la nube*. Esta API es una nueva plataforma que formaliza la compatibilidad con los motores de sincronización. La API de archivos en la nube proporciona compatibilidad con los motores de sincronización de una manera que ofrece muchas ventajas nuevas a los desarrolladores y usuarios finales.

La API de archivos en la nube contiene las siguientes API nativas de Win32 y Windows Runtime (WinRT):

* [CLOUD Filter API:](cloud-filter-reference.md)esta API nativa de Win32 proporciona funcionalidad en el límite entre el modo de usuario y el sistema de archivos. Esta API controla la creación y administración de archivos y directorios de marcador de posición.
* [Windows. Storage. Espacio de nombres del](/uwp/api/windows.storage.provider)proveedor: esta API de WinRT permite a las aplicaciones configurar el proveedor de almacenamiento en la nube y registrar la raíz de sincronización con el sistema operativo.

> [!NOTE]
> La API de archivos en la nube no admite actualmente la implementación de motores de sincronización en la nube en aplicaciones para UWP. Los motores de sincronización en la nube deben implementarse en aplicaciones de escritorio.

## <a name="supported-features"></a>Características admitidas

La API de archivos en la nube proporciona las siguientes características para crear motores de sincronización en la nube.

### <a name="placeholder-files"></a>Archivos de marcador de posición

* Los motores de sincronización pueden crear archivos de marcador de posición que consumen solo 1 KB de almacenamiento para el encabezado del sistema de archivos y que se hidratan automáticamente en archivos completos en condiciones de uso normal. Los archivos de marcador de posición se presentan como archivos típicos a las aplicaciones y a los usuarios finales en Windows Shell.
* Los archivos de marcador de posición se integran verticalmente desde el kernel de Windows hasta Windows Shell, y la compatibilidad de la aplicación con los archivos de marcador de posición suele ser un problema. Tanto si usa las API del sistema de archivos, el símbolo del sistema, un escritorio o una aplicación para UWP para acceder a un archivo de marcador de posición, el archivo se hidratará sin cambios de código adicionales y esa aplicación puede usar el archivo normalmente.
* Los archivos pueden existir en tres estados:
  * **Archivo de marcador** de posición: una representación vacía del archivo y solo disponible si el servicio de sincronización está disponible.
  * **Archivo completo:** el archivo se ha hidratado implícitamente y el sistema podría deshidratarlo si se necesita espacio.
  * **Archivo completo anclado:** el usuario ha hidratado explícitamente el archivo a través de Explorador de archivos y se garantiza que está disponible sin conexión.

En la imagen siguiente se muestra cómo se muestran los estados de archivo completo, completo y anclado del marcador de posición en Explorador de archivos.

  ![Ejemplo de tres estados de archivo en Explorador de archivos](images/cloud-file-states-file-explorer.png)

### <a name="standardized-sync-root-registration"></a>Registro raíz de sincronización estandarizado

* El registro de una raíz de sincronización es sencillo y estandarizado. Esto incluye la creación de un nodo de marca en el panel de navegación Explorador de archivos, como se muestra en la captura de pantalla siguiente. Las raíces se pueden crear como entradas individuales de nivel superior o como elementos secundarios de una agrupación primaria.

  ![Ejemplo de una entrada raíz de sincronización en Explorador de archivos](images/register-sync-root-file-explorer.png)

### <a name="shell-integration"></a>Integración de Shell

* Iconos de estado:
  * La API de archivos en la nube proporciona iconos de estado de hidratación estandarizados y automáticos que se muestran en Explorador de archivos y en Windows escritorio.
  * Además de los iconos de Windows de estado estándar que se usan para el estado de hidratación, puede proporcionar iconos de estado personalizados para propiedades adicionales específicas del servicio.
  * Reemplaza las extensiones de Shell superpuestas a iconos heredados.
* Indicación de progreso:
  * Al abrir un archivo de marcador de posición que tarda más de unos segundos en hidratarse, se mostrará el progreso de la hidratación. El progreso se muestra en algunas ubicaciones en función del contexto:
    * En una ventana de diálogo del motor de copia.
    * El progreso en línea se muestra junto al archivo en Explorador de archivos.
    * Si el archivo no se abre en la instrucción específica del usuario, se muestra una notificación del sistema para informar al usuario y proporcionar una manera de controlar la actividad de hidratación no deseada.
* Miniaturas y metadatos:
  * Los archivos de marcador de posición pueden tener miniaturas enriquecciones proporcionadas por el servicio y metadatos de archivo extendidos para proporcionar al usuario una experiencia Explorador de archivos sin problemas.
* Explorador de archivos panel de navegación:
  * El registro de una raíz de sincronización con la API de archivos en la nube hace que esa raíz de sincronización (con un icono y un nombre personalizado) aparezca en Explorador de archivos panel de navegación del usuario.
* Explorador de archivos menús contextuales:
  * El registro de una raíz de sincronización con la API de archivos en la nube proporciona automáticamente varios verbos (entradas de menú) en el menú contextual de Explorador de archivos que permiten al usuario controlar el estado de hidratación de su archivo.
  * Se pueden agregar verbos adicionales a esta sección del menú contextual mediante Puente de dispositivo de escritorio API compatibles.
* Control de usuario de la hidratación de archivos:
  * Los usuarios siempre controlan la hidratación de archivos, incluso cuando el usuario no hidrata explícitamente los archivos. Se muestra un sistema interactivo para la hidratación en segundo plano para alertar al usuario y proporcionar opciones. En la imagen siguiente se muestra una notificación del sistema para un archivo de hidratación.
    ![Ejemplo de un sistema interactivo que se muestra para la hidratación de archivos en segundo plano](images/file-hydration-interactive-toast.png)
  * Si un usuario impide que una aplicación pueda hidratar archivos a  través de un sistema interactivo, puede desbloquear la aplicación en la página Descargas automáticas de archivos **Configuración**.
    ![Captura de pantalla de la configuración de descargas automáticas de archivos](images/allow-automatic-file-downloads-setting.png)
* Enlazar operaciones del motor de copia (admitidas en Windows 10 Insider Preview Build 19624 y versiones posteriores):
  * Los proveedores de almacenamiento en la nube pueden registrar un enlace de copia de shell para supervisar las operaciones de archivo dentro de su raíz de sincronización.
  * El proveedor registra su enlace de copia estableciendo el valor del Registro **CopyHook** bajo su clave del Registro raíz de sincronización en un CLSID de su objeto de servidor local COM. Este objeto de servidor local implementa la [interfaz IStorageProviderCopyHook.](../shell/nn-shobjidl-istorageprovidercopyhook.md)

### <a name="desktop-bridge"></a>Puente de dispositivo de escritorio

* Los motores de sincronización mediante las API de archivos en la nube están diseñados para usar el [Puente de dispositivo de escritorio](/windows/uwp/porting/desktop-to-uwp-root) como requisito de implementación.

## <a name="cloud-mirror-sample"></a>Ejemplo de Cloud Mirror

En [el ejemplo de Cloud Mirror](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/CloudMirror) se muestra cómo crear una solución que usa la API de archivos en la nube. No está pensado para usarse como código de producción. Carece de un control de errores sólido y está escrito para que se entienda lo más fácilmente posible. Se denomina Reflejo en la nube porque simplemente refleja una carpeta local en el disco local. Especifique una carpeta de servidor que esté pensada para representar el servidor de archivos en la nube y una carpeta de cliente que esté pensada para especificar la ruta de acceso raíz de sincronización. Aparece un nodo de nivel superior en el panel de navegación de Explorador de archivos denominado **TestStorageProviderDisplayName** y este nodo se asigna a la carpeta de cliente especificada.

En lo que respecta a la sincronización, estos son los aspectos que debe implementar un proveedor de sincronización de archivos en la nube totalmente desarrollado:

* Cuando el archivo raíz de sincronización es simplemente un marcador de posición, el servicio es responsable de copiar el contenido del archivo para la hidratación. Esto se implementa en el ejemplo.
* Cuando el archivo raíz de sincronización es un archivo completo y el contenido del archivo en el servicio en la nube cambia, el servicio es responsable de notificar al cliente de sincronización local del cambio y el cliente de sincronización local debe controlar las mezclas según sus propias especificaciones. Esto no se implementa en el ejemplo.
* Cuando el archivo raíz de sincronización es un archivo completo y el contenido del archivo en la ruta de acceso raíz de sincronización (el cliente local) cambia, el cliente de sincronización local debe notificar al servicio en la nube y controlar las mezclas según sus propias especificaciones. La notificación de cambio de archivo local se implementa en el ejemplo, pero no hace nada.

### <a name="use-the-sample"></a>Uso del ejemplo

1. Cree dos carpetas en el disco duro local. Uno de ellos actuará como servidor y el otro como cliente.
2. Agregue algunos archivos a la carpeta del servidor. Asegúrese de que la carpeta de cliente está vacía.
3. Abra el ejemplo de Cloud Mirror en Visual Studio. Establezca el **proyecto CloudMirrorPackage** como proyecto de inicio y, a continuación, compile y ejecute el ejemplo. Cuando se le solicite en el ejemplo, escriba las dos rutas de acceso a las carpetas de servidor y cliente. Después, verá una ventana de consola con información de diagnóstico.
4. Abra Explorador de archivos y confirme que ve el nodo **TestStorageProviderDisplayName** y los marcadores de posición de todos los archivos que copió en la carpeta del servidor. Para simular una aplicación que intenta abrir archivos sin usar el selector, copie varias imágenes en la carpeta del servidor. Haga doble clic en uno de ellos en la carpeta raíz de sincronización y confirme que se hidrata. A continuación, abra Fotos aplicación. La aplicación cargará previamente los archivos adyacentes en segundo plano para que sea más probable que el usuario no experimente retrasos al mirar las otras imágenes. Puede observar que la deshidratación en segundo plano se realiza a través de notificaciones del sistema o en Explorador de archivos.
5. Haga clic con el botón derecho en Explorador de archivos abrir un menú contextual y confirme que ve el **elemento de menú TestCommand.** Al hacer clic en este elemento de menú se mostrará un cuadro de mensaje.
6. Para detener el ejemplo, establezca el foco en la salida de la consola y **presione Ctrl+C.** Esto limpiará el registro raíz de sincronización para que se desinstale el proveedor. Si el ejemplo se bloquea, es posible que la raíz de sincronización permanezca registrada. Esto hará que Explorador de archivos se reinicie cada vez que haga clic en cualquier cosa y se le pedirán las ubicaciones de cliente y servidor falsas. Si esto ocurre, desinstale la aplicación de ejemplo **CloudMirrorPackage** del equipo.

### <a name="sample-architecture"></a>Arquitectura de muestra

El ejemplo es deliberadamente sencillo. Usa clases estáticas para que no sea necesario pasar punteros de instancia. Estas son las clases principales del ejemplo:

* **FakeCloudProvider:** esta clase de nivel superior controla las siguientes clases de trabajo:
  * **CloudProviderRegistrar:** registra la información raíz de sincronización con Windows Shell.
  * **Marcadores de posición:** genera los archivos de marcador de posición en la ruta de acceso raíz de sincronización.
  * **ShellServices:** construye los proveedores Windows Shell para el menú contextual, las miniaturas y otros servicios.
  * **CloudProviderSyncRootWatcher:** crea una instancia de DirectoryWatcher para supervisar los cambios en la ruta de acceso raíz de sincronización y actuar en función de los cambios.
  * **FileCopierWithProgress:** copia los archivos de la carpeta del servidor en la carpeta de cliente lentamente en fragmentos para simular su descarga desde un servidor en la nube real. Proporciona una indicación de progreso para que las notificaciones Explorador de archivos interfaz de usuario muestre al usuario algo informativo.

Además de las clases anteriores, el ejemplo también proporciona varias clases auxiliares para solicitar al usuario carpetas y algunas utilidades. **TestExplorerCommandHandler,** **CustomStateProvider,** **ThumbnailProvider** y **UriSource** son ejemplos de proveedores de servicios de Shell.

## <a name="cloud-files-api-architecture"></a>Arquitectura de API de archivos en la nube

En el núcleo de la pila de almacenamiento de la API de archivos en la nube se encuentra un controlador de minifiltro del sistema de archivos denominado cldflt.sys. Este controlador actúa como proxy entre las aplicaciones del usuario y el motor de sincronización. El motor de sincronización sabe cómo descargar y cargar los datos a petición, mientras que es responsabilidad de cldflt.sys trabajar con shell para presentar archivos como si los datos en la nube estuvieran disponibles localmente.

Cldflt.sys admite actualmente volúmenes NTFS porque depende de algunas características únicas de NTFS.

Hay muchos controladores de minifiltro del sistema de archivos en un sistema y pueden estar activos en un volumen determinado al mismo tiempo. Los controladores que son de mayor interés para la API de archivos en la nube son los filtros del sistema de archivos antivirus.

Los controladores de minifiltro del sistema de archivos se administran y admiten mediante un componente especial de modo kernel denominado administrador de filtros. Entre muchas otras tareas, el administrador de filtros facilita la comunicación sin filtrar entre los filtros y los componentes del modo de usuario a través de una construcción conocida como puerto de mensaje de filtro.

## <a name="hydration-policies"></a>Directivas de hidratación

Windows admite una variedad de directivas de [hidratación principales y](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_primary) [modificadores de directiva](/windows/desktop/api/cfapi/ne-cfapi-cf_hydration_policy_modifier) de hidratación secundarios. Las directivas de hidratación principal tienen este orden:

  **Always full > Full > Progressive > Partial**

Tanto las aplicaciones como los motores de sincronización pueden definir su directiva de hidratación principal preferida. Si no se especifica, la directiva de hidratación predeterminada es progresiva para las aplicaciones y los motores de sincronización.

La directiva de hidratación de un archivo en la nube se determina en el momento de la apertura del archivo mediante esta fórmula:

  ```File hydration policy = max(app hydration policy, provider hydration policy)```

Por ejemplo, supongamos que el usuario está intentando abrir un archivo PDF almacenado en Fabrikam Cloud Drive mediante el Visor de PDF de Contoso, que no especifica una directiva de hidratación preferida. Por lo tanto, la directiva de hidratación de la aplicación es una hidratación progresiva, en este caso de forma predeterminada. Sin embargo, dado que Fabrikam Cloud Drive es un motor de sincronización de hidratación completa, la directiva de hidratación final del archivo se convierte en una hidratación completa, lo que dará lugar a que el archivo esté totalmente hidratado en el primer acceso. El mismo resultado se produce en los casos en los que el motor de sincronización admite la hidratación progresiva, pero la preferencia de la aplicación es la hidratación completa.

Tenga en cuenta que la directiva de hidratación de archivos no se puede cambiar después de abrir el archivo.

## <a name="compatibility-with-applications-that-use-reparse-points"></a>Compatibilidad con aplicaciones que usan puntos de reanción

La API de archivos en la nube implementa el sistema de marcadores de posición mediante [puntos de rean aproximado.](/windows/desktop/FileIO/reparse-points) Un concepto erróneo común sobre los puntos de reanuso es que son iguales que los vínculos simbólicos. Esta idea errónea se refleja ocasionalmente en las implementaciones de aplicaciones y, como resultado, muchas aplicaciones existentes producen errores al encontrar cualquier punto de reanuso.

Para mitigar este problema de compatibilidad, la API de archivos en la nube siempre oculta sus puntos de reancha de todas las aplicaciones, excepto los motores de sincronización y los procesos cuya imagen principal reside en **%systemroot%.** Las aplicaciones que comprenden correctamente los puntos de reanimación pueden forzar a la plataforma a exponer puntos de reanud de API de archivos en la nube mediante [RtlSetProcessPlaceholderCompatibilityMode](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetprocessplaceholdercompatibilitymode) o [RtlSetThreadProcessPlaceholderCompatibilityMode.](/windows-hardware/drivers/ddi/content/ntifs/nf-ntifs-rtlsetthreadplaceholdercompatibilitymode)