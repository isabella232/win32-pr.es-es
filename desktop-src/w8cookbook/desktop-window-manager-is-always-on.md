---
title: Administrador de ventanas de escritorio está siempre on
description: Administrador de ventanas de escritorio está siempre on
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f855635615dee734b9a719d4e51d3ead663d144e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575653"
---
# <a name="desktop-window-manager-is-always-on"></a>Administrador de ventanas de escritorio está siempre on

## <a name="platforms"></a>Plataformas

**Clientes:** Windows 8  
**Servidores:** Windows Server 2012  


## <a name="description"></a>Descripción

En Windows 8, Administrador de ventanas de escritorio (DWM) siempre está on y no pueden deshabilitarla los usuarios finales y las aplicaciones. Como en Windows 7, DWM se usa para crear el escritorio. Además de las experiencias habilitadas en Windows 7, ahora la composición de escritorio de DWM permite la composición de escritorio para todos los temas, la compatibilidad con 3D estereoscópico y la administración, separación y protección de la experiencia con aplicaciones de Windows Store.

**Composición de escritorio para todos los temas**

En Windows Vista y Windows 7, la composición de escritorio solo está habilitada con el tema glass de AERO. Por lo tanto, los usuarios de los temas clásicos y de contraste alto de Windows no pueden usar experiencias habilitadas por la composición de escritorio, como Windows Flip, escalado automático para el escalado de alta resolución (PPP), vista previa en miniatura y lupa de pantalla completa. Además, en estas versiones anteriores de Windows, los desarrolladores de aplicaciones deben escribir y mantener varias rutas de acceso de código: una donde está habilitada la composición de escritorio y otra donde la composición de escritorio está deshabilitada.

Con Windows 8, la composición de escritorio está habilitada para todos los temas. Los usuarios de los temas clásicos y de contraste alto de Windows pueden usar las experiencias habilitadas por la composición de escritorio, como Windows Flip, escalado automático para el escalado de alta resolución (PPP), vistas previas de miniaturas y lupa de pantalla completa. Además, los desarrolladores no necesitan escribir y mantener varias rutas de acceso de código, lo que simplifica el desarrollo.

**Compatibilidad con estereocopía 3D**

La composición de escritorio dwm admite la representación y presentación del contenido de la aplicación 3D estereomática de pantalla completa y en ventanas.

**Administración, separación y protección de la experiencia con Windows Store**

La composición de escritorio de DWM permite separar y proteger las ventanas de aplicaciones de escritorio de las nuevas ventanas de aplicaciones de Windows Store mediante la administración y separación de las ventanas de la aplicación de escritorio de las ventanas de Windows Store. Dado que la composición de escritorio es responsable de administrar todas las ventanas de la aplicación, deshabilitar la composición de escritorio puede dar lugar a un comportamiento inesperado. Además, la composición de escritorio es responsable de componer el nuevo menú Inicio, así como de animaciones de ventana adicionales que forman la personalidad principal del nuevo Windows operativo.

## <a name="controlling-desktop-composition"></a>Control de la composición del escritorio

En Windows Vista y Windows 7, la composición de escritorio está deshabilitada en una serie de escenarios. En Windows 8, la composición de escritorio de DWM es un componente principal del sistema operativo y no se puede deshabilitar. Con algunas excepciones, la composición de escritorio está siempre en estado on; se inicia antes del inicio de sesión del usuario y permanece activo durante la sesión. En esta sección se describe cómo Windows 8 los escenarios de Windows 7 en los que la composición de escritorio está deshabilitada.

**SKU de servidor y determinadas SKU de cliente**

En Windows 8, todas las SKU de servidor y cliente tienen habilitada la composición de escritorio. Esto garantiza que los administradores y usuarios del servidor puedan beneficiarse de las experiencias habilitadas por la composición del escritorio.

**Requisitos fundamentales para la composición de escritorio**

Windows 8 garantiza que los requisitos de profundidad de color del sistema y adaptador de gráficos se cumplen a través de la compatibilidad con el controlador WDDM y la profundidad de color del sistema.

**Compatibilidad con controladores WDDM**

