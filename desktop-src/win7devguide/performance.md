---
title: Rendimiento (Windows 7 Developer Guide)
description: Windows 7 maximiza la eficiencia energética y la escalabilidad del hardware, a la vez que mantiene un alto rendimiento.
ms.assetid: db48aa8f-749e-4a56-8a91-ac9b81d6e8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5636b6cb7178fa660381196f44b811c905478c1bcd31e0580ea631955b13c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032062"
---
# <a name="performance-windows-7-developer-guide"></a>Rendimiento (Windows 7 Developer Guide)

Windows 7 maximiza la eficiencia energética y la escalabilidad del hardware, a la vez que mantiene un alto rendimiento. La eficiencia energética se mejora a través de una actividad en segundo plano reducida y una nueva compatibilidad con el desencadenador que inicia los servicios del sistema. Windows 7 también ofrece mejoras en el kernel de Windows que permiten que las aplicaciones y los servicios se escalen de forma eficaz entre plataformas. El rendimiento de muchas características y API se ha mejorado en Windows 7 frente a Windows Vista. Por ejemplo, el rendimiento del controlador en los servidores se optimiza mediante nuevas API de topología en modo de usuario y modo kernel. La representación de gráficos es considerablemente más fluida y rápida. El rendimiento de accesibilidad también es significativamente más rápido que antes.

## <a name="building-power-efficient-applications"></a>Creación de Power-Efficient aplicaciones

La creación de aplicaciones de bajo consumo que aprovechan las tecnologías de administración de energía más recientes es un desafío importante al que se enfrentan los desarrolladores en la actualidad. Normalmente, los fabricantes de procesadores y dispositivos obtienen toda la atención a medida que se miden y comparan sus ofertas más recientes. Sin embargo, una sola aplicación puede impedir fácilmente que la última generación de hardware se dé cuenta de su potencial de eficiencia energética. Por ejemplo, una sola aplicación que aumenta la resolución del temporizador de plataforma puede reducir la duración de la batería en un 10 %.

El funcionamiento extendido de la energía de la batería y el uso de tecnologías de bajo consumo son requisitos clave para los desarrolladores actuales. Windows 7 reduce en gran medida el número de actividades que realiza el sistema operativo que impiden el uso de modos de ahorro de energía. También admite el inicio del desencadenador de los servicios del sistema para permitir que los procesadores se vuelvan inactivos con más frecuencia y permanezcan inactivos durante más tiempo, lo que reduce el consumo de energía. Además, Windows 7 aprovecha el hardware de bajo consumo más reciente, incluidos adaptadores de red, dispositivos de almacenamiento y tarjetas gráficas.

Windows 7 proporciona la infraestructura y las herramientas que permiten a los desarrolladores determinar fácilmente el impacto energético de sus aplicaciones. Un conjunto de devoluciones de llamada de eventos permite a las aplicaciones reducir su actividad cuando el sistema está con batería y escalar verticalmente automáticamente cuando el sistema está encendido *por ca.* En el caso de las aplicaciones que implican un proceso o servicio en segundo plano, Windows 7 ofrece una nueva infraestructura para habilitar automáticamente las tareas en segundo plano cuando sea más adecuado con el fin de maximizar la eficiencia energética. (Vea [WHDC Performance Central](https://www.microsoft.com/whdc/system/sysperf/default.mspx) and Power Management en información general Windows [7).](https://www.climatesaverscomputing.org/wordpress/wp-content/uploads/2011/06/Power_Management_in_Windows_7_Overview.pdf)

## <a name="service-control-manager"></a>Administrador de control de servicios

El Windows 7Service Control Manager (SCM) se ha ampliado para que un servicio se pueda iniciar y detener automáticamente cuando se produzca un evento o desencadenador del sistema específico en el sistema. Las funcionalidades de inicio del desencadenador eliminan la necesidad de que los servicios se inicien automáticamente al iniciar el equipo y, a continuación, sondeen o esperen a que se produzca un evento, como la llegada del dispositivo. Los eventos de desencadenador comunes para los servicios incluyen:

-   Llegada de la interfaz de clase de dispositivo: inicie un servicio solo cuando un determinado tipo de dispositivo esté presente o conectado en el sistema.
-   Unión a un dominio: inicie un servicio solo si el sistema está unido a un dominio Windows dominio.
-   Cambio de directiva de grupo: inicie un servicio automáticamente cuando las directivas de grupo se actualicen en el sistema.
-   Llegada de la dirección IP: inicie un servicio solo cuando el sistema esté conectado a la red.

Los desarrolladores de software pueden usar los tipos de desencadenador predefinidos para Windows 7 y las opciones de configuración para habilitar la funcionalidad de inicio del desencadenador. El Windows 7SCM expone un nuevo conjunto de API que permiten a un servicio registrarse para eventos de desencadenador personalizados específicos. (Consulte [Administrador de control de servicios).](../services/service-control-manager.md)

## <a name="windows-troubleshooting-platform"></a>Plataforma de solución de problemas de Windows

Windows 7 ofrece una plataforma de solución de problemas completa y extensible que usa un mecanismo basado en PowerShell para solucionar problemas. Los componentes clave de la plataforma de solución de problemas incluyen un paquete de solución de problemas, un motor de solución de problemas y el Asistente para solución de problemas. El paquete de solución de problemas es una colección de scripts de PowerShell y metadatos pertinentes. El motor de solución de problemas inicia un runtime de PowerShell para ejecutar un paquete de solución de problemas y expone un conjunto de interfaces para controlar la ejecución del paquete de solución de problemas.

El Asistente para la solución de problemas proporciona una experiencia coherente entre los paquetes de solución de problemas, que se comunica con el motor de solución de problemas para solucionar los problemas especificados en un paquete de solución de problemas. La ejecución de un paquete de solución de problemas también se puede controlar a través de un conjunto de *commandlets de* PowerShell .

La plataforma de solución de problemas se integra perfectamente con el Centro de soluciones de Windows 7PC, lo que permite que otras aplicaciones ejecuten diagnósticos de forma similar como parte de su administración de equipos. Los profesionales de TI pueden configurar la plataforma de solución de problemas a través de *directiva de grupo* para su uso dentro de la empresa, y también hay disponible un Toolkit de solución de problemas de Windows que permite a los desarrolladores crear paquetes de solución de problemas. (Consulte [Windows de solución de problemas).](/previous-versions/windows/desktop/wintt/windows-troubleshooting-toolkit-portal)

![solución de problemas de la interfaz de usuario de la plataforma](images/windows7-devguide-troubleshoot.jpg)

La plataforma de solución de problemas se integra perfectamente con el Centro de soluciones Windows 7PC

 

 
