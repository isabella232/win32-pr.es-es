---
description: Uso de las API de configuración de controles parentales
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: Uso de las API de configuración de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dde4827dfe3ed5ee7eec6787744e6ff92f18775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815363"
---
# <a name="using-parental-controls-settings-apis"></a>Uso de las API de configuración de controles parentales

La configuración se trata con anterioridad al registro porque el registro es condicional en la configuración del usuario.

## <a name="wmi-api-settings-writeread"></a>Escritura/lectura de la configuración de la API de WMI

La API de WMI proporciona acceso no abstracto (sin formato) a todas las opciones de configuración creadas por la infraestructura de controles parentales, tal como se define en el archivo de esquema Wpcsprov. mof. El almacén de configuración existe en \\ el \\ espacio de nombres WindowsParentalControls de aplicaciones de cimv2 raíz \\ \\ , con las siguientes definiciones de clase que definen un esquema. Se indican los elementos de extensibilidad.

Por equipo:

-   WpcSystemSettings (una instancia)
    -   Los métodos AddUser () y RemoveUser () para crear y eliminar la configuración de controles parentales para un SID determinado, respectivamente.
    -   Propiedades del sistema actual de clasificación de juegos en vigor y seguimiento y notificación relacionados con la comprobación de administración de registros.
    -   Extensibilidad: propiedades de la aplicación HTTP de solo lectura y de lectura/escritura y las listas de exenciones de dirección URL para el filtrado de contenido Web, el filtro de contenido web invalida el identificador y la ruta de acceso y el identificador del archivo DLL de recurso de nombre, y el registro de campos y el registro de nombres de encabezado.
-   WpcRatingsSystem (una instancia por cada sistema de clasificación instalado)
    -   WpcRating (una instancia por nivel de clasificación).
    -   WpcRatingDescriptor (una instancia por cada descriptor de clasificación).
-   Extensibilidad: WpcExtension (se ha agregado una instancia por cada vínculo de extensibilidad del panel de controles parentales).
    -   Propiedades de GUID, subsistema, identificador, ruta de acceso del recurso de imagen, ruta de acceso del recurso de imagen de estado deshabilitada, ruta de acceso de archivo, nombre para mostrar ruta de acceso e ID. de dll de recurso de subtítulo y identificador.

Usuario controlado:

-   WpcUserSettings (una instancia por usuario controlado)
    -   Propiedades para el indicador de SID de propiedad, marca de activación/desactivación, marca de inicio/desactivación, límite de tiempo activado/desactivado, marca de invalidaciones habilitadas, máscara de horas de inicio de sesión y restricciones de aplicaciones generales en la marca/desactivación.
    -   En Windows 8, la propiedad existente representa la primera media hora de cada hora. Se ha agregado una nueva propiedad de media hour para representar la segunda mitad de cada hora. Se presentó una nueva propiedad adicional para representar la asignación de tiempo diaria.

        **Windows 7 y Windows Vista:** Las restricciones de temporizador admiten la granularidad de 1 hora.

-   WpcWebSettings (una instancia por usuario controlado)
    -   Propiedades para el SID de propiedad, marca de filtrado de activado/desactivado, nivel de filtro, marca de descargas bloqueadas de archivo, marca de sitios sin clasificación bloqueados.
-   WpcUrlOverride (una instancia por dirección URL permitida o denegada explícitamente en la lista de invalidamientos de direcciones URL usada como permitir o bloquear la lista para el filtrado de contenido web)
    -   Propiedades para el estado SID, URL afectada, permitido o bloqueado.
-   WpcAppOverride (una instancia por ruta de acceso permitida explícitamente en la lista de invalidaciones de aplicación de restricciones de aplicaciones generales)
    -   Propiedades para el SID de propiedad. IDENTIFICADOR de regla más seguro, ruta de acceso a la aplicación.
-   WpcGamesSettings (una instancia por usuario controlado)
    -   Propiedades del SID propietario, marca de juegos permitidos, GUID del sistema de clasificación para esta configuración, permitir marca de juegos sin clasificación, ID. de la clasificación máxima permitida en el sistema actual, colección de descriptores denegados.
-   WpcGameOverride (una instancia por cada identificador de aplicación permitida o denegada explícitamente)
    -   Propiedades de SID propietario, juego de identificación de identificador de aplicación, estado permitido o denegado.

## <a name="data-representation-notes"></a>Notas de representación de datos

