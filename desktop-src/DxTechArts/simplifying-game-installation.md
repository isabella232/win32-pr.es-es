---
title: Simplificación de la instalación de juegos
description: En este artículo se describen algunos conceptos que los desarrolladores de juegos para Windows pueden y deben implementar para mejorar la experiencia general.
ms.assetid: 356780b7-801d-c6dd-a266-6272bcb8bd36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53062b9905e59435f1b9175eb95832294d93e51193003622d3bcc6dd16ee07df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042483"
---
# <a name="simplifying-game-installation"></a>Simplificación de la instalación de juegos

Una ventaja importante de los juegos que se ejecutan en una consola en lugar de en Windows es el proceso de instalación o su falta. Cuando un juego se ejecuta por primera vez en una consola, el jugador realiza algunas opciones o confirmaciones y puede empezar a jugar casi inmediatamente. La instalación de un juego en Windows es más complicada, en comparación, por su necesidad de una entrada de usuario considerable y su proceso de instalación potencialmente largo. Sin embargo, este proceso de instalación se puede mejorar para proporcionar una mejor experiencia a los jugadores de Windows basados en juegos. En este artículo se describen algunos conceptos que los desarrolladores de juegos para Windows pueden y deben implementar para mejorar la experiencia general.

-   [Instalación típica de juegos](#typical-game-installation)
-   [Instalación simplificada de juegos](#simplified-game-installation)
    -   [Hacer todas las preguntas por adelantado](#ask-all-questions-up-front)
    -   [Proporcionar modos de instalación especiales](#provide-special-installation-modes)
    -   [Minimizar la cantidad de preguntas de instalación](#minimize-the-quantity-of-installation-questions)
    -   [Cambiar componentes opcionales a componentes necesarios](#change-optional-components-into-required-components)
    -   [Instalar siempre DirectX y Hacerlo de forma silenciosa](#always-install-directx-and-do-so-silently)
    -   [Piense en el CLUF.](#think-about-your-eula)
    -   [Inicio automático después de la instalación](#automatically-launch-after-installation)
    -   [Optimización del rendimiento de la instalación](#optimize-your-installation-performance)
    -   [Registro con Windows Firewall durante la instalación](#register-with-windows-firewall-during-installation)
    -   [Instalación para todos los usuarios, no solo para el usuario actual](#install-for-all-users-not-just-the-current-user)
-   [Ejemplo de instalación simplificada](#example-of-simplified-installation)
-   [Resumen](#summary)

## <a name="typical-game-installation"></a>Instalación típica de juegos

Al comparar la facilidad de instalación y la cantidad de tiempo necesario para empezar a jugar a un juego, la experiencia típica de Xbox es mucho mejor que Windows. En el gráfico de flujo de la figura 1 se muestran los procesos de instalación típicos en Xbox y Windows, para la comparación.

**Figura 1. Proceso de instalación típico, Xbox frente a Windows**

![xbox \- vs \- pc](images/pcvsconsoleinstall.png)

## <a name="simplified-game-installation"></a>Instalación simplificada de juegos

Sin embargo, no es necesario cumplir los mayores requisitos que se deben cumplir para que el usuario instale un juego en Windows juego. Al implementar los conceptos siguientes, disminuirá el número de pasos que debe completar un usuario, lo que puede reducir la cantidad de tiempo necesario para la instalación.

### <a name="ask-all-questions-up-front"></a>Hacer todas las preguntas por adelantado

Todas las opciones que selecciona el jugador durante la instalación que podrían provocar la anulación de la instalación deben ofrecerse antes que aquellas que no detengan la instalación. el peor de los casos es que el jugador tenga una opción que podría provocar la anulación de la instalación después de que el juego se haya copiado completamente de los medios de instalación. Esto puede resultar especialmente frustrante si la instalación requiere el intercambio de varios discos para completarse. Debe diseñar el instalador para que haga todas las preguntas importantes (como la aceptación del CLUF) al principio del proceso, de modo que la instalación no tenga que revertirse al final o cerca de su finalización.

También puede pedir al usuario que acepte el CLUF y que escriba la clave de producto cuando se inicia el juego por primera vez, en lugar de solicitarlo como parte de la instalación. En este escenario, rechazar aceptar el CLUF o cancelar durante la entrada de la clave de producto no revertirá la instalación, porque estos avisos forman parte del propio juego. Esto puede ser útil si tiene escenarios de OEM o preinstalados. Sin embargo, no pida al usuario que tome decisiones durante el inicio inicial que requieran credenciales administrativas.

### <a name="provide-special-installation-modes"></a>Proporcionar modos de instalación especiales

Idealmente, Windows instaladores de juegos solo deben ofrecer modos de instalación completamente automáticos y personalizados y nada entre ellos.

El modo automático no debe hacer más preguntas de las absolutamente necesarias para crear una instalación en funcionamiento y simplemente usar la configuración predeterminada sin solicitar otras opciones. A muchos jugadores no les importa la ubicación del juego en el disco duro o la configuración inicial del juego: solo quieren jugar al juego lo antes posible.

El modo personalizado solo debe ser para los usuarios avanzados que necesiten o quieran cambiar la ruta de instalación u otras opciones de instalación, y no debe ser el modo predeterminado.

El modo personalizado puede ofrecer la opción de una instalación completa o de una instalación mínima que instala solo los archivos necesarios para jugar al juego. Si el jugador elige una instalación mínima, el juego puede usar técnicas de instalación a petición o streaming para leer los datos de instalación restantes, lo que permite al jugador empezar a jugar rápidamente sin tener que esperar a que se complete una instalación completa. Sin embargo, la instalación de datos de esta manera tiene un impacto en el diseño del motor de juego. Para obtener más información sobre cómo instalar contenido a petición, vea [Install-on-Demand for Games](/windows/desktop/DxTechArts/install-on-demand-for-games).

### <a name="minimize-the-quantity-of-installation-questions"></a>Minimizar la cantidad de preguntas de instalación

En ambos modos de instalación, debe intentar limitar el número de veces que se solicita al jugador durante la instalación. Esto reducirá la cantidad de lectura necesaria para instalar y ejecutar el juego. Si es necesario, solo debe haber un aviso de seguimiento una vez finalizada la instalación. Como puede ver, el ejemplo que se muestra en la figura 1 tiene demasiados mensajes posteriores a la instalación.

### <a name="change-optional-components-into-required-components"></a>Cambiar componentes opcionales a componentes necesarios

Haga que la instalación de todos los componentes sea necesaria en lugar de convertirla en opcional, a menos que haya una buena razón para hacer lo contrario. La simple instalación de todos los componentes hará que el juego comience sin más retrasos ni problemas.

### <a name="always-install-directx-and-do-so-silently"></a>Instalar siempre DirectX y Hacerlo de forma silenciosa

Se recomienda encarecidamente que el juego instale de forma silenciosa directX redistribuible en el que se creó el juego. El proceso de instalación de DirectX está diseñado para que compruebe si es necesario actualizar algo y devuelve rápidamente si no lo hace. Por lo tanto, no es necesario preguntar a los usuarios si quieren instalar DirectX. Para realizar una instalación silenciosa de DirectX, ejecute este comando desde el paquete de instalación: **dxsetup.exe /silent**

Preguntar a un usuario si quiere instalar DirectX puede causar muchos problemas. Por ejemplo, si el usuario asume que tiene instalada la versión más reciente redistribuible y decide omitir la instalación de DirectX; La instalación del juego podría continuar correctamente de todos modos. Sin embargo, si el juego requiere una versión específica de D3DX u otra funcionalidad actualizada que se omitió, el juego no funcionará y el usuario estará muy frustrado.

Si por alguna razón debe preguntar al usuario si quiere instalar DirectX, el instalador debe anular y revertir, al menos, todo el proceso de instalación si el usuario decide no instalar DirectX. Revertir la instalación evitará los errores causados por que el sistema no tenga instalada la versión más reciente de DirectX cuando se inicie el juego.

Tenga en cuenta que es importante enviar el redistribuible con el que se creó el juego en lugar de simplemente enviar el redistribuible desde el SDK de DirectX más reciente. Es posible que la versión redistribuible más reciente no contenga todos los componentes encontrados en una versión anterior.

También es importante que el instalador compruebe lo que ya está instalado y determine si es necesario reiniciar el sistema. Si DirectX está actualizado, no es necesario reiniciar la copia de un archivo DLL.

### <a name="think-about-your-eula"></a>Piense en el CLUF.

El CLUF de DirectX puede y debe anexarse al CLUF del desarrollador del juego. No tiene sentido permitir que el usuario acepte el CLUF del desarrollador y no el CLUF de DirectX. El usuario debe aceptar ambas EULA o no instalar el juego. Si un desarrollador considera que debe ofrecer al usuario la opción, se producirá un error en toda la instalación si el usuario decide no aceptar el CLUF de DirectX.

Si es posible, consulte con su departamento legal para ver si puede evitar las EULA por completo y usar un CLUF encapsulado en reducción como el uso de juegos de consola. Esto evitará la necesidad de preguntar a los usuarios si quieren aceptar el CLUF. El CLUF de DirectX debe anexarse al CLUF reducido; De lo contrario, se debe mostrar y aceptar el CLUF de DirectX, lo que contrae el propósito de usar un CLUF ajustado para reducir.

Una excepción a un CLUF ajustado por reducción es para un editor de contenido. Cualquier editor debe mostrar un CLUF durante la instalación del editor o cuando el editor se inicia por primera vez. Muchos jugadores solo están interesados en reproducir y no en crear contenido, por lo que la instalación de un editor debe ser un proceso independiente.

### <a name="automatically-launch-after-installation"></a>Inicio automático después de la instalación

Casi todos los jugadores quieren jugar un juego en cuanto lo reciben. De forma predeterminada, el instalador debe iniciar el juego después de finalizar la instalación, aunque es una buena práctica, en una instalación personalizada, especificarlo en una casilla que el usuario pueda invalidar.

### <a name="optimize-your-installation-performance"></a>Optimización del rendimiento de la instalación

Los desarrolladores deben probar sus instalaciones para determinar cuánto tiempo se necesita para la instalación. Los desarrolladores pueden reducir el tiempo de instalación mediante la versión más reciente de sus herramientas de instalación y optimizando el diseño de datos en los medios de instalación. La mayoría de las herramientas de creación de DVD tienen opciones para la optimización del diseño que pueden mejorar los tiempos de instalación sin aumentar la carga de trabajo de desarrollo.

### <a name="register-with-windows-firewall-during-installation"></a>Registro con Windows Firewall durante la instalación

Si el juego se puede ejecutar como un servidor o el modelo de red del juego es punto a punto, registre el juego con Windows firewall en el momento de la instalación. Esto impedirá que el cuadro de diálogo de firewall se presente en medio del juego cuando el usuario intente acceder a la red. Si el juego es un cliente puro, el instalador no debe agregar el juego a la lista de excepciones del firewall.

Para obtener más información, consulte Windows Firewall para desarrolladores de juegos.

### <a name="install-for-all-users-not-just-the-current-user"></a>Instalación para todos los usuarios, no solo para el usuario actual

Simplemente, el valor predeterminado es instalar el juego para todos los usuarios. Esto permitirá que cualquier nuevo usuario del sistema pueda jugar al juego sin tener que instalarlo para ellos. Si se intenta instalar para todos los usuarios en una cuenta de Least-Privileged usuario, el instalador producirá un error o solicitará al usuario una contraseña de administrador. Por lo tanto, intente detectar si la cuenta tiene los privilegios adecuados antes de ofrecer la opción de instalar para todos los usuarios. Si el usuario decide instalar el juego solo para el usuario actual, asegúrese de cambiar la ruta de instalación a una ubicación dentro del perfil del usuario. Lo ideal es cambiar la ruta de acceso a algún lugar de datos de aplicación no móviles (por ejemplo, un subdirectorio de CSIDL \_ LOCAL \_ APPDATA).

## <a name="example-of-simplified-installation"></a>Ejemplo de instalación simplificada

A continuación, en la figura 2 se muestra un ejemplo de un proceso mejorado para instalar un juego en Windows, con diálogos de instalación simplificados.

**Figura 2. Proceso de instalación simplificado**

![instalar](images/simplifiedgameinstall.png)

Los siguientes son puntos importantes a tener en cuenta:

-   El instalador se inicia automáticamente tras la inserción del disco de instalación (ejecución automática).
-   La pantalla de presentación , con opciones para instalar, quitar, ver el sitio web o salir, no se muestra si el juego aún no está instalado en el equipo.
-   El **cuadro de** diálogo Instalación es el primer diálogo que muestra el instalador.
-   El **botón** Instalar es la implementación del modo de instalación automática.
-   El **botón** Opciones es la implementación del modo de instalación personalizada.
-   El **botón** Cancelar se cerrará inmediatamente del instalador. Dado que iniciar el instalador es una acción trivial para el usuario, no solicite confirmación.
-   Una vez que el usuario acepta el CLUF y escribe una clave de producto válida, se inicia la instalación.
-   Una vez completado el proceso de instalación, el juego se iniciará automáticamente o mostrará un cuadro de  diálogo que avisa al usuario de que la instalación se ha completado y ofrece opciones adicionales, en función de si se ha seleccionado Ejecutar juego después de la instalación.
-   La **casilla Ejecutar juego** proporciona otra oportunidad para iniciar el juego, para mayor comodidad. Esta opción siempre no está seleccionada  de forma predeterminada, ya  que el cuadro de diálogo Instalación completa solo se puede mostrar si Ejecutar juego después de la instalación no se ha seleccionado en el cuadro de diálogo **Opciones de** instalación.
-   El **botón** Aceptar descarta el cuadro de diálogo y, opcionalmente, toma medidas en las casillas **Ejecutar** y Ver el **archivo Léame.**

## <a name="summary"></a>Resumen

Los jugadores quieren estar haciendo un juego lo antes posible. Lo último que un jugador quiere hacer es pasar por diálogos y tomar decisiones que sean las mismas que para todos los demás juegos que haya instalado. La implementación de estas ideas puede reducir la cantidad de tiempo que un jugador dedica a instalar un juego en Windows y ayudar a mejorar la calidad general de la experiencia de Windows juegos.

 

 