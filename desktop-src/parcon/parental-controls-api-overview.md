---
description: Información general sobre la API de controles parentales
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Información general sobre la API de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0aa88592f2262b89f98cfd5baaac5ad2f35f959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716999"
---
# <a name="parental-controls-api-overview"></a>Información general sobre la API de controles parentales

Las API que se usan para controles parentales exponen la Directiva y las restricciones en el cuadro y la funcionalidad de registro.

## <a name="settings"></a>Configuración

Se proporcionan dos API públicas:

-   Una API de cumplimiento mínimo basada en COM (denominada API de cumplimiento) principalmente para las aplicaciones para determinar si se debe activar el registro. Además, se proporcionan métodos simples para:
    -   Recuperación del estado de restricciones para restricciones Web, límites de tiempo, restricciones de juegos y restricciones de aplicación.
    -   Recuperando el identificador del filtro de contenido Web activo.
    -   Determinar si se deben mostrar los elementos de la interfaz de usuario del proveedor, de manera coherente con la ocultación en el cuadro cuando se une a un dominio.
    -   Recuperar la última vez que se ha cambiado un valor de configuración para un usuario.
    -   Recuperación de si se debe bloquear la descarga de archivos basados en el explorador o en el explorador para un usuario, así como la capacidad de solicitar una dirección URL que permita específicamente el filtro de contenido web para ese usuario.
    -   Determinar si un juego determinado está bloqueado para un usuario.
-   Acceso de API de Instrumental de administración de Windows (WMI) a un espacio de nombres de controles parentales para el acceso de lectura y escritura completo a todos los valores expuestos. El control parental implementa un proveedor de WMI para administrar los permisos de lectura y escritura en el almacén de configuración subyacente con el cumplimiento adecuado de los privilegios para administradores y usuarios controlados.

Se solicita a los ISV que usen la API de cumplimiento y la API de WMI según sea necesario para controlar las restricciones según sea necesario para la seguridad secundaria basada en la funcionalidad de la aplicación o la solución.

## <a name="logging"></a>Registro

-   Las API de consumo y publicación de eventos estándar de Windows se usan para la supervisión de la actividad de controles parentales. El sistema de informes y seguimiento de eventos de Windows Vista ha mejorado el rendimiento respecto a la funcionalidad anterior de seguimiento de eventos para Windows (ETW). Controles parentales define un canal único para sus datos en ETW.
-   Se solicita a los ISV que usen la API de publicación de eventos para registrar la actividad de los usuarios según se especifica en la sección uso de las API de controles parentales.

 

 



