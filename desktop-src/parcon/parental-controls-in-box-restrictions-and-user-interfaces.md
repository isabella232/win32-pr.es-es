---
description: Se proporcionan varias implementaciones de restricciones.
ms.assetid: a00d9a3a-d052-492c-b9e7-3ecb1455a392
title: Restricciones de In-Box parentales & interfaces de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9cb430a05d6e23b5ffa736398d30197aaec1dbbcdf6d1610ec8bc2db50d6556
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846654"
---
# <a name="parental-controls-in-box-restrictions--user-interfaces"></a>Restricciones de In-Box parentales & interfaces de usuario

Se proporcionan varias implementaciones de restricciones.

-   [Restricciones web](#web-restrictions)
-   [Límites de tiempo](#time-limits)
-   [Juegos](#games)
-   [Permitir y bloquear programas específicos](#allow-and-block-specific-programs)

## <a name="web-restrictions"></a>Restricciones web

-   Filtro de contenido web en cuadro mediante un servicio de clasificación dinámica gratuito. Configurable individualmente por usuario controlado.
-   Filtra todo el tráfico HTTP cuando está habilitado y devuelve una página con formato personalizado si está bloqueada. Permite una funcionalidad aceptable con todos los exploradores principales. Al supervisar todas las solicitudes HTTP Get y Post de una página, permite bloquear partes de páginas web individuales.
-   Altamente configurable mediante la interfaz de usuario que permite o bloquea listas de direcciones URL, valores preestablecidos de categoría de clasificación simplificado ActiveX s o un control de más de 12 categorías, así como una directiva para bloquear las descargas de archivos.

> [!Note]  
> El bloqueo real de la descarga de archivos requiere que las aplicaciones implementen la restricción, de acuerdo con la configuración proporcionada.

 

-   Se implementa como un controlador Windows Filtering Platform (WFP) que se comunica con el proceso de supervisión de seguridad familiar que se ejecuta en las sesiones de los usuarios. La implementación ha cambiado de un filtro de proveedor de servicios por capas (LSP) a un controlador de Windows Filtering Platform (WFP) que se comunica con el proceso de supervisión de seguridad familiar que se ejecuta en las sesiones de los usuarios.

    **Windows 7 y Windows Vista:** Se implementa como un filtro de proveedor de servicios por capas (LSP) que se comunica con un servicio de derechos bajos para la administración y supervisión generales. El filtro permanece en la cadena LSP cuando está deshabilitado, pero pasa todo el tráfico a través de . Esta implementación solo se admite para los sistemas operativos enumerados.

-   Las aplicaciones pueden proporcionar una interfaz de usuario para mostrar el bloqueo parcial de páginas y respetar la directiva para bloquear las descargas de archivos. También pueden invocar una API para permitir que el usuario solicite permiso para ver una página bloqueada. Esta invalidación administrativa invoca una pequeña aplicación que muestra las direcciones URL intentadas y que solicita credenciales para permitirlas.
-   Se proporciona una API para casos especiales en los que una aplicación debe registrarse para omitir el filtrado, o se deben permitir direcciones URL específicas siempre.
-   Dado que solo debe ejecutarse un filtro de contenido web a la vez, los terceros pueden registrarse como filtro activo y deshabilitar el filtro de entrada. Esta extensibilidad, junto con la capacidad de mostrar un filtro de terceros en la interfaz de usuario, permite un reemplazo simple. Los filtros deben quitar su registro cuando se desinstalan.

## <a name="time-limits"></a>Límites de tiempo

-   Las restricciones de tiempo incluidas se mejoraron al proporcionar la capacidad de controlar la cantidad total de tiempo al día que se puede usar el equipo (asignación de tiempo), además de la capacidad de controlar las horas en las que se puede usar el equipo (toque de queda), que estaba disponible en versiones anteriores de Windows.
-   La interfaz de usuario para el toque de queda permite un control independiente para cada día de la semana con granularidad de media hora
-   La interfaz de usuario para la asignación de tiempo permite controles para días laborables y fines de semana o control independiente para cada día de la semana con granularidad de 15 minutos
-   El mecanismo de cambio rápido de usuario (FUS) ya no se usa para bloquear o bloquear el inicio de sesión del usuario controlado cuando se encuentra bloqueado. Para estos fines se usa un conmutador a un escritorio independiente. Tenga en cuenta que FUS conserva el estado del usuario cuando se bloquea.

## <a name="games"></a>Juegos

-   Funciona junto con El Explorador de juegos.
-   Permite a los administradores controlar qué juegos se pueden reproducir a través de una interfaz de usuario enriquez para seleccionar un sistema de clasificaciones de juegos y un nivel (más descriptores si están presentes) o permitiendo o bloqueando títulos específicamente.
-   Los metadatos de las clasificaciones de juegos se obtienen de una de estas dos maneras:
    -   Los títulos admitidos implementan sus propios archivos de definición de juego (GDF).
    -   Aproximadamente 2000 títulos heredados están cubiertos por una base de datos local.
-   Se usan tres mecanismos para la aplicación:
    -   Deniegue las ACL para el acceso de escritura de usuario controlado a la carpeta del juego.
    -   Procesar la terminación de los títulos heredados mediante la tecnología de compatibilidad de aplicaciones shim.
    -   Auto check API use by supported titles to block run (Uso de la API de autoprobado por los títulos admitidos para bloquear la ejecución).
-   Se recomienda conocer los eventos de límites de tiempo que se explican en la sección anterior.
-   La documentación de los GDF y el Explorador de juegos se proporciona principalmente a través de las versiones del SDK de DirectX.

## <a name="allow-and-block-specific-programs"></a>Permitir y bloquear programas específicos

-   También se conoce como Restricciones generales de aplicaciones (GAR).
-   Desactivado de forma predeterminada. Si está activado, solo permite a un usuario controlado ejecutar aplicaciones aprobadas por un administrador, con excepciones razonables.
-   La interfaz de usuario proporciona una lista de nombres de programa con las rutas de acceso correspondientes, cada una con una casilla permitir. También se proporciona un botón Examinar.
-   Se implementa mediante directivas de restricción de software (SRP), también conocidas como SAFER:
    -   Impide la ejecución desde todos los medios (claves USB, disquetes, entre otros).
    -   Usa reglas de ruta de acceso para especificar los programas que se pueden ejecutar.
    -   Los permisos de escritura de ACL ntfs se revocan de todo lo permitido para que el usuario controlado ejecute.
    -   Si se bloquea y se invalida posteriormente para permitir, la aplicación se debe volver a iniciar manualmente.
-   Entre las excepciones se incluyen:
    -   Todos los archivos binarios necesarios para que un subconjunto básico de Windows funcione.
    -   Todos los archivos ejecutables que se registren mediante una API se permitirán para un usuario determinado.
    -   Juegos especificados como permitidos en Restricciones de juegos.
-   Tenga en cuenta que el comando RunAs está bloqueado por diseño para un usuario cuando GAR está en.

 

 



