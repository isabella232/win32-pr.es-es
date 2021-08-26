---
description: Uso de controles parentales Configuración API
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: Uso de controles parentales Configuración API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c9dd75565559e8fe52413280e35abf076a57ad6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885813"
---
# <a name="using-parental-controls-settings-apis"></a>Uso de controles parentales Configuración API

Configuración se debate antes del registro porque el registro es condicional en la configuración del usuario.

## <a name="wmi-api-settings-writeread"></a>Escritura/lectura Configuración API WMI

La API wmi proporciona acceso no abstracto (sin procesar) a todas las configuraciones de las que la infraestructura de controles parentales crea instancias, tal como se define en el archivo de esquema Wpcsprov.mof. El almacén de configuración existe en el espacio de nombres WindowsParentalControls de aplicaciones CIMV2 raíz, con las \\ \\ siguientes \\ \\ definiciones de clase que definen un esquema. Se anotan los elementos de extensibilidad.

Por equipo:

-   WpcSystemSettings (una instancia)
    -   Métodos AddUser() y RemoveUser() para crear y eliminar la configuración de controles parentales para un SID determinado, respectivamente.
    -   Propiedades del sistema de clasificaciones de juegos actual en vigor y seguimiento y notificación relacionados con la comprobación de registros por parte del administrador.
    -   Extensibilidad: propiedades para la aplicación HTTP de solo lectura y lectura/escritura y listas de exención de direcciones URL para el filtrado de contenido web, id. de invalidación del filtro de contenido web y nombre de la ruta de acceso y el identificador de DLL del recurso de nombre, y el número de eventos de registro personalizado de campos y registro de nombre de encabezado.
-   WpcRatingsSystem (una instancia por cada sistema de clasificaciones instalado)
    -   WpcRating (una instancia por nivel de clasificación).
    -   WpcRatingDescriptor (una instancia por descriptor de clasificación).
-   Extensibilidad: WpcExtension (una instancia por cada vínculo de extensibilidad del Panel de controles parentales agregado).
    -   Propiedades de GUID, subsistema, identificador, ruta de acceso de recursos de imagen, ruta de acceso de recurso de imagen de estado deshabilitado, ruta de acceso ejecutable, ruta de acceso de DLL de recursos de nombre para mostrar e identificador, ruta de acceso de DLL de recursos de subtítulos e identificador.

Por usuario controlado:

-   WpcUserSettings (una instancia por usuario controlado)
    -   Propiedades para poseer sid, controles parentales activados o desactivados, marca de inicio y cierre de sesión, marca de límites de tiempo activado/desactivado, invalida la marca habilitada, máscara de horas de inicio de sesión y marca de activado/desactivado de restricciones de aplicación generales.
    -   En Windows 8 la propiedad existente representa la primera media hora para cada hora. Se ha agregado una nueva propiedad de media hora para representar la segunda mitad de cada hora. Se introdujo una nueva propiedad adicional para representar la asignación de tiempo diaria.

        **Windows 7 y Windows Vista:** Las restricciones de temporizador admiten granularidad de 1 hora.

-   WpcWebSettings (una instancia por usuario controlado)
    -   Propiedades para poseer SID, filtrar la marca de encendido y apagado, el nivel de filtro, la marca de bloqueo de descargas de archivos, la marca de bloqueo de sitios no clasificados.
-   WpcUrlOverride (una instancia por dirección URL permitida o denegada explícitamente en la lista de invalidación de url usada como lista de permitidos o bloqueados para el filtrado de contenido web)
    -   Propiedades para poseer sid, dirección URL afectada, estado permitido o bloqueado.
-   WpcAppOverride (una instancia por ruta de acceso permitida explícitamente en la lista de invalidación de aplicaciones de restricciones de aplicación generales)
    -   Propiedades para poseer sid. Id. de regla SAFER, ruta de acceso a la aplicación.
-   WpcGamesSettings (una instancia por usuario controlado)
    -   Las propiedades para poseer SID, la marca de juegos permitidos, el GUID del sistema de clasificaciones para esta configuración, permiten la marca de juegos no clasificados, el identificador de la clasificación máxima permitida en el sistema actual y la colección de descriptores denegados.
-   WpcGameOverride (una instancia por identificador de aplicación permitida o denegada explícitamente)
    -   Propiedades para poseer sid, identificador de aplicación que identifica el juego, estado permitido o denegado.

## <a name="data-representation-notes"></a>Notas de representación de datos

