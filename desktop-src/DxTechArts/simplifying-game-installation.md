---
title: Simplificar la instalación de juegos
description: En este artículo se describen algunos conceptos que los desarrolladores de juegos para Windows pueden y deben implementar para mejorar la experiencia general.
ms.assetid: 356780b7-801d-c6dd-a266-6272bcb8bd36
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8728eb2c9c53a99673ee742a5c961b91e37abed6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359213"
---
# <a name="simplifying-game-installation"></a>Simplificar la instalación de juegos

Una ventaja importante de los juegos que se ejecutan en una consola en lugar de en Windows es el proceso de instalación, o la ausencia de este. Cuando un juego se ejecuta por primera vez en una consola, el jugador realiza algunas elecciones o confirmaciones y es capaz de comenzar a reproducirse casi de inmediato. La instalación de un juego en Windows es más complicada, por comparación, por su necesidad de intervención del usuario considerable y de un proceso de instalación potencialmente largo. Sin embargo, se puede mejorar este proceso de instalación para proporcionar una mejor experiencia a los reproductores de juegos basados en Windows. En este artículo se describen algunos conceptos que los desarrolladores de juegos para Windows pueden y deben implementar para mejorar la experiencia general.

-   [Instalación típica del juego](#typical-game-installation)
-   [Instalación simplificada de un juego](#simplified-game-installation)
    -   [Formule todas las preguntas por adelantado](#ask-all-questions-up-front)
    -   [Proporcionar modos de instalación especiales](#provide-special-installation-modes)
    -   [Minimizar la cantidad de preguntas de instalación](#minimize-the-quantity-of-installation-questions)
    -   [Cambiar componentes opcionales en componentes necesarios](#change-optional-components-into-required-components)
    -   [Instalar siempre DirectX y hacerlo de forma silenciosa](#always-install-directx-and-do-so-silently)
    -   [Piense en su CLUF](#think-about-your-eula)
    -   [Iniciar automáticamente después de la instalación](#automatically-launch-after-installation)
    -   [Optimizar el rendimiento de la instalación](#optimize-your-installation-performance)
    -   [Registrarse en el Firewall de Windows durante la instalación](#register-with-windows-firewall-during-installation)
    -   [Instalación para todos los usuarios, no solo para el usuario actual](#install-for-all-users-not-just-the-current-user)
-   [Ejemplo de instalación simplificada](#example-of-simplified-installation)
-   [Resumen](#summary)

## <a name="typical-game-installation"></a>Instalación típica del juego

Al comparar la facilidad de instalación y la cantidad de tiempo necesario para comenzar a reproducir un juego, la experiencia típica de Xbox es mucho mejor que Windows. En el diagrama de flujo de la figura 1 se muestran los procesos de instalación típicos en Xbox y en Windows para realizar la comparación.

**Figura 1. Proceso de instalación típico, Xbox frente a Windows**

![Xbox \- vs \- PC](images/pcvsconsoleinstall.png)

## <a name="simplified-game-installation"></a>Instalación simplificada de un juego

Sin embargo, no es necesario que los requisitos mayores que se colocan en el usuario para instalar un juego en Windows. Mediante la implementación de los siguientes conceptos, disminuirá el número de pasos que debe completar un usuario, lo que puede reducir la cantidad de tiempo necesario para la instalación.

### <a name="ask-all-questions-up-front"></a>Formule todas las preguntas por adelantado

Todas las opciones que el jugador selecciona durante la instalación y que pueden provocar la anulación de la instalación se deben ofrecer antes que las que no detendrán la instalación. el escenario del peor de los casos es que el jugador ofrezca una opción que podría hacer que la instalación se anulara después de que el juego se copiara por completo desde el disco de instalación. Esto puede ser especialmente frustrante si la instalación requiere el intercambio de varios discos para completarse. Debe diseñar el instalador para que formule preguntas importantes (por ejemplo, la aceptación del CLUF) al principio del proceso, de modo que no sea necesario revertir la instalación a o cerca de su finalización.

También puede pedir al usuario que acepte el CLUF y que escriba la clave del producto cuando el juego se inicie por primera vez, en lugar de solicitarlos como parte de la instalación. En este escenario, el rechazo de la aceptación del CLUF o la cancelación durante la entrada de la clave de producto no revertirá la instalación, ya que estos mensajes son parte del propio juego. Esto puede ser útil si tiene escenarios preinstalados o OEM. Sin embargo, tenga cuidado de no pedir al usuario que realice elecciones durante el inicio inicial que requieran credenciales administrativas.

### <a name="provide-special-installation-modes"></a>Proporcionar modos de instalación especiales

Idealmente, los instaladores de juegos de Windows solo deben ofrecer modos completamente automático y personalizado de instalación y nada entre ellos.

El modo automático no debe plantear más preguntas de las necesarias para crear una instalación en funcionamiento y simplemente usar la configuración predeterminada sin preguntar otras opciones. Muchos jugadores no se interesan en la ubicación del juego en el disco duro o en la configuración inicial del juego, sino que solo quieren jugar lo antes posible.

El modo personalizado solo debe ser para los usuarios avanzados que necesiten o deseen cambiar la ruta de instalación u otras opciones de instalación, y no debe ser el modo predeterminado.

El modo personalizado puede ofrecer la opción de una instalación completa o de una instalación mínima que solo instala los archivos necesarios para reproducir el juego. Si el jugador elige la instalación mínima, el juego puede usar técnicas de instalación a petición o de streaming para leer los datos de instalación restantes, lo que permite que el jugador empiece a reproducir el juego rápidamente sin tener que esperar a que se complete una instalación completa. Sin embargo, la instalación de los datos de esta manera afecta al diseño del motor de juegos. Para obtener más información sobre la instalación de contenido a petición, consulte [instalación a petición de juegos](/windows/desktop/DxTechArts/install-on-demand-for-games).

### <a name="minimize-the-quantity-of-installation-questions"></a>Minimizar la cantidad de preguntas de instalación

En ambos modos de instalación, debe intentar limitar el número de veces que se solicita el jugador durante la instalación. Esto reducirá la cantidad de lectura necesaria para que el juego se instale y se ejecute. Si es necesario, solo debería haber una solicitud de seguimiento una vez finalizada la instalación. Como puede ver, el ejemplo que se muestra en la figura 1 tiene demasiadas solicitudes posteriores a la instalación.

### <a name="change-optional-components-into-required-components"></a>Cambiar componentes opcionales en componentes necesarios

Realice la instalación de todos los componentes necesarios en lugar de hacer que cualquiera de ellos sea opcional, a menos que haya una buena razón para hacer lo contrario. Basta con instalar todos los componentes para que el juego se inicie sin retrasos y complicaciones.

### <a name="always-install-directx-and-do-so-silently"></a>Instalar siempre DirectX y hacerlo de forma silenciosa

Se recomienda encarecidamente que el juego Instale de forma silenciosa el paquete redistribuible de DirectX con el que se compiló el juego. El proceso de instalación de DirectX está diseñado de modo que compruebe si es necesario actualizar algo y devuelve rápidamente si no lo hace. Por lo tanto, no es necesario preguntar a los usuarios si desean instalar DirectX. Para realizar una instalación silenciosa de DirectX, ejecute este comando desde el paquete de instalación: **dxsetup.exe/Silent**

Preguntar a un usuario si desea instalar DirectX puede causar muchos problemas. Por ejemplo, si el usuario supone que tiene la versión más reciente del paquete redistribuible instalada y elige omitir la instalación de DirectX. la instalación del juego podría continuar correctamente de todos modos. Sin embargo, si el juego requiere una versión específica de D3DX, u otra funcionalidad actualizada que se omitió, el juego no funcionará y el usuario se verá muy frustrado.

Si por alguna razón debe preguntar al usuario si desea instalar DirectX, el instalador debe, al menos, anular y revertir todo el proceso de instalación si el usuario decide no instalar DirectX. La reversión de la instalación evitará que se produzcan errores causados por el sistema que no tiene instalada la versión más reciente de DirectX cuando se inicia el juego.

Tenga en cuenta que es importante enviar el redistribuible en el que se compiló el juego en lugar de simplemente enviar el redistribuible desde el último SDK de DirectX. Es posible que el último redistribuible no contenga todos los componentes encontrados en una versión anterior.

También es importante que el instalador compruebe lo que ya está instalado y determine si es necesario reiniciar el sistema. Si DirectX está actualizado, la copia de una DLL no debe reiniciarse.

### <a name="think-about-your-eula"></a>Piense en su CLUF

El CLUF de DirectX puede y debe anexarse al CLUF del desarrollador de juegos. No hay ningún punto en permitir al usuario aceptar el CLUF del desarrollador y no el CLUF de DirectX. El usuario debe aceptar ambos CLUF o no instalar el juego. Si un desarrollador piensa que debe ofrecer al usuario la opción, se producirá un error en toda la instalación si el usuario decide no aceptar el CLUF de DirectX.

Si es posible, póngase en contacto con su departamento legal para ver si puede evitar por completo los términos de licencia y usar un CLUF incluido en la reducción, como los juegos de consola. Esto evitará la necesidad de preguntar a los usuarios si quieren aceptar el CLUF. El CLUF de DirectX debe anexarse al CLUF ajustado contra la reducción; de lo contrario, se debe mostrar y aceptar el CLUF de DirectX, lo que anula el propósito de usar un CLUF ajustado con reducción.

Una excepción a un CLUF ajustado por reducción es para un editor de contenido. Cualquier editor necesita mostrar un CLUF durante la instalación del editor o cuando el editor se inicia por primera vez. Muchos jugadores solo están interesados en jugar y no en el contenido, por lo que la instalación de un editor debe ser un proceso independiente.

### <a name="automatically-launch-after-installation"></a>Iniciar automáticamente después de la instalación

Casi todos los jugadores quieren jugar al juego en cuanto lo reciben. De forma predeterminada, el instalador debe iniciar el juego después de finalizar la instalación, aunque en una instalación personalizada se recomienda especificar esto en una casilla que el usuario pueda invalidar.

### <a name="optimize-your-installation-performance"></a>Optimizar el rendimiento de la instalación

Los desarrolladores deben probar sus instalaciones para determinar cuánto tiempo se requiere para la instalación. Los desarrolladores pueden reducir el tiempo de instalación mediante el uso de la versión más reciente de sus herramientas de instalación y la optimización del diseño de los datos en los medios de instalación. La mayoría de las herramientas de creación de DVD tienen opciones de optimización de diseño que pueden mejorar los tiempos de instalación sin aumentar la carga de trabajo de desarrollo.

### <a name="register-with-windows-firewall-during-installation"></a>Registrarse en el Firewall de Windows durante la instalación

Si el juego puede ejecutarse como un servidor o el modelo de red del juego es de punto a punto, registre el juego con el Firewall de Windows en el momento de la instalación. Esto impedirá que el cuadro de diálogo de Firewall se expulse en el centro del juego cuando el usuario intente acceder a la red. Si el juego es un cliente puro, el instalador no debería agregar el juego a la lista de excepciones del firewall.

Para obtener más información, vea Firewall de Windows para desarrolladores de juegos.

### <a name="install-for-all-users-not-just-the-current-user"></a>Instalación para todos los usuarios, no solo para el usuario actual

Solo tiene que instalar el juego de forma predeterminada para todos los usuarios. Esto permitirá que cualquier usuario nuevo del sistema juegue el juego sin tener que instalarlo para ellos. Si se intenta realizar la instalación para todos los usuarios en una cuenta de usuario Least-Privileged, se producirá un error en el instalador o se solicitará al usuario una contraseña de administrador. Por lo tanto, intente detectar si la cuenta tiene los privilegios adecuados antes de ofrecer la opción de instalación para todos los usuarios. Si el usuario decide instalar el juego solo para el usuario actual, asegúrese de cambiar la ruta de instalación a una ubicación en el perfil del usuario. Idealmente, cambie la ruta de acceso a alguna parte de los datos de aplicaciones que no sean móviles (por ejemplo, un subdirectorio de CSIDL \_ local \_ AppData).

## <a name="example-of-simplified-installation"></a>Ejemplo de instalación simplificada

En la figura 2 se proporciona un ejemplo de un proceso mejorado para instalar un juego en Windows, con cuadros de diálogo de instalación simplificados.

**Figura 2. Proceso de instalación simplificado**

![instalar](images/simplifiedgameinstall.png)

Estos son algunos puntos importantes de la Nota:

-   El instalador se inicia automáticamente al insertar el disco de instalación (ejecución automática).
-   La pantalla de presentación (con opciones para instalar, quitar, ver el sitio web o salir) no se muestra si el juego aún no está instalado en el equipo.
-   El cuadro de diálogo de **instalación** es el primer cuadro de diálogo que muestra el instalador.
-   El botón **instalar** es la implementación del modo de instalación automática.
-   El botón **Opciones** es la implementación del modo de instalación personalizada.
-   El botón **Cancelar** cerrará inmediatamente el instalador. Dado que el inicio del instalador es una acción trivial para el usuario, no pida confirmación.
-   Una vez que el usuario acepte el CLUF y escriba una clave de producto válida, se iniciará la instalación.
-   Una vez completado el proceso de instalación, el juego se iniciará automáticamente o mostrará un cuadro de diálogo que avisa al usuario de que la instalación ha finalizado y ofrece opciones adicionales, en función de si se ha seleccionado **Ejecutar juego después** de la instalación.
-   La casilla **Ejecutar juego** proporciona otra oportunidad para lanzar el juego, por comodidad. Esta opción está siempre desactivada de forma predeterminada, ya que el cuadro de diálogo **Instalación completada** solo se puede mostrar si **Ejecutar juego después** de la instalación no se seleccionó en el cuadro de diálogo **Opciones de instalación** .
-   El botón **Aceptar** descarta el cuadro de diálogo y, opcionalmente, realiza una acción en las casillas **Ejecutar** y **ver el archivo Léame** .

## <a name="summary"></a>Resumen

Los jugadores quieren jugar lo antes posible. Lo último que un jugador desea hacer es WADING a través de cuadros de diálogo y realizar elecciones que son las mismas que para todos los demás juegos que ha instalado. La implementación de estas ideas puede acortar el tiempo que un jugador invierte en instalar un juego en Windows y ayudar a mejorar la calidad general de la experiencia de juegos de Windows.

 

 