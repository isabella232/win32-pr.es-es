---
title: Administrador de ventanas de escritorio está siempre activado
description: Administrador de ventanas de escritorio está siempre activado
ms.assetid: 36E2DD1B-E480-47A9-850B-3057119641C0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f855635615dee734b9a719d4e51d3ead663d144e
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104359459"
---
# <a name="desktop-window-manager-is-always-on"></a>Administrador de ventanas de escritorio está siempre activado

## <a name="platforms"></a>Plataformas

**Clientes** : Windows 8  
**Servidores** : Windows Server 2012  


## <a name="description"></a>Descripción

En Windows 8, Administrador de ventanas de escritorio (DWM) está siempre activado y los usuarios finales y las aplicaciones no pueden deshabilitarlo. Como en Windows 7, DWM se usa para crear el escritorio. Además de las experiencias habilitadas en Windows 7, la composición de escritorio de DWM permite la composición del escritorio para todos los temas, compatibilidad con Stereoscopic 3D, y administración, separación y protección de la experiencia con aplicaciones de la tienda Windows.

**Composición del escritorio para todos los temas**

En Windows Vista y Windows 7, la composición de escritorio solo está habilitada con el tema AERO Glass. Por lo tanto, los usuarios de los temas de contraste alto y clásico de Windows no pueden usar experiencias habilitadas por la composición del escritorio, como Windows Flip, el escalado automático para el escalado de alta resolución (PPP), la vista previa en miniatura y la lupa de pantalla completa Además, en estas versiones anteriores de Windows, los desarrolladores de aplicaciones deben escribir y mantener varias rutas de acceso de código, una en la que la composición de escritorio está habilitada y otra en la que la composición de escritorio está deshabilitada.

Con Windows 8, la composición de escritorio está habilitada para todos los temas. Los usuarios de temas clásicos y de contraste alto de Windows pueden usar las experiencias habilitadas por la composición del escritorio, como Windows Flip, el escalado automático para el escalado de alta resolución (PPP), las vistas previas en miniatura y el ampliador de pantalla completa. Además, los desarrolladores no necesitan escribir y mantener varias rutas de acceso de código, lo que simplifica el desarrollo.

**Compatibilidad con Stereoscopic 3D**

La composición de escritorio de DWM admite la representación y presentación del contenido de la aplicación de Stereoscopic 3D de pantalla completa y con ventanas.

**Administración, separación y protección de la experiencia con aplicaciones de la tienda Windows**

La composición de escritorio de DWM permite separar y proteger las ventanas de aplicación de escritorio de las nuevas ventanas de aplicaciones de la tienda Windows mediante la administración y separación de las ventanas de aplicación de escritorio desde las ventanas de aplicaciones de la tienda Windows. Dado que la composición del escritorio es responsable de administrar todas las ventanas de la aplicación, deshabilitar la composición del escritorio puede producir un comportamiento inesperado. Además, la composición de escritorio es responsable de crear el nuevo menú Inicio, así como animaciones de ventana adicionales que forman la personalidad principal del nuevo sistema operativo Windows.

## <a name="controlling-desktop-composition"></a>Controlar la composición de escritorio

En Windows Vista y Windows 7, la composición de escritorio está deshabilitada en varios escenarios. En Windows 8, la composición de escritorio DWM es un componente básico del sistema operativo y no se puede deshabilitar. Con algunas excepciones, la composición del escritorio siempre está activada; se inicia antes del inicio de sesión del usuario y permanece activo mientras dure una sesión. En esta sección se describe cómo Windows 8 trata los escenarios de Windows 7 en los que la composición de escritorio está deshabilitada.

**SKU de servidor y ciertas SKU de cliente**

En Windows 8, todas las SKU de servidor y cliente tienen la composición de escritorio habilitada. Esto garantiza que los administradores del servidor y los usuarios puedan beneficiarse de las experiencias habilitadas por la composición del escritorio.

**Requisitos fundamentales para la composición de escritorio**

Windows 8 garantiza que se cumplan los requisitos de profundidad de color del sistema y el adaptador de gráficos a través de la compatibilidad con controladores WDDM y la profundidad de color del sistema.

**Compatibilidad con controladores WDDM**

