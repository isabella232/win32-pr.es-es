---
description: Se proporcionan varias implementaciones de restricciones.
ms.assetid: a00d9a3a-d052-492c-b9e7-3ecb1455a392
title: Controles parentales In-Box restricciones & interfaces de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5f155f8323fd6b006e510d75865ea25e278c70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688580"
---
# <a name="parental-controls-in-box-restrictions--user-interfaces"></a>Controles parentales In-Box restricciones & interfaces de usuario

Se proporcionan varias implementaciones de restricciones.

-   [Restricciones Web](#web-restrictions)
-   [Límites de tiempo](#time-limits)
-   [Juegos](#games)
-   [Permitir y bloquear programas específicos](#allow-and-block-specific-programs)

## <a name="web-restrictions"></a>Restricciones Web

-   Filtro de contenido web integrado con un servicio de clasificación dinámico gratuito. Configurable individualmente por usuario controlado.
-   Filtra todo el tráfico HTTP cuando está habilitado, devuelve una página con formato personalizado si está bloqueada. Permite una funcionalidad aceptable con todos los exploradores principales. Mediante la supervisión de todas las solicitudes HTTP GET y post de una página, permite bloquear elementos de página web individuales.
-   Es muy configurable mediante el uso de la interfaz de usuario que permite o bloquea listas de direcciones URL, valores predeterminados de categoría de clasificación simplificada o control ActiveX de 12 categorías, así como una directiva para bloquear descargas de archivos.

> [!Note]  
> El bloqueo real de descarga de archivos requiere que las aplicaciones implementen la restricción, de acuerdo con la configuración proporcionada.

 

-   Se implementa como un controlador de plataforma de filtrado de Windows (WFP) que se comunica con el proceso de supervisión de seguridad de la familia que se ejecuta en las sesiones de los usuarios. La implementación ha cambiado de un filtro de proveedor de servicios por capas (LSP) a un controlador de plataforma de filtrado de Windows (WFP) que se comunica con el proceso de supervisión de seguridad de la familia que se ejecuta en las sesiones de los usuarios.

    **Windows 7 y Windows Vista:** Se implementa como un filtro de proveedor de servicios por capas (LSP) que se comunica con un servicio de derechos reducidos para la administración y supervisión generales. El filtro permanece en la cadena de LSP cuando está deshabilitado, pero pasa todo el tráfico a través de. Esta implementación solo es compatible con los sistemas operativos enumerados.

-   Las aplicaciones pueden proporcionar una interfaz de usuario para mostrar el bloqueo parcial de páginas y respetar la Directiva para bloquear las descargas de archivos. También pueden invocar una API para permitir que el usuario solicite permiso para ver una página bloqueada. Esta invalidación administrativa invoca una pequeña aplicación que muestra las direcciones URL intentadas y que solicita las credenciales para permitirlos.
-   Se proporciona una API para casos especiales en los que una aplicación necesita registrarse para omitir el filtrado o siempre se permitirán direcciones URL específicas.
-   Dado que solo debe ejecutarse un filtro de contenido web a la vez, es posible que terceras partes se registren como filtro activo y deshabiliten el filtro en la caja. Esta extensibilidad, junto con la capacidad de mostrar un filtro de terceros en la interfaz de usuario, permite un reemplazo sencillo. Los filtros deben quitar su registro cuando se desinstalen.

## <a name="time-limits"></a>Límites de tiempo

-   Las restricciones de tiempo integradas se han mejorado ofreciendo la posibilidad de controlar la cantidad total de tiempo por día que se puede usar (asignación de tiempo), además de la capacidad de controlar los tiempos en que se puede usar el equipo (Curfew), que estaba disponible en versiones anteriores de Windows.
-   La interfaz de usuario de Curfew permite el control independiente para cada día de la semana con granularidad de media hora
-   La interfaz de usuario para el tiempo permitido permite controles para los días laborables y fines de semana, o control independiente para cada día de la semana con una granularidad de 15 minutos.
-   El mecanismo de cambio rápido de usuario (FUS) ya no se usa para bloquear o bloquear el inicio de sesión del usuario controlado en un período de tiempo bloqueado. Para estos propósitos, se usa un conmutador a un escritorio independiente. Tenga en cuenta que el FUS conserva el estado del usuario cuando se bloquea.

## <a name="games"></a>Juegos

-   Funciona junto con el explorador de juegos.
-   Permite a los administradores controlar qué juegos pueden reproducirse a través de una interfaz de usuario enriquecida para seleccionar un nivel y sistema de clasificación de juegos (más descriptores si están presentes) y/o mediante la autorización o el bloqueo específicos de los títulos.
-   Los metadatos de las clasificaciones de juegos se obtienen de una de estas dos maneras:
    -   Los títulos admitidos implementan sus propios archivos de definición de juego (GDFs).
    -   En una base de datos incluida, se incluyen aproximadamente 2000 títulos heredados.
-   Se usan tres mecanismos para la aplicación:
    -   Denegar ACL para el acceso de escritura de usuario controlado a la carpeta Game.
    -   Terminación de procesos para títulos heredados mediante la tecnología de corrección de compatibilidad de aplicaciones.
    -   Uso automático de la API mediante títulos compatibles para bloquear la ejecución.
-   Se recomienda el reconocimiento de los eventos de límites de tiempo descritos en la sección anterior.
-   La documentación de GDFs y el explorador de juegos se proporcionarán principalmente a través de las versiones del SDK de DirectX.

## <a name="allow-and-block-specific-programs"></a>Permitir y bloquear programas específicos

-   También se conoce como restricciones de aplicación generales (GAR).
-   Desactivado de forma predeterminada. Si está activada, solo permite a un usuario controlado ejecutar aplicaciones aprobadas por un administrador, con excepciones razonables.
-   La interfaz de usuario proporciona una lista de nombres de programa con las rutas de acceso correspondientes, cada una con una casilla permitir. También se proporciona un botón examinar.
-   Se implementa mediante el uso de directivas de restricción de software (SRP), también conocido como más seguro:
    -   Impide la ejecución de todos los medios (claves USB, disquetes, etc.).
    -   Usa reglas de ruta de acceso para especificar los programas que se pueden ejecutar.
    -   Los permisos de escritura de la ACL de NTFS se revocan de cualquier elemento permitido para que el usuario controlado se ejecute.
    -   Si se bloquea y posteriormente se invalida para permitir, la aplicación debe reiniciarse manualmente.
-   Entre las excepciones se incluyen:
    -   Todos los archivos binarios necesarios para que funcione un subconjunto básico de Windows.
    -   Todos los archivos ejecutables que se registran mediante una API se permiten para un usuario determinado.
    -   Juegos especificados como permitidos en restricciones de juegos.
-   Tenga en cuenta que el comando runas está bloqueado por el diseño de un usuario cuando GAR está activado.

 

 



