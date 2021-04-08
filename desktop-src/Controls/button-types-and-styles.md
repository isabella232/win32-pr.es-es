---
title: Tipos de botón
description: Hay varios tipos de botones y uno o varios estilos de botón para distinguir entre los botones del mismo tipo.
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682cc39ed2f88ce88f499757fbc4f902bfdceeea
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103794098"
---
# <a name="button-types"></a>Tipos de botón

Hay varios tipos de botones y uno o varios estilos de botón para distinguir entre los botones del mismo tipo.

En este documento se describen los temas siguientes.

-   [Tipos y estilos de botón](#button-types-and-styles)
-   [Casillas](#check-boxes)
-   [Cuadros de grupo](#group-boxes)
-   [Botones de reenvío](#push-buttons)
-   [Botones de radio](#radio-buttons)
-   [Temas relacionados](#related-topics)

## <a name="button-types-and-styles"></a>Tipos y estilos de botón

Un botón pertenece a un tipo y puede tener estilos adicionales que afecten a su apariencia y comportamiento. Para obtener una tabla de estilos de botón, consulte [estilos de botón](button-styles.md).

En la captura de pantalla siguiente se muestran los distintos tipos de botones.

![captura de pantalla de un cuadro de diálogo que muestra ejemplos de ocho tipos de botones](images/buttontypes.png)

En la captura de pantalla se muestra cómo pueden aparecer los botones en Windows Vista. La apariencia variará en diferentes versiones del sistema operativo y según el tema establecido por el usuario.

Tenga en cuenta los siguientes puntos acerca de la ilustración:

-   La casilla de tres Estados se muestra en el estado indeterminado. Cuando está activada o desactivada, tiene el aspecto de una casilla normal.
-   El botón de inserción grande se ha establecido en el estado insertado mediante programación (enviando el mensaje de [**BM \_ SETSTATE**](bm-setstate.md) ), para que conserve su apariencia incluso cuando no se haga clic en él.
-   En el estilo visual que se muestra, el fondo del botón de opción predeterminado (u otro botón de acción que tenga el foco de entrada) se desplaza entre el azul y el gris.

## <a name="check-boxes"></a>Casillas

Una *casilla* se compone de un cuadrado y una etiqueta, un icono o un mapa de bits definido por la aplicación que indica una opción que el usuario puede hacer seleccionando el botón. Normalmente, las aplicaciones muestran casillas para permitir al usuario elegir una o más opciones que no son mutuamente excluyentes.

Una casilla puede ser uno de cuatro estilos: estándar, automático, tres Estados y automático de tres Estados, tal y como se define en la [**\_ casilla**](button-styles.md)de verificación de constantes BS, [**BS \_ autocheckbox**](button-styles.md), [**BS \_ 3STATE**](button-styles.md)y [**BS \_ AUTO3STATE**](button-styles.md), respectivamente. Cada estilo puede suponer dos Estados de activación: activado (una marca de verificación dentro del cuadro) o desactivado (sin marca de verificación). Además, una casilla de tres Estados puede suponer un estado indeterminado (un cuadro sombreado dentro de la casilla), lo que puede significar que el usuario no ha realizado una selección. Al hacer clic varias veces en una casilla estándar o automática, se alterna entre activada y desactivada. Al hacer clic varias veces en una casilla de tres Estados, se alterna de activado a desactivado y, a continuación, se repite el ciclo.

Cuando el usuario hace clic en una casilla (de cualquier estilo), la casilla recibe el foco de teclado. El sistema envía a la ventana primaria de la casilla un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) que contiene el código de notificación en el que se ha [ \_ haga clic en BN](bn-clicked.md) . La ventana primaria no tiene que controlar este mensaje si proviene de una casilla automática o de una casilla de tres Estados automática, ya que el sistema establece automáticamente el estado de comprobación de esos estilos. Sin embargo, la ventana primaria debe controlar el mensaje si proviene de una casilla de verificación no automática o de tres Estados, porque la ventana primaria es responsable de establecer el estado de activación de esos estilos. Independientemente del estilo de casilla, el sistema vuelve a dibujar automáticamente la casilla una vez que se cambia su estado.

La aplicación puede determinar el estado de una casilla mediante la función [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

## <a name="group-boxes"></a>Cuadros de grupo

Un *cuadro de grupo* es un rectángulo que rodea un conjunto de controles, como las casillas o los botones de radio, con una etiqueta de texto definida por la aplicación en la esquina superior izquierda. El único propósito de un cuadro de grupo es organizar los controles relacionados con un propósito común (normalmente indicado por la etiqueta). El cuadro de grupo tiene solo un estilo, definido por el [**\_ GROUPBOX**](button-styles.md)de constante. Dado que no se puede seleccionar un cuadro de grupo, no tiene ningún estado de activación, estado de foco o estado de inserción.

## <a name="push-buttons"></a>Botones de reenvío

Un *botón de reenvío* es un rectángulo que contiene una etiqueta de texto definida por la aplicación, un icono o un mapa de bits que indica lo que hace el botón cuando el usuario lo selecciona.

Un botón de opción puede ser uno de dos estilos, estándar o predeterminado, tal y como se define en las constantes [**\_ PUSHBUTTON PUSHBUTTON**](button-styles.md) y [**BS \_ DEFPUSHBUTTON**](button-styles.md). Normalmente, se usa un botón de tecla de preinstalación estándar para iniciar una operación. Recibe el foco del teclado cuando el usuario hace clic en él. Un botón de opción predeterminado se usa normalmente para indicar la elección más común o predeterminada, como cerrar el cuadro de diálogo. Es un botón que el usuario puede seleccionar presionando entrar cuando ningún otro botón de acción del cuadro de diálogo tiene el foco de entrada.

Cuando el usuario hace clic en un botón de envío, recibe el foco de teclado. El sistema envía la ventana primaria del botón a un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) que contiene el código de notificación en el que se [ \_ hizo clic en BN](bn-clicked.md) .

El *botón de expansión* es un tipo especial de botón de instalación introducido en Windows Vista y en la [versión 6,00](common-control-versions.md). Un botón de expansión se divide en dos partes. La parte principal funciona como un botón de opción normal o predeterminado. La segunda parte tiene una flecha que apunta hacia abajo. Normalmente, se muestra un menú cuando se hace clic en la flecha.

Un botón de expansión tiene el estilo [**BS \_ SPLITBUTTON**](button-styles.md) o el estilo [**BS \_ DEFSPLITBUTTON**](button-styles.md) si es el botón predeterminado de un cuadro de diálogo. Puede modificar la apariencia del botón mediante el mensaje SETSPLITINFO de [**BCM \_**](bcm-setsplitinfo.md) o la macro SETSPLITINFO de [**botón \_**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) correspondiente.

Cuando el usuario hace clic en la parte principal del botón de expansión, envía una notificación de un [ \_ clic de BN](bn-clicked.md) como un botón de tecla de preinstalación normal. Pero cuando el usuario hace clic en la flecha hacia abajo, envía una notificación de [ \_ desplegable de BCN](bcn-dropdown.md) . Es responsabilidad de la aplicación mostrar un menú en respuesta a la \_ lista desplegable BCN.

Windows Vista y la [versión 6,00](common-control-versions.md) también introdujeron otro tipo de botón de comando, el *vínculo de comandos*. Visualmente, un vínculo de comando es muy diferente de un botón de comando normal, pero tiene la misma funcionalidad. Un vínculo de comando suele mostrar un icono de flecha, una línea de texto y texto adicional en una fuente menor.

## <a name="radio-buttons"></a>Botones de radio

Un *botón de radio* (también denominado botón de opción) consta de un botón redondo y una etiqueta, un icono o un mapa de bits definido por la aplicación que indica una opción que el usuario puede realizar seleccionando el botón. Normalmente, una aplicación usa botones de radio en un cuadro de grupo para permitir al usuario elegir uno de un conjunto de opciones relacionadas, pero mutuamente excluyentes.

Un botón de radio puede ser uno de dos estilos: estándar o automático, tal como se define en las constantes de estilo [**BS \_ RadioButton**](button-styles.md) y el [**\_ componente autoradiobutton de BS**](button-styles.md). Cada estilo puede suponer dos Estados de activación: activado (un punto en el botón) o desactivado (no hay ningún punto en el botón).

Cuando el usuario selecciona cualquier Estado, el botón de radio recibe el foco de teclado. El sistema envía la ventana primaria del botón a un mensaje de [**\_ comando de WM**](/windows/desktop/menurc/wm-command) que contiene el código de notificación en el que se [ \_ hizo clic en BN](bn-clicked.md) . No es necesario que la ventana primaria controle este mensaje si procede de un botón de radio automático, ya que el sistema establece automáticamente el estado de comprobación de ese estilo. Sin embargo, la ventana primaria debe controlar el mensaje si procede de un botón de radio no automático, ya que la ventana primaria es responsable de establecer el estado de comprobación de ese estilo. Independientemente del estilo del botón de radio, el sistema vuelve a dibujar automáticamente el botón a medida que cambia su estado.

Los botones de radio están organizados en grupos y solo se puede comprobar un botón del grupo en cualquier momento. Si se establece la marca de [**\_ Grupo WS**](/windows/desktop/winmsg/window-styles) para cualquier botón de radio, ese botón es el primer botón de un grupo y todos los botones que los siguen inmediatamente en el orden de tabulación (pero no tienen la marca de **\_ Grupo WS** ) forman parte de su grupo. Si ningún botón de radio tiene la marca de **\_ Grupo WS** , todos los botones de radio del cuadro de diálogo se tratarán como un solo grupo.

La aplicación puede determinar si se comprueba un botón de radio mediante la función [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Vista**
</dt> <dt>

[Usar botones](using-buttons.md)
</dt> </dl>

 

 