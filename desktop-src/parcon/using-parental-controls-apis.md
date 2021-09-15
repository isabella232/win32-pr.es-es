---
description: Uso de las API de controles parentales
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Uso de las API de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574689"
---
# <a name="using-parental-controls-apis"></a>Uso de las API de controles parentales

## <a name="api-selection"></a>Selección de API

Como se indicó en la sección de información general, el desarrollo implica el uso de hasta tres API:

-   Acceso a la configuración básica: la API COM de cumplimiento mínimo de los controles parentales (API de cumplimiento) definida en Wpcapi.h para un acceso sencillo a un subconjunto clave del estado de los controles parentales.
-   Acceso de lectura/escritura de configuración completa: el uso de un pequeño subconjunto de la API COM de WMI para el acceso completo solo es necesario si el ISV necesita modificar la configuración. La adición de un vínculo de extensibilidad de la interfaz de usuario, el reemplazo del filtro de contenido web o las adiciones a la aplicación HTTP de todo el equipo o las listas de exención de filtrado de direcciones URL son los motivos principales para usar la API. Como el uso del espacio de nombres Controles parentales wmi proporciona acceso sin procesar al almacén de configuración subyacente, los ISV deben continuar con precaución al interpretar el estado de una configuración individual que, de hecho, puede tener dependencias de acceso en otras configuraciones. Por lo tanto, se recomienda usar la API de cumplimiento para leer el estado de todos los valores expuestos por esa API.
-   Registro: la API del sistema de informes y seguimiento de eventos de Windows Vista (también denominada ETW) para publicar eventos de actividad en los registros de controles parentales, junto con descriptores de eventos y enumeraciones de matrices definidas en WpcEvent.h.

Todas las API se pueden llamar como un usuario estándar. Para el registro, cualquier usuario puede producir eventos de registro de origen. Se producirá un error al llamar a para recuperar o cambiar la configuración de otro usuario si el autor de la llamada no tiene privilegios de administrador. En otras palabras, un usuario estándar solo puede acceder a su propia configuración y solo para lectura.

Configuración uso de la API de registro y registro se analizan más adelante en estas secciones:

-   [Uso de controles parentales Configuración API](using-parental-controls-settings-apis.md)
-   [Uso de las API de registro para los controles parentales](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a>Entorno de desarrollo

El desarrollo para controles parentales requiere acceso a tres archivos de encabezado: Wpc.h, WpcApi.h y WpcEvent.h. Wpc.h es un recopilador que incluye la API de cumplimiento público de configuración y los encabezados de evento, por lo que es suficiente incluir Wpc.h en el código de la aplicación.

El archivo Wpcsprov.mof especifica los permisos de lectura y escritura para la API wmi. Este archivo se instala en el subdirectorio WBEM en el directorio Windows System32.

El Kit de desarrollo de software (SDK) de Microsoft Windows contiene código de ejemplo para reforzar el código de ejemplo que se muestra aquí y proporcionar herramientas sencillas controladas por la línea de comandos para la exploración de API o las pruebas de integración.

 

 