Algunas de las opciones del esquema están restringidas por el archivo. mof con un atributo que no \_ es NULL. No se pueden establecer en una variante nula. En el caso de todos los tipos que no son de matriz, el código de controles parentales inicializa valores. En el caso de las matrices, los Estados vacíos se pueden escribir con una variante nula, una variante vacía o una matriz de variantes de tamaño cero. El proveedor WMI normalizará todos estos valores en una representación de estado variante nula en la lectura.

## <a name="user-interface-extensibility-link-notes"></a>Notas del vínculo de extensibilidad de la interfaz de usuario

El uso de WMI para registrar un vínculo de extensibilidad de la interfaz de usuario requiere la especificación de la siguiente información:

-   GUID: varios vínculos pueden compartir el mismo GUID si forman parte de un paquete o conjunto común.
-   Subsistema: diseñado para indicar las clasificaciones de tipos de vínculo, como conjuntos o aplicaciones compatibles independientes
-   Nombre y ruta de acceso de la DLL del recurso Name: especifica el recurso para el nombre para mostrar que se mostrará para el vínculo.
-   IDENTIFICADOR y ruta de acceso del archivo DLL de recursos de subtítulos: especifica el recurso para texto adicional debajo del nombre.
-   Ruta de acceso de la imagen: ruta de acceso completa de un mapa de bits de 24 x 24 píxeles (BMP), con una profundidad de color de 8 bits por píxel y, preferiblemente, un canal alfa. Esto se especifica de manera coherente con las extensiones de Shell: <file system path> , <negative resource ID> . Por ejemplo: C: \\ Windows \\ system32 \\Wpccpl.dll,-20.
-   Ruta de acceso de imagen deshabilitada: igual que la ruta de acceso de la imagen anterior, excepto la variante del mapa de bits que muestra el estado Esta imagen se muestra cuando el control parental está desactivado.
-   Ruta de acceso de exe: ruta de acceso completa a un archivo ejecutable que se va a invocar mediante ShellExecute (). Esta ruta de acceso se debe especificar con barras diagonales inversas o el vínculo no invocará el archivo ejecutable. La adición de un token% SID% después de la ruta de acceso del archivo exe dará como resultado la ejecución del vínculo que sustituye a la cadena SID del usuario para el que se está viendo la página del concentrador. Después, el ejecutable puede usar la cadena SID para administrar la funcionalidad del usuario especificado.

La desinstalación de la aplicación debe quitar un registro de vínculo de extensibilidad.

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a>Notas sobre el vínculo de extensibilidad web y el filtro de contenido web

Al establecer la propiedad FilterID en el mismo GUID que un vínculo de extensibilidad de la interfaz de usuario registrado existente, el vínculo mostrado se promoverá de un vínculo genérico en otros valores al vínculo restricciones web exclusivas. Se trata de una configuración de todo el equipo, por lo que el LSP del filtro de contenido web integrado omitirá todos los filtros de todos los usuarios controlados. También se debe establecer un nombre descriptivo en la propiedad FilterName, que se especifica mediante una ruta de acceso a la DLL de recursos y el identificador.

El sistema de controles parentales recomienda lo siguiente desde cualquier filtro Web de invalidación:

-   Respetar el estado general de activar y desactivar controles parentales para un usuario.
-   Respetar la configuración de informes de actividad de un usuario.
-   Supervise la propiedad FilterID. Si cambia desde el GUID especificado del proveedor, otro filtro ha tomado posesión y el filtro del proveedor debe deshabilitarse. Se ha agregado una interfaz COM para reducir la sobrecarga de comprobar periódicamente este cambio frente a una llamada WMI.
-   Se recomienda encarecidamente que respete las entradas de la lista de exclusión de URL y la aplicación HTTP de solo lectura y de lectura/escritura.
-   Se recomienda respetar la lista de invalidaciones de direcciones URL por usuario (lista de permitidos o bloqueados).
-   Sea robusto para el cambio rápido de usuario.

Los controles parentales no imponen ninguna limitación sobre cómo se conecta un filtro de contenido o Web a Windows para implementar el filtrado. Los proveedores pueden aprovechar sus inversiones actuales o tecnologías preferidas (LSP, TDI, otras).

La desinstalación del filtro del proveedor debe anular el registro de las entradas FilterID y FilterName. Esto se realiza estableciendo FilterID en GUID \_ null y filtername en una variante null. Se volverá a habilitar el filtro de contenido web en la caja.

Tenga en cuenta que al volver a habilitar el filtro Web integrado solo se filtrarán las sesiones nuevas y no las sesiones activas desde antes del cambio.

## <a name="web-content-filter-allowblock-list-exportimport-format"></a>Filtro de contenido web-formato de exportación/importación de lista de bloqueo

Esta característica no se admite en Windows 8.

**Windows 7 y Windows Vista:** Esta característica es compatible.

<WebAddresses>

<URL AllowBlock="1">https://alloweddomain.com/</URL>

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html</URL>

<URL AllowBlock="2">https://blockeddomain.com/</URL>

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html</URL>

</WebAddresses>

## <a name="application-restrictions-override-notes"></a>Notas de invalidación de restricciones de aplicación

Las invalidaciones de restricciones de aplicación se establecen en función de cada usuario para permitir rutas de acceso o archivos binarios específicos. Si se configura un nuevo usuario controlado con control parental y se necesitan invalidaciones de restricciones de aplicación para ese usuario, se recomienda usar la clave de ejecución de Windows en el registro con una aplicación pequeña marcada como que requiere elevación implementada para escribir las invalidaciones. Esto producirá una solicitud de credenciales de un solo tiempo para configurar las invalidaciones del usuario, después de las cuales los archivos binarios de destino para las invalidaciones no serán molestas para los usuarios debido a mensajes de invalidación de administrador adicionales.

## <a name="actions-required-for-settings-changes-to-become-effective"></a>Acciones necesarias para que los cambios de configuración surtan efecto

Si un administrador cambia la configuración de un usuario estándar que ha iniciado sesión, se genera un mensaje de advertencia. Indica que es posible que los cambios de configuración no surtan efecto hasta que el usuario controlado cierre la sesión y vuelva a intentarlo. Se trata de un diseño conservador. La mayoría de las opciones de configuración se aplicarán casi inmediatamente mientras el usuario controlado haya iniciado sesión. Una excepción es para juegos, donde la configuración surtirá efecto la próxima vez que se ejecute el explorador de juegos o se intente invocar el juego.

## <a name="sample-code"></a>Código de ejemplo

En el SDK se proporcionan ejemplos de C++ que muestran el uso de las características de extensibilidad de configuración. Consulte la sección ejemplos de controles parentales.

## <a name="independent-test-tools"></a>Herramientas de pruebas independientes

El complemento Wmimgmt. msc y la herramienta Wbemtest.exe facilitan la inspección de clases e instancias.

## <a name="64-bit-considerations"></a>Consideraciones de 64 bits

las versiones de sistema operativo Windows de 64 bits tienen actualmente un proveedor WMI de 32 bits y un proveedor de 64 bits instalado.

## <a name="general-code-development-and-debugging"></a>Desarrollo y depuración de código generales

Si se usa Visual Studio para el desarrollo de código de administración de configuración, la depuración local requerirá la ejecución de Visual Studio con derechos de administrador (al invocar con ejecutar como administrador mediante la línea de comandos o la opción de hacer clic con el botón derecho). Esto se debe al aislamiento de procesos y mensajes implementado por UAC.

## <a name="minimum-compliance-api-settings-read"></a>Configuración de API de cumplimiento mínima leída

### <a name="interfaces-and-methods"></a>Interfaces y métodos

La API de cumplimiento controlada por el archivo de encabezado Wpcapi. h proporciona acceso de solo lectura simplificado a las siguientes configuraciones mediante el uso de interfaces COM.

Los métodos de interfaz raíz [**IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) proporcionan acceso a:

-   Métodos IWPCSettings:
    -   IsLoggingRequired (): ¿los informes de actividad se configuran como on para el usuario?
    -   GetLastSettingsChangeTime (): la aplicación puede ser consciente de que las directivas de configuración han cambiado desde una comprobación anterior.
    -   GetRestrictions (): leer si las restricciones Web, los límites de tiempo, las restricciones de juego o las restricciones de la aplicación se establecen en on.
-   Métodos IWPCWebSettings:
    -   GetSettings (): recupera marcas para el filtro activado o desactivado y descargas bloqueadas.
    -   RequestURLOverride (): escriba una solicitud en el mecanismo de invalidación del administrador (aprobación por encima del hombro) que presentará un cuadro de diálogo que contiene las direcciones URL que se van a aprobar.
-   Métodos IWPCGamesSettings:
    -   IsBlocked (): para un identificador de aplicación de juego determinado, es el juego bloqueado por controles parentales y por qué motivo.
-   GetVisibility (): proporciona información sobre si la interfaz de usuario de controles parentales está oculta actualmente.
-   GetWebFilterInfo (): proporciona una interfaz para obtener el identificador del filtro de contenido Web activo actualmente.

### <a name="sample-code"></a>Código de ejemplo

En el SDK se proporcionan ejemplos de C++ que muestran el uso de la API de cumplimiento. Consulte la sección ejemplos de controles parentales.

 

 



