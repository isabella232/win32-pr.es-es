---
description: Contiene información sobre la interfaz de programación para el servicio configuración inalámbrica cero en Windows XP y Windows Server 2003.
ms.assetid: cd9e8fc0-0a65-4654-95aa-201751183521
title: Referencia de configuración inalámbrica de cero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358ff3727edc34d4a5de0f4195895cf02b4596722aecd5849f4e35b9991dbe88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684438"
---
# <a name="wireless-zero-configuration-reference"></a>Referencia de configuración inalámbrica de cero

\[La interfaz de programación configuración inalámbrica cero ya no se admite a partir de Windows Vista y Windows Server 2008. En su lugar, use [la API Wi-Fi nativa,](native-wifi-reference.md)que proporciona una funcionalidad similar. Para obtener más información, vea [Acerca de la API Wi-Fi nativa.](about-the-native-wifi-api.md)\]

Esta sección contiene información sobre la interfaz de programación del servicio Wireless Zero Configuration en Windows XP y Windows Server 2003. Los temas incluyen:

-   [Funciones de configuración inalámbrica cero](wireless-zero-configuration-functions.md)
-   [Estructuras de configuración inalámbricas de cero](wireless-zero-configuration-structures.md)

Configuración cero inalámbrica es un servicio Windows en Windows XP y Windows Server 2003 que se usa para configurar y administrar conexiones de red inalámbricas en un adaptador inalámbrico. El nombre del servicio de configuración inalámbrica cero es WZCSVC. En Windows XP, el nombre para mostrar del servicio WZCSVC es Configuración inalámbrica cero. En Windows Server 2003, el nombre para mostrar del servicio WZCSVC es Configuración inalámbrica.

El servicio configuración inalámbrica cero se inicia normalmente en el momento del arranque. La interfaz de programación para el servicio Configuración inalámbrica cero solo se puede usar si se ha iniciado el servicio Configuración inalámbrica cero. Si no se inicia el servicio configuración inalámbrica cero, las funciones configuración inalámbrica cero devolverán un error.

Para habilitar el servicio configuración inalámbrica cero para que se inicie automáticamente, vaya al **botón** Iniciar. Seleccione la **Configuración** y, a continuación, **seleccione Panel de control**. Si usa la vista Windows XP, seleccione la categoría Rendimiento y **mantenimiento** y, a continuación, **herramientas administrativas**. Si usa la vista clásica, seleccione **Herramientas administrativas.** Haga clic **en el icono** Servicios en el panel izquierdo. Haga clic en el icono Configuración inalámbrica de cero en el panel derecho y cambie el cuadro desplegable **Tipo** de inicio a **Automático.** Esta configuración establecerá el servicio para que se inicie automáticamente en el momento del arranque. A continuación, haga clic **en** el botón Iniciar para iniciar el servicio Wireless Zero Wireless Zero Configuration y haga clic **en el botón** Aceptar.

La configuración inalámbrica cero también se puede iniciar y detener desde un símbolo del sistema. Para iniciar la configuración inalámbrica de cero, ejecute el siguiente comando:

**net start wzcsvc**

Para detener la configuración inalámbrica de cero, ejecute el siguiente comando:

**net stop wzcsvc**

 

 