Varias de las configuraciones del esquema están restringidas por el archivo .mof con el atributo non \_ null. No se pueden establecer en una variante null. Para todos los tipos que no son de matriz, el código controles parentales inicializa los valores. En el caso de las matrices, los estados vacíos se pueden escribir mediante una variante nula, una variante vacía o una matriz de variantes de tamaño cero. El proveedor WMI normalizará todos ellos en una representación de estado variante null en la lectura.

## <a name="user-interface-extensibility-link-notes"></a>Interfaz de usuario de vínculo de extensibilidad

El uso de WMI para registrar un vínculo de extensibilidad de la interfaz de usuario requiere especificar la siguiente información:

-   GUID: varios vínculos pueden compartir el mismo GUID si forman parte de un paquete o conjunto común.
-   Subsistema: diseñado para indicar clasificaciones de tipos de vínculo, como conjuntos o aplicaciones compatibles independientes
-   Nombre de la ruta de acceso dll del recurso y el identificador: especifica el recurso para el nombre para mostrar que se va a mostrar para el vínculo.
-   Id. y ruta de acceso del archivo DLL de recursos de subtítulos: especifica el recurso para el texto adicional debajo del nombre.
-   Ruta de acceso de imagen: ruta de acceso completa de un mapa de bits de 24 × 24 píxeles (BMP), con una profundidad de color de 8 bits por píxel y preferiblemente un canal alfa. Se especifica de forma coherente con las extensiones de shell: <file system path> , <negative resource ID> . Por ejemplo: C: \\ Windows \\ System32 \\Wpccpl.dll,-20.
-   Ruta de acceso de imagen deshabilitada: igual que la ruta de acceso de la imagen anterior, excepto la variante de mapa de bits que muestra el estado deshabilitado. Esta imagen se muestra cuando los controles parentales están desactivados.
-   Ruta de acceso de exe: ruta de acceso completa a un ejecutable que se invocará mediante ShellExecute(). Esta ruta de acceso debe especificarse con barras diagonales inversas o el vínculo no invocará el archivo ejecutable. La adición de un token %SID% después de la ruta de acceso del archivo exe dará lugar a que la ejecución del vínculo sustituye la cadena de SID por el usuario para el que se está viendo actualmente la página central. A continuación, el ejecutable puede usar la cadena SID para administrar la funcionalidad del usuario especificado.

La desinstalación de aplicaciones debe quitar un registro de vínculo de extensibilidad.

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a>Vínculo de extensibilidad web y notas de invalidación del filtro de contenido web

Al establecer la propiedad FilterID en el mismo GUID que un vínculo de extensibilidad de la interfaz de usuario registrada existente, el vínculo mostrado se promoverá desde un vínculo genérico en Otros Configuración al vínculo restricciones web exclusivo. Se trata de una configuración de todo el equipo, por lo que hará que el LSP de filtro de contenido web de cuadro omita todo el filtrado para todos los usuarios controlados. También se debe establecer un nombre descriptivo en la propiedad FilterName, que se especifica mediante una ruta de acceso a la DLL y el identificador del recurso.

El sistema de controles parentales recomienda lo siguiente desde cualquier filtro web de reemplazo:

-   Respetar el estado general de encendido y apagado de los controles parentales de un usuario.
-   Respetar la Informe de actividades configuración de un usuario.
-   Supervise la propiedad FilterID. Si cambia desde el GUID especificado del proveedor, otro filtro ha tomado posesión y el filtro del proveedor debe deshabilitarse a sí mismo. Se ha agregado una interfaz COM para reducir la sobrecarga de comprobar periódicamente este cambio frente a una llamada WMI.
-   Se recomienda encarecidamente respetar las entradas de la aplicación HTTP de solo lectura y de lectura/escritura y la lista de exención de dirección URL.
-   Se recomienda respetar la lista de invalidaciones de direcciones URL por usuario (lista de permitidos o bloqueados).
-   Ser sólido para que los usuarios cambien rápidamente.

Los controles parentales no aplican ninguna limitación en el modo en que un filtro web u otro filtro de contenido se conecta a Windows para implementar el filtrado. Los proveedores pueden aprovechar sus inversiones actuales o tecnologías preferidas (LSP, TDI, otros).

La desinstalación del filtro del proveedor debe anular el registro de las entradas FilterID y FilterName. Esto se realiza estableciendo FilterID en \_ GUID NULL y FilterName en una variante null. A continuación, se volverá a habilitar el filtro de contenido web de la caja.

Tenga en cuenta que al volver a habilitar el filtro web en el cuadro solo se filtrarán las sesiones nuevas y no las sesiones activas desde antes del cambio.

## <a name="web-content-filter-allowblock-list-exportimport-format"></a>Formato de importación/exportación de lista de bloqueo/permitir filtro de contenido web

Esta característica no se admite en Windows 8.

