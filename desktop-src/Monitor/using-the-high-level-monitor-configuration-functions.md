---
title: Uso de las funciones de configuración High-Level Monitor
description: Uso de las funciones de configuración High-Level Monitor
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- monitor,functions
- monitor, funciones de configuración de alto nivel
- monitor, enumerar monitores físicos
- monitor, configuración continua
- supervisar la configuración, funciones de configuración de alto nivel
- monitor configuration,functions
- configuración de monitor, enumeración de monitores físicos
- configuración de monitor, configuración continua
- enumerar monitores físicos
- funciones de configuración de alto nivel
- configuración de monitor continuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827d19ef0006dc89208061c18ef34c28c8f993c3e0d6ebd0d1c1005daf2cd640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066605"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a>Uso de las funciones de configuración High-Level Monitor

## <a name="enumerating-physical-monitors"></a>Enumeración de monitores físicos

Hay varias funciones que enumeran los dispositivos de presentación, [**incluidos EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) [**y MonitorFromWindow.**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow) Estas funciones se documentan en la documentación Windows GDI, en el tema [Monitores de pantalla múltiples](/windows/desktop/gdi/multiple-display-monitors). Estas funciones devuelven **identificadores HMONITOR.** Sin embargo, a pesar del nombre, **un identificador HMONITOR** se puede asociar a más de un monitor físico. Para configurar los valores en un monitor, la aplicación debe obtener un identificador único para el monitor físico mediante una llamada a [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor).

Si la aplicación usa Direct3D, puede obtener un identificador de monitor desde un dispositivo Direct3D llamando a [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9).

## <a name="supported-functions"></a>Funciones admitidas

Es posible que un monitor no admita todas las funciones de configuración del monitor. Para averiguar qué funciones admite un monitor, llame a [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities).

## <a name="continuous-monitor-settings"></a>Monitor continuo Configuración

Una *configuración* de supervisión continua es aquella que puede oscilar entre algún valor mínimo y máximo. La mayoría de las funciones de configuración de supervisión de alto nivel controlan la configuración de supervisión continua. Por ejemplo, el brillo y el contraste son configuraciones continuas.

La configuración del monitor continuo no tiene unidades definidas del mundo real. Las unidades son arbitrarias y pueden variar de un fabricante a otro. Si dos monitores tienen el mismo valor de brillo, por ejemplo, un monitor podría tener un aspecto mucho más brillante que otro. Normalmente, una aplicación presentará controles deslizantes o controles de flecha hacia abajo al usuario. A continuación, el usuario puede ajustar la configuración para proporcionar la mejor calidad subjetiva.

## <a name="changes-in-monitor-state"></a>Cambios en el estado de supervisión

Un monitor puede cambiar los estados por diversos motivos, entre los que se incluyen:

-   El usuario cambia la configuración con los controles del panel frontal del monitor.
-   El usuario cambia la resolución de pantalla, la frecuencia de actualización o la profundidad de bits del monitor.
-   La aplicación usa las funciones de supervisión de bajo nivel para cambiar una configuración a la que no se puede acceder desde las funciones de alto nivel.
-   La aplicación llama [**a RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) [**o RestoreMonitorFactoryDefaults.**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults)

Todos estos eventos pueden cambiar la configuración del monitor. También pueden cambiar el valor mínimo y máximo de una configuración.

## <a name="dependencies-among-monitor-settings"></a>Dependencias entre monitores Configuración

Cambiar la temperatura del color puede cambiar la unidad actual y obtener la configuración, y lo contrario también es cierto. Estas son las únicas dependencias entre las funciones de configuración de supervisión de alto nivel. Es posible que solo se pueda acceder a otras configuraciones a través de las funciones de supervisión de bajo nivel. Puede haber dependencias entre esa configuración y la configuración de alto nivel. Estas dependencias son específicas del proveedor. Una aplicación puede controlar este problema de varias maneras:

-   Use solo funciones de alto nivel.
-   Después de llamar a una función de bajo nivel, obtenga el valor actual de cada configuración de monitor. Desafortunadamente, este enfoque puede ser lento, ya que obtener cada configuración tarda aproximadamente 40 milisegundos.
-   Use funciones de bajo nivel solo con modelos de supervisión específicos cuyo comportamiento comprenda.

## <a name="disabled-monitor-settings"></a>Monitor deshabilitado Configuración

Una aplicación no puede deshabilitar ninguna configuración de monitor llamando a las funciones de supervisión de alto nivel. Sin embargo, una aplicación podría deshabilitar accidentalmente una configuración si usa las funciones de bajo nivel para cambiar una configuración de monitor que no es compatible con las funciones de alto nivel. Además, un usuario podría deshabilitar una configuración mediante el control del panel frontal. Estos comportamientos son específicos del proveedor.

Si se deshabilita una configuración de monitor, cualquier función que establezca o recupere esa configuración producirá un error y establecerá el código del último error en ERROR \_ DISABLED \_ MONITOR \_ SETTING. Cuando esto sucede, la aplicación puede realizar una de las siguientes acciones:

-   Muestre un mensaje de error y sugiera al usuario que intente ajustar la configuración mediante el control del panel frontal.
-   Llame a [**la función RestoreMonitorFactoryDefaults.**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) Si un monitor tiene la marca de funcionalidadES MC \_ RESTORE \_ FACTORY \_ DEFAULTS ENABLES MONITOR SETTINGS, esta función habilita toda la configuración del monitor que admiten las funciones de \_ supervisión de alto \_ \_ nivel. Desafortunadamente, la función también restablece la configuración del monitor a su valor predeterminado de fábrica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la configuración de Monitor](using-monitor-configuration.md)
</dt> </dl>

 

 