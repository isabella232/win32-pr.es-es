---
description: Contiene información sobre la interfaz de programación del servicio de configuración inalámbrica rápida en Windows XP y Windows Server 2003.
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: Referencia de configuración inalámbrica cero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ebe202e16aa38fef617f382559f124772d50a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276702"
---
# <a name="wireless-zero-configuration-reference"></a>Referencia de configuración inalámbrica cero

\[La interfaz de programación de configuración inalámbrica cero ya no se admite en Windows Vista y Windows Server 2008. En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar. Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]

Esta sección contiene información sobre la interfaz de programación del servicio de configuración inalámbrica rápida en Windows XP y Windows Server 2003. Los temas incluyen:

-   [Funciones de configuración inalámbrica cero](wireless-zero-configuration-functions.md)
-   [Estructuras de configuración inalámbrica cero](wireless-zero-configuration-structures.md)

La configuración inalámbrica rápida es un servicio de Windows en Windows XP y Windows Server 2003 que se usa para configurar y administrar conexiones de red inalámbrica en un adaptador inalámbrico. El nombre del servicio para la configuración inalámbrica rápida es WZCSVC. En Windows XP, el nombre para mostrar del servicio WZCSVC es configuración inalámbrica rápida. En Windows Server 2003, el nombre para mostrar del servicio WZCSVC es configuración inalámbrica.

El servicio de configuración inalámbrica rápida se inicia normalmente en el momento del arranque. La interfaz de programación del servicio de configuración inalámbrica rápida solo se puede usar si se ha iniciado el servicio de configuración inalámbrica cero. Si no se inicia el servicio de configuración inalámbrica cero, las funciones de configuración de la conexión inalámbrica cero devolverán un error.

Para habilitar el servicio de configuración inalámbrica rápida para que se inicie automáticamente, vaya al botón **iniciar** . Seleccione la opción **configuración** y, a continuación, seleccione **Panel de control**. Si usa la vista de Windows XP, seleccione la categoría **rendimiento y mantenimiento** y, a continuación, seleccione **herramientas administrativas**. Si utiliza la vista clásica, seleccione **herramientas administrativas**. Haga clic en el icono **servicios** en el panel izquierdo. Haga clic en el icono configuración inalámbrica de cero en el panel derecho y cambie el **tipo de inicio** Dropbox a **automático**. Esta configuración establecerá el servicio para que se inicie automáticamente durante el arranque. A continuación, haga clic en el botón **iniciar** para iniciar el servicio de configuración inalámbrica cero inalámbrica cero y haga clic en el botón **Aceptar** .

La configuración inalámbrica rápida también se puede iniciar y detener desde un símbolo del sistema. Para iniciar la configuración de la conexión inalámbrica de cero, ejecute el siguiente comando:

**net start wzcsvc**

Para detener la configuración de la conexión inalámbrica de cero, ejecute el siguiente comando:

**net stop wzcsvc**

 

 



