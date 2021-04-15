---
title: Uso de las funciones de configuración del monitor de High-Level
description: Uso de las funciones de configuración del monitor de High-Level
ms.assetid: 23e5d45d-a924-4119-b21d-b24764b53a94
keywords:
- supervisión, funciones
- supervisión, funciones de configuración de alto nivel
- supervisar, enumerar monitores físicos
- monitor, configuración continua
- supervisión de la configuración y las funciones de configuración de alto nivel
- supervisión de la configuración, funciones
- configuración del monitor, enumeración de monitores físicos
- configuración de supervisión, configuración continua
- enumerar monitores físicos
- funciones de configuración de alto nivel
- configuración del monitor continuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff494388aac91d8aacd92ed4fe345722ea18659f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665803"
---
# <a name="using-the-high-level-monitor-configuration-functions"></a>Uso de las funciones de configuración del monitor de High-Level

## <a name="enumerating-physical-monitors"></a>Enumerar monitores físicos

Hay varias funciones que enumeran los dispositivos de visualización, incluidos [**EnumDisplayMonitors**](/windows/desktop/api/winuser/nf-winuser-enumdisplaymonitors) y [**MonitorFromWindow**](/windows/desktop/api/winuser/nf-winuser-monitorfromwindow). Estas funciones están documentadas en la documentación de GDI de Windows, en el tema [monitores de varias pantallas](/windows/desktop/gdi/multiple-display-monitors). Estas funciones devuelven los identificadores de **HMONITOR** . Sin embargo, a pesar del nombre, un identificador de **HMONITOR** se puede asociar a más de un monitor físico. Para configurar las opciones de un monitor, la aplicación debe obtener un identificador único para el monitor físico llamando a [**GetPhysicalMonitorsFromHMONITOR**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromhmonitor).

Si la aplicación usa Direct3D, puede obtener un identificador de monitor desde un dispositivo Direct3D llamando a [**GetPhysicalMonitorsFromIDirect3DDevice9**](/windows/desktop/api/PhysicalMonitorEnumerationAPI/nf-physicalmonitorenumerationapi-getphysicalmonitorsfromidirect3ddevice9).

## <a name="supported-functions"></a>Funciones admitidas

Es posible que un monitor no admita todas las funciones de configuración del monitor. Para averiguar qué funciones admite un monitor, llame a [**GetMonitorCapabilities**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-getmonitorcapabilities).

## <a name="continuous-monitor-settings"></a>Configuración del monitor continuo

Una configuración de monitor *continuo* es aquella que puede oscilar entre algunos valores mínimo y máximo. La mayoría de las funciones de configuración del monitor de alto nivel controlan la configuración del monitor continuo. Por ejemplo, el brillo y el contraste son valores continuos.

La configuración del monitor continuo no tiene unidades del mundo real definidas. Las unidades son arbitrarias y pueden variar de un fabricante a otro. Si dos monitores tienen el mismo valor de brillo, por ejemplo, un monitor podría parecer mucho más brillante que otro. Normalmente, una aplicación presentará controles deslizantes o controles de flechas al usuario. A continuación, el usuario puede ajustar la configuración para proporcionar la mejor calidad subjetiva.

## <a name="changes-in-monitor-state"></a>Cambios en el estado del monitor

Un monitor puede cambiar Estados por diversos motivos, entre los que se incluyen:

-   El usuario cambia la configuración con los controles del panel frontal del monitor.
-   El usuario cambia la resolución de pantalla, la frecuencia de actualización o la profundidad de bits del monitor.
-   La aplicación usa las funciones de monitor de bajo nivel para cambiar una configuración que no es accesible desde las funciones de alto nivel.
-   La aplicación llama a [**RestoreMonitorFactoryColorDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorycolordefaults) o [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults).

Todos estos eventos pueden cambiar la configuración del monitor. También pueden cambiar el valor mínimo y máximo de un valor de configuración.

## <a name="dependencies-among-monitor-settings"></a>Dependencias entre la configuración del monitor

Cambiar la temperatura del color puede cambiar la unidad actual y obtener la configuración, y también se aplica el valor REVERSE. Estas son las únicas dependencias entre las funciones de configuración del monitor de alto nivel. Otras opciones de configuración solo pueden ser accesibles a través de las funciones de monitor de bajo nivel. Puede haber dependencias entre esos valores y la configuración de alto nivel. Estas dependencias son específicas del proveedor. Una aplicación puede controlar este problema de varias maneras:

-   Use solo funciones de alto nivel.
-   Después de llamar a una función de bajo nivel, obtenga el valor actual de cada valor de monitor. Desafortunadamente, este enfoque puede ser lento, ya que la obtención de cada configuración tarda aproximadamente 40 milisegundos.
-   Use funciones de bajo nivel solo con modelos de monitor concretos cuyo comportamiento entienda.

## <a name="disabled-monitor-settings"></a>Configuración de monitor deshabilitada

Una aplicación no puede deshabilitar ninguna configuración de monitor mediante una llamada a las funciones de supervisión de alto nivel. Sin embargo, una aplicación podría deshabilitar accidentalmente un valor si usa las funciones de bajo nivel para cambiar una configuración de monitor que no es compatible con las funciones de alto nivel. Además, un usuario podría deshabilitar una configuración mediante el control de panel frontal. Estos comportamientos son específicos del proveedor.

Si se deshabilita la configuración de un monitor, cualquier función que establezca o recupere esa configuración producirá un error y establecerá el último código de error en ERROR \_ deshabilitado \_ \_ . Cuando esto ocurre, la aplicación puede realizar una de las siguientes acciones:

-   Muestre un mensaje de error y sugiera al usuario que intente ajustar la configuración mediante el control de panel frontal.
-   Llame a la función [**RestoreMonitorFactoryDefaults**](/windows/desktop/api/HighLevelMonitorConfigurationAPI/nf-highlevelmonitorconfigurationapi-restoremonitorfactorydefaults) . Si un monitor tiene los \_ \_ valores predeterminados del Factory de restauración de MC habilita la marca de capacidades de \_ \_ \_ supervisión de la \_ configuración, esta función habilita todas las opciones de supervisión admitidas por las funciones de supervisión de alto nivel. Desafortunadamente, la función también restablece la configuración del monitor a su valor predeterminado de fábrica.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la configuración de monitor](using-monitor-configuration.md)
</dt> </dl>

 

 