---
title: Tipos de botón
description: Hay varios tipos de botones y uno o varios estilos de botón para distinguir entre botones del mismo tipo.
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682cc39ed2f88ce88f499757fbc4f902bfdceeea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173985"
---
# <a name="button-types"></a>Tipos de botón

Hay varios tipos de botones y uno o varios estilos de botón para distinguir entre botones del mismo tipo.

En este documento se de tratan los temas siguientes.

-   [Estilos y tipos de botón](#button-types-and-styles)
-   [Casillas](#check-boxes)
-   [Cuadros de grupo](#group-boxes)
-   [Botones](#push-buttons)
-   [Botones de radio](#radio-buttons)
-   [Temas relacionados](#related-topics)

## <a name="button-types-and-styles"></a>Estilos y tipos de botón

Un botón pertenece a un tipo y puede tener estilos adicionales que afectan a su apariencia y comportamiento. Para obtener una tabla de estilos de botón, vea [Estilos de botón](button-styles.md).

En la siguiente captura de pantalla se muestran los distintos tipos de botones.

![captura de pantalla de un cuadro de diálogo que muestra ejemplos de ocho tipos de botones](images/buttontypes.png)

La captura de pantalla muestra cómo pueden aparecer los botones Windows Vista. La apariencia variará según las distintas versiones del sistema operativo y según el tema establecido por el usuario.

Tenga en cuenta los siguientes puntos sobre la ilustración:

-   La casilla de tres estados se muestra en estado indeterminado. Cuando está activada o desactivada, parece una casilla normal.
-   El botón de inserción grande se ha establecido en el estado de inserción mediante programación (mediante el envío del mensaje [**\_ BM SETSTATE),**](bm-setstate.md) de modo que conserva su apariencia incluso cuando no se hace clic en él.
-   En el estilo visual que se muestra, el fondo del botón de inserción predeterminado (u otro botón de inserción que tenga el foco de entrada) se cycles between blue and gray (Azul y gris).

## <a name="check-boxes"></a>Casillas

Una *casilla consta* de un cuadro cuadrado y una etiqueta, un icono o un mapa de bits definidos por la aplicación que indica una opción que el usuario puede realizar seleccionando el botón. Las aplicaciones suelen mostrar casillas para permitir al usuario elegir una o varias opciones que no son mutuamente excluyentes.

Una casilla puede ser de uno de cuatro estilos: estándar, automático, de tres estados y automático de tres estados, tal como se define en las constantes [**BS \_ CHECKBOX**](button-styles.md), [**BS \_ AUTOCHECKBOX,**](button-styles.md) [**BS \_ 3STATE**](button-styles.md)y [**BS \_ AUTO3STATE,**](button-styles.md)respectivamente. Cada estilo puede suponer dos estados de comprobación: activado (una marca de verificación dentro de la casilla) o desactivado (sin marca de verificación). Además, una casilla de tres estados puede asumir un estado indeterminado (una casilla sombreada dentro de la casilla), lo que podría indicar que el usuario no ha elegido ninguna opción. Al hacer clic repetidamente en una casilla estándar o automática, se cambia de activado a desactivado y de nuevo. Al hacer clic repetidamente en una casilla de tres estados, se cambia de activado a desactivado a indeterminado y, a continuación, se repite el ciclo.

Cuando el usuario hace clic en una casilla (de cualquier estilo), la casilla recibe el foco del teclado. El sistema envía a la ventana primaria de la casilla un mensaje [**\_ WM COMMAND**](/windows/desktop/menurc/wm-command) que contiene el código de notificación CLICKED de [BN. \_](bn-clicked.md) La ventana primaria no tiene que controlar este mensaje si procede de una casilla automática o una casilla automática de tres estados, ya que el sistema establece automáticamente el estado de comprobación para esos estilos. Pero la ventana primaria debe controlar el mensaje si procede de una casilla no automática o de tres estados, ya que la ventana primaria es responsable de establecer el estado de comprobación de esos estilos. Independientemente del estilo de casilla, el sistema vuelve a dibujar automáticamente la casilla una vez que se cambia su estado.

La aplicación puede determinar el estado de una casilla mediante la [**función IsDlgButtonChecked.**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked)

## <a name="group-boxes"></a>Cuadros de grupo

Un *cuadro de grupo* es un rectángulo que rodea un conjunto de controles, como casillas o botones de radio, con una etiqueta de texto definida por la aplicación en la esquina superior izquierda. El único propósito de un cuadro de grupo es organizar los controles relacionados con un propósito común (normalmente indicado por la etiqueta ). El cuadro de grupo solo tiene un estilo, definido por la [**constante BS \_ GROUPBOX**](button-styles.md). Dado que no se puede seleccionar un cuadro de grupo, no tiene ningún estado de comprobación, estado de foco o estado de inserción.

## <a name="push-buttons"></a>Botones

Un *botón de inserción* es un rectángulo que contiene una etiqueta de texto definida por la aplicación, un icono o un mapa de bits que indica lo que hace el botón cuando el usuario lo selecciona.

Un botón de inserción puede ser uno de dos estilos, estándar o predeterminado, tal como se define en las constantes [**BS \_ PUSHBUTTON**](button-styles.md) y [**BS \_ DEFPUSHBUTTON**](button-styles.md). Normalmente, se usa un botón de inserción estándar para iniciar una operación. Recibe el foco del teclado cuando el usuario hace clic en él. Normalmente, se usa un botón de inserción predeterminado para indicar la opción más común o predeterminada, como cerrar el cuadro de diálogo. Es un botón que el usuario puede seleccionar simplemente presionando ENTRAR cuando ningún otro botón de inserción del cuadro de diálogo tenga el foco de entrada.

Cuando el usuario hace clic en un botón de inserción, recibe el foco del teclado. El sistema envía a la ventana primaria del botón un [**mensaje \_ WM COMMAND**](/windows/desktop/menurc/wm-command) que contiene el código de notificación [ \_ BN CLICKED.](bn-clicked.md)

El *botón de división* es un tipo especial de botón de inserción introducido en Windows Vista y versión [6.00.](common-control-versions.md) Un botón de división se divide en dos partes. La parte principal funciona como un botón de inserción normal o predeterminado. La segunda parte tiene una flecha que apunta hacia abajo. Normalmente se muestra un menú cuando se hace clic en la flecha.

Un botón de división tiene el estilo [**\_ SPLITBUTTON**](button-styles.md) de BS o el estilo [**\_ BS DEFSPLITBUTTON**](button-styles.md) si es el botón predeterminado en un cuadro de diálogo. Puede modificar la apariencia del botón mediante el mensaje [**\_ SETSPLITINFO**](bcm-setsplitinfo.md) de BCM o la macro [**Button \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) correspondiente.

Cuando el usuario hace clic en la parte principal del botón de división, envía una notificación [BN \_ CLICKED](bn-clicked.md) igual que un botón de inserción normal. Pero cuando el usuario hace clic en la flecha abajo, envía una notificación [DE LISTA DESPLEGABLE \_ de BCN.](bcn-dropdown.md) Es responsabilidad de la aplicación mostrar un menú en respuesta a LA LISTA DESPLEGABLE de \_ BCN.

Windows Vista y [la versión 6.00](common-control-versions.md) también presentaron otro tipo de botón de inserción, el *vínculo de comando*. Visualmente, un vínculo de comando es muy diferente de un botón de inserción normal, pero tiene la misma funcionalidad. Normalmente, un vínculo de comando muestra un icono de flecha, una línea de texto y texto adicional en una fuente más pequeña.

## <a name="radio-buttons"></a>Botones de radio

Un *botón de radio* (también denominado botón de opción) consta de un botón de redondeo y una etiqueta, un icono o un mapa de bits definidos por la aplicación que indica una opción que el usuario puede realizar seleccionando el botón. Normalmente, una aplicación usa botones de radio en un cuadro de grupo para permitir al usuario elegir uno de un conjunto de opciones relacionadas pero mutuamente excluyentes.

Un botón de radio puede ser uno de dos estilos: estándar o automático, tal y como se define en las constantes de estilo [**BS \_ RADIOBUTTON**](button-styles.md) y [**BS \_ AUTORADIOBUTTON**](button-styles.md). Cada estilo puede asumir dos estados de comprobación: activado (un punto en el botón) o desactivado (sin punto en el botón).

Cuando el usuario selecciona cualquiera de los estados, el botón de radio recibe el foco del teclado. El sistema envía a la ventana primaria del botón un mensaje [**\_ WM COMMAND**](/windows/desktop/menurc/wm-command) que contiene el código de notificación CLICKED de [BN. \_](bn-clicked.md) La ventana primaria no necesita controlar este mensaje si procede de un botón de radio automático, ya que el sistema establece automáticamente el estado de comprobación para ese estilo. Pero la ventana primaria debe controlar el mensaje si procede de un botón de radio no automático, ya que la ventana primaria es responsable de establecer el estado de comprobación para ese estilo. Independientemente del estilo del botón de radio, el sistema vuelve a dibujar el botón automáticamente a medida que cambia su estado.

Los botones de radio se organizan en grupos y solo se puede comprobar un botón del grupo en cualquier momento. Si la marca [**WS \_ GROUP**](/windows/desktop/winmsg/window-styles) está establecida para cualquier botón de radio, ese botón es el primer botón de un grupo y todos los botones que lo siguen inmediatamente en el orden de tabulación (pero no tienen la marca **WS \_ GROUP)** forman parte de su grupo. Si ningún botón de radio tiene la **marca WS \_ GROUP,** todos los botones de radio del cuadro de diálogo se tratan como un único grupo.

La aplicación puede determinar si se comprueba un botón de radio mediante la [**función IsDlgButtonChecked.**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Estilos de botón](button-styles.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Usar botones](using-buttons.md)
</dt> </dl>

 

 