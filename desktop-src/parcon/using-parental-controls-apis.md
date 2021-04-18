---
description: Uso de las API de controles parentales
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Uso de las API de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720523"
---
# <a name="using-parental-controls-apis"></a>Uso de las API de controles parentales

## <a name="api-selection"></a>Selección de API

Como se indicó en la sección de información general, el desarrollo implica el uso de hasta tres API:

-   Acceso de configuración básica: la API COM de cumplimiento mínimo de control parental (API de cumplimiento) definida en Wpcapi. h para el acceso sencillo a un subconjunto clave de estado de controles parentales.
-   Acceso completo de lectura y escritura: el uso de un pequeño subconjunto de la API COM de WMI para el acceso completo solo es necesario si el ISV necesita modificar la configuración. La adición de un vínculo de extensibilidad de la interfaz de usuario, el reemplazo del filtro de contenido web o las adiciones a las listas de exención de filtrado de URL o aplicación HTTP para todo el equipo son los motivos principalmente para usar la API. Como el uso del espacio de nombres de controles parentales de WMI proporciona acceso sin formato al almacén de configuración subyacente, los ISV deben proseguir con precaución al interpretar el estado de los valores de configuración individuales que, de hecho, pueden tener dependencias en otras opciones de configuración. Por lo tanto, se recomienda usar la API de cumplimiento para leer el estado de todos los valores expuestos por esa API.
-   Registro: la API del sistema de informes y seguimiento de eventos de Windows Vista (también denominada ETW) para publicar eventos de actividad en los registros de control parental, junto con los descriptores de eventos y las enumeraciones de matriz definidos en WpcEvent. h.

Todas las API se pueden llamar como un usuario estándar. Para el registro, cualquier usuario puede registrar eventos de registro. Si se llama a para recuperar o cambiar la configuración de otro usuario, se producirá un error si el autor de la llamada no tiene privilegios de administrador. En otras palabras, un usuario estándar solo puede tener acceso a su propia configuración y solo para lectura.

La configuración y el uso de la API de registro se describen con más detalle en estas secciones:

-   [Uso de las API de configuración de controles parentales](using-parental-controls-settings-apis.md)
-   [Uso de las API de registro para controles parentales](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a>Entorno de desarrollo

El desarrollo de controles parentales requiere acceso a tres archivos de encabezado: WPC. h, WpcApi. h y WpcEvent. h. WPC. h es un recopilador que incluye la configuración Public Compliance API y los encabezados de evento, por lo que es suficiente incluir WPC. h en el código de la aplicación.

El archivo Wpcsprov. mof especifica los permisos de lectura y escritura para la API de WMI. Este archivo se instala en el subdirectorio WBEM en el directorio system32 de Windows.

El kit de desarrollo de software (SDK) de Microsoft Windows contiene código de ejemplo para reforzar el código de ejemplo que se muestra aquí y proporcionar herramientas orientadas a la línea de comandos simples para la exploración de API o las pruebas de integración.

 

 