**Windows 7 y Windows Vista:** Se admite esta característica.

&lt;WebAddresses&gt;

<URL AllowBlock="1">https://alloweddomain.com/&lt;/URL&gt;

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html&lt;/URL&gt;

<URL AllowBlock="2">https://blockeddomain.com/&lt;/URL&gt;

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html&lt;/URL&gt;

&lt;/WebAddresses&gt;

## <a name="application-restrictions-override-notes"></a>Notas de invalidación de restricciones de aplicación

Las invalidaciones de restricciones de aplicación se establecen por usuario para permitir archivos binarios o rutas de acceso específicas. Si se configura un nuevo usuario controlado parentalmente y se necesitan invalidaciones de restricciones de aplicación para ese usuario, se recomienda usar la clave de ejecución de Windows en el Registro con una aplicación pequeña marcada como que requiere la elevación implementada para escribir las invalidaciones. Esto dará como resultado una solicitud de credenciales única para configurar las invalidaciones para el usuario, después de lo cual los archivos binarios de destino para las invalidaciones no serán un problema para los usuarios debido a más solicitudes de invalidación de administrador.

## <a name="actions-required-for-settings-changes-to-become-effective"></a>Acciones necesarias para que Configuración cambios sean efectivos

Si un administrador cambia la configuración de un usuario estándar que ha iniciado sesión, se genera un mensaje de advertencia. Indica que los cambios de configuración pueden no tener efecto hasta que el usuario controlado cierra sesión y vuelve a intentarlo. Se trata de un diseño conservador. La mayoría de las configuraciones tendrán efecto casi inmediatamente mientras el usuario controlado haya iniciado sesión. Una excepción es para los juegos, donde la configuración se hará efectiva la próxima vez que se ejecute el Explorador de juegos o se invoje el juego.

## <a name="sample-code"></a>Código de ejemplo

En el SDK se proporcionan ejemplos de C++ que muestran el uso de las características de extensibilidad de configuración. Consulte la sección Ejemplos de controles parentales.

## <a name="independent-test-tools"></a>Herramientas de pruebas

La inspección de clases e instancias se facilita mediante el complemento Wmimgmt.msc y la herramienta Wbemtest.exe trabajo.

## <a name="64-bit-considerations"></a>Consideraciones de 64 bits

Actualmente, las Windows de sistema operativo de 64 bits tienen instalado un proveedor WMI de 32 bits y un proveedor de 64 bits.

## <a name="general-code-development-and-debugging"></a>Desarrollo y depuración de código general

Si Visual Studio para el desarrollo de código de administración de configuración, la depuración local requerirá ejecutar Visual Studio con derechos de administrador (invocar con ejecutar como administrador mediante la línea de comandos o la opción de clic con el botón derecho). Esto se debe al aislamiento de procesos y mensajes implementado por UAC.

## <a name="minimum-compliance-api-settings-read"></a>Lectura de la API Configuración cumplimiento mínimo

### <a name="interfaces-and-methods"></a>Interfaces y métodos

La API de cumplimiento controlada por el archivo de encabezado Wpcapi.h proporciona acceso simplificado de solo lectura a la siguiente configuración mediante interfaces COM.

Los métodos de interfaz raíz de [**IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) proporcionan acceso a:

-   Métodos IWPCSettings:
    -   IsLoggingRequired(): ¿los informes de actividad están configurados como para el usuario?
    -   GetLastSettingsChangeTime():la aplicación puede ser consciente de si alguna directiva de configuración ha cambiado desde una comprobación anterior.
    -   GetRestrictions(): lea si las restricciones web, los límites de tiempo, las restricciones de juegos o las restricciones de aplicación están establecidos en on.
-   Métodos de IWPCWebSettings:
    -   GetSettings(): recupera marcas para filtrar o desactivar y las descargas se bloquean.
    -   RequestURLOverride():escriba una solicitud en el mecanismo de invalidación de administrador (aprobación por encima del aprobación) que presentará un cuadro de diálogo que contiene las direcciones URL que se van a aprobar.
-   Métodos IWPCGamesSettings:
    -   IsBlocked(): para un identificador de aplicación de juego determinado, es el juego bloqueado por los controles parentales y por qué motivo.
-   GetVisibility(): proporciona información sobre si la interfaz de usuario de controles parentales está oculta actualmente.
-   GetWebFilterInfo(): proporciona una interfaz para obtener el identificador del filtro de contenido web actualmente activo.

### <a name="sample-code"></a>Código de ejemplo

En el SDK se proporcionan ejemplos de C++ que muestran el uso de la API de cumplimiento. Consulte la sección Ejemplos de controles parentales.

 

 