Si un sistema no tiene un controlador de gráficos compatible con WDDM, Windows 8 usa el adaptador de pantalla básico de Microsoft como adaptador predeterminado. Como DWM siempre se ejecuta en el adaptador predeterminado, elegirá el adaptador de pantalla básico de Microsoft para crear el escritorio cuando un controlador de gráficos compatible con WDDM no esté disponible (ya esté instalado o deshabilitado) en el sistema.

El adaptador de pantalla básico de Microsoft es un rasterizador de software que usa la CPU en lugar de la GPU para realizar todo el dibujo. Tenga en cuenta que el rendimiento de la composición del escritorio en el adaptador de pantalla básico de Microsoft (especialmente animaciones) puede no ser tan suave como cuando se ejecuta la composición de escritorio en una GPU.

**Profundidad de color del sistema**

No se puede ejecutar la composición de escritorio a menos que la profundidad de color esté establecida en 32 bits por píxel. En Windows 7, la profundidad de color del sistema se puede cambiar en estos escenarios:

-   Un usuario final usa el panel de control pantalla de Windows o un panel de control de terceros para cambiar el color del sistema
-   Un usuario final ejecuta una aplicación que cambia la profundidad de color del sistema a través de una API pública.

A diferencia de Windows 7, Windows 8 no admite la profundidad de color que no sea 32 bits por píxel. El usuario ya no puede cambiar la profundidad de color del sistema mediante el panel de control.

Además, los desarrolladores de aplicaciones no pueden usar las API para cambiar la profundidad de color del sistema. Windows 8 detectará las aplicaciones que intentan cambiar la profundidad de color del sistema a menos de 32 bits por píxel e informará al usuario de que se debe aplicar una corrección de compatibilidad de aplicaciones para ejecutar las aplicaciones. Después de la confirmación del usuario, se aplica la corrección de compatibilidad de la aplicación y la corrección de compatibilidad virtualiza el modo de color inferior de la aplicación, a la vez que mantiene el sistema en ejecución en 32 bits por píxel.

**WinSAT**

En Windows 8, la composición de escritorio no depende de las puntuaciones de WinSAT. Además, WinSAT ya no incluye la evaluación de DWM.

**Compatibilidad de aplicaciones y acción del usuario**

En Windows 8:

-   Se quitan todas las opciones para deshabilitar la composición de escritorio que existen en la ventana 7
-   La composición del escritorio es responsable de crear todos los temas
-   Las aplicaciones no pueden usar DwmEnableComposition para deshabilitar la composición de escritorio. Para mantener la compatibilidad con versiones anteriores, una llamada a esta API devolverá un resultado correcto; sin embargo, la composición del escritorio no está deshabilitada
-   Se ha quitado la corrección de compatibilidad "deshabilitar composición de escritorio"
-   Se quita la opción "deshabilitar composición de escritorio" de la pestaña Compatibilidad del cuadro de diálogo Propiedades de la aplicación.

**Una aplicación usa un controlador de creación de reflejo para la comunicación remota**

En Windows 8:

-   No admite controladores de reflejo para escenarios de comunicación remota; Aunque la mayoría de las aplicaciones existentes que usan controladores de reflejo deben seguir funcionando, debido al cambio de infraestructura necesario para admitir los controladores reflejados existentes en Windows 8 con DWM en, es posible que algunas características o aplicaciones que usan controladores reflejados no funcionen.
-   Admite las API de duplicación de escritorio para los desarrolladores de aplicaciones que usan controladores de reflejo para escenarios de comunicación remota.
-   No es compatible con los controladores de reflejo de accesibilidad existentes
-   Los controladores de reflejo existentes se deben actualizar para asegurarse de que son compatibles con Windows 8

**Conexión a escritorio remoto**

En Windows 8, la composición de escritorio siempre está habilitada para una conexión de escritorio remoto. Un equipo cliente que se conecte a un equipo remoto con Windows 8 siempre obtendrá la composición de escritorio habilitada para la sesión de escritorio remoto con independencia de la versión de cliente de Windows. La composición del escritorio es compatible con varios monitores en el equipo cliente, así como con la sesión de la aplicación remota.

Además, al conectarse a un equipo remoto con Windows 8, esta configuración del cliente de Conexión a Escritorio remoto no surte efecto:

-   Profundidad de color
-   Casilla "habilitar composición"

La profundidad de color de la conexión siempre está establecida en 32 bits por píxel y la composición de escritorio siempre está habilitada.

 

 