Si un sistema no tiene un controlador de gráficos compatible con WDDM, Windows 8 adaptador de pantalla básico de Microsoft como adaptador predeterminado. Dado que DWM siempre se ejecuta en el adaptador predeterminado, elegirá Adaptador de pantalla básico de Microsoft para crear el escritorio cuando un controlador de gráficos compatible con WDDM no esté disponible (ya sea si no está instalado o deshabilitado) en el sistema.

El adaptador de pantalla básico de Microsoft es un rasterizador de software que usa la CPU en lugar de la GPU para realizar todo el dibujo. Tenga en cuenta que el rendimiento de la composición de escritorio en el adaptador de pantalla básico de Microsoft (especialmente las animaciones) puede no ser tan suave como cuando se ejecuta la composición de escritorio en una GPU.

**Profundidad de color del sistema**

Desktop Composition no se puede ejecutar a menos que la profundidad de color esté establecida en 32 bits por píxel. En Windows 7, la profundidad de color del sistema se puede cambiar en estos escenarios:

-   Un usuario final usa el panel Windows display o un panel de control de terceros para cambiar el color del sistema.
-   Un usuario final ejecuta una aplicación que cambia la profundidad de color del sistema a través de una API pública

A Windows 7, Windows 8 no admite una profundidad de color distinta de 32 bits por píxel. El usuario ya no puede cambiar la profundidad de color del sistema mediante el panel de control.

Además, los desarrolladores de aplicaciones no pueden usar las API para cambiar la profundidad de color del sistema. Windows 8 detectará las aplicaciones que intentan cambiar la profundidad de color del sistema a menos de 32 bits por píxel e informará al usuario de que se debe aplicar una corrección de compatibilidad de aplicaciones para ejecutar las aplicaciones. Después de la confirmación del usuario, se aplica la corrección de compatibilidad de la aplicación y la corrección de compatibilidad virtualiza el modo de color bajo en la aplicación mientras se mantiene el sistema en ejecución a 32 bits por píxel.

**WinSAT**

En Windows 8, la composición de escritorio no depende de las puntuaciones de WinSAT. Además, WinSAT ya no incluye la evaluación de DWM.

**Compatibilidad de aplicaciones y acción del usuario**

En Windows 8:

-   Se quitan todas las opciones para deshabilitar la composición de escritorio que existen en la ventana 7.
-   La composición de escritorio es responsable de componer todos los temas
-   Las aplicaciones no pueden usar DwmEnableComposition para deshabilitar la composición del escritorio. Para mantener la compatibilidad con versiones anteriores, una llamada a esta API devolverá éxito; sin embargo, la composición de escritorio no está deshabilitada
-   Se ha quitado la corrección de compatibilidad (shim) "Deshabilitar composición de escritorio".
-   Se ha quitado la opción "Deshabilitar composición de escritorio" de la pestaña compatibilidad del cuadro de diálogo Propiedades de la aplicación.

**Una aplicación usa un controlador de creación de reflejo para la comunicación remota**

En Windows 8:

-   No admite controladores reflejados para escenarios de comunicación remota. aunque la mayoría de las aplicaciones existentes que usan controladores reflejados deben seguir funcionando, debido al cambio de infraestructura necesario para admitir controladores reflejados existentes en Windows 8 con DWM ON, es posible que algunas características o aplicaciones que usan controladores reflejados no funcionen.
-   Admite api de duplicación de escritorio para desarrolladores de aplicaciones que usan controladores reflejados para escenarios de comunicación remota.
-   No admite controladores de reflejo de accesibilidad existentes
-   Los controladores de reflejo existentes deben actualizarse para asegurarse de que son compatibles con Windows 8

**Conexión a Escritorio remoto**

En Windows 8, la composición de escritorio siempre está habilitada para una conexión a Escritorio remoto. Un equipo cliente que se conecta a un Windows 8 remoto siempre tendrá habilitada la composición de escritorio para la sesión de Escritorio remoto independientemente de Windows versión del cliente. La composición de escritorio se admite para varios monitores en el equipo cliente, así como para la sesión de la aplicación remota.

Además, al conectarse a un Windows 8 remoto, esta configuración en Conexión a Escritorio remoto cliente no tiene efecto:

-   Profundidad de color
-   Casilla "Habilitar composición"

La profundidad de color de la conexión siempre se establece en 32 bits por píxel y la composición del escritorio siempre está habilitada.

 

 




