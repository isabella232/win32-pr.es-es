---
description: Información general sobre la API de controles parentales
ms.assetid: 647e5df8-7c6d-466a-a3d4-eac13efa797d
title: Información general sobre la API de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2dc1995db834aa206dea1a4f657565ac3e38b35766ca6a83ac495c4f1734af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712585"
---
# <a name="parental-controls-api-overview"></a>Información general sobre la API de controles parentales

Las API que se usan para los controles parentales exponen la configuración de restricciones de directivas y en el cuadro, y la funcionalidad de registro.

## <a name="settings"></a>Configuración

Se proporcionan dos API públicas:

-   Una API de cumplimiento mínimo ligera basada en COM (denominada API de cumplimiento) principalmente para que las aplicaciones determinen si el registro debe estar activado. Además, se proporcionan métodos sencillos para:
    -   Recuperar el estado de restricciones para restricciones web, límites de tiempo, restricciones de juegos y restricciones de aplicaciones.
    -   Recuperación del identificador del filtro de contenido web activo.
    -   Determinar si se deben mostrar los elementos de la interfaz de usuario del proveedor, de forma coherente con la ocultación integrada cuando se une a un dominio.
    -   Recuperación de la última vez que se ha cambiado una configuración para un usuario.
    -   Recuperar si las descargas de archivos basadas en explorador o de tipo explorador deben bloquearse para un usuario y la capacidad de solicitar que el filtro de contenido web permita específicamente una dirección URL para ese usuario.
    -   Determinar si un juego determinado está bloqueado para un usuario.
-   Windows Acceso de API de Instrumental de administración (WMI) a un espacio de nombres de controles parentales para el acceso de lectura y escritura completo a todas las configuraciones expuestas. Los controles parentales implementan un proveedor WMI para administrar los permisos de lectura y escritura en el almacén de configuración subyacente con el cumplimiento adecuado de los privilegios para administradores y usuarios controlados.

Se solicita a los ISV que usen la API de cumplimiento y la API wmi según sea necesario para controlar las restricciones según corresponda para la seguridad secundaria en función de la funcionalidad de la aplicación o la solución.

## <a name="logging"></a>Registro

-   Windows api estándar de publicación y consumo de eventos se usan para la supervisión de la actividad de los controles parentales. El Windows de seguimiento y generación de informes de eventos de Vista ha mejorado el rendimiento con respecto al anterior seguimiento de eventos Windows funcionalidad de Windows (ETW). Los controles parentales definen un canal único para sus datos en ETW.
-   Se solicita a los ISV que usen la API de publicación de eventos para registrar la actividad del usuario como se especifica en la sección Uso de las API de controles parentales.

 

 



