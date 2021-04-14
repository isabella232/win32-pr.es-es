---
title: Rendimiento (guía para desarrolladores de Windows 7)
description: Windows 7 maximiza la eficiencia y escalabilidad de la energía del hardware, al tiempo que mantiene un alto rendimiento.
ms.assetid: db48aa8f-749e-4a56-8a91-ac9b81d6e8c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752f66e80265bf7d6b3ea26e7baabdc6550ce921
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359586"
---
# <a name="performance-windows-7-developer-guide"></a>Rendimiento (guía para desarrolladores de Windows 7)

Windows 7 maximiza la eficiencia y escalabilidad de la energía del hardware, al tiempo que mantiene un alto rendimiento. La eficacia energética se mejora a través de la actividad en segundo plano reducida y la nueva compatibilidad para el desencadenador que inicia los servicios del sistema. Windows 7 también ofrece mejoras en el kernel de Windows que permiten escalar eficazmente las aplicaciones y los servicios entre plataformas. El rendimiento de muchas características y API se ha mejorado en Windows 7 frente a Windows Vista. Por ejemplo, el rendimiento del controlador en servidores está optimizado por las nuevas API de topología en modo de kernel y usuario. La representación de gráficos es considerablemente más suave y más rápida. El rendimiento de accesibilidad también es significativamente más rápido que antes.

## <a name="building-power-efficient-applications"></a>Compilar aplicaciones Power-Efficient

La creación de aplicaciones de eficacia energética que aprovechan las tecnologías de administración de energía más recientes es un reto importante que los desarrolladores enfrentan hoy en día. Normalmente, los fabricantes de procesadores y dispositivos reciben toda la atención, ya que sus ofertas más recientes se miden y se comparan. Sin embargo, una sola aplicación puede evitar fácilmente que la última generación de hardware pueda hacer realidad su potencial de eficiencia energética. Por ejemplo, una sola aplicación que aumenta la resolución del temporizador de la plataforma puede reducir la duración de la batería en un 10 por ciento.

La operación extendida con la alimentación de la batería y el uso de tecnologías de eficacia energética son requisitos clave para los desarrolladores de hoy en día. Windows 7 reduce en gran medida el número de actividades que realiza el sistema operativo, lo que impide el uso de los modos de ahorro de energía. También admite el desencadenador: Inicio de servicios del sistema para permitir que los procesadores se queden inactivos más a menudo y permanezcan inactivos más tiempo, lo que reduce el consumo de energía. Además, Windows 7 aprovecha el hardware más eficaz de energía, incluidos los adaptadores de red, los dispositivos de almacenamiento y las tarjetas gráficas.

Windows 7 proporciona la infraestructura y las herramientas que facilitan a los desarrolladores la determinación del impacto energético de sus aplicaciones. Un conjunto de devoluciones de llamada de eventos permite a las aplicaciones reducir su actividad cuando el sistema funciona con batería y escalar verticalmente de forma automática cuando el sistema está en corriente *alterna* . En el caso de las aplicaciones que implican un proceso o un servicio en segundo plano, Windows 7 ofrece una nueva infraestructura para habilitar automáticamente las tareas en segundo plano cuando sea más adecuada con el fin de maximizar la eficiencia energética. (Consulte [whdc performance central](https://www.microsoft.com/whdc/system/sysperf/default.mspx) and [Power Management in Windows 7 Overview](https://www.climatesaverscomputing.org/wordpress/wp-content/uploads/2011/06/Power_Management_in_Windows_7_Overview.pdf)).

## <a name="service-control-manager"></a>Administrador de control de servicios

El administrador de control de 7Service (SCM) de Windows se ha ampliado para que un servicio se pueda iniciar automáticamente y detenerse cuando se produzca un evento del sistema o un desencadenador específico en el sistema. Las funcionalidades de inicio de desencadenador eliminan la necesidad de que los servicios se inicien automáticamente al iniciarse el equipo y, a continuación, sondean o esperan a que se produzca un evento, como la llegada del dispositivo. Los eventos de desencadenadores comunes para los servicios incluyen:

-   Llegada de la interfaz de clase de dispositivo: inicia un servicio solo cuando un determinado tipo de dispositivo está presente o conectado en el sistema.
-   Unión a un dominio: inicie un servicio solo si el sistema está unido a un dominio de Windows.
-   Cambio de directiva de Grupo: inicia un servicio automáticamente cuando se actualizan las directivas de grupo en el sistema.
-   Llegada de dirección IP: inicie un servicio solo cuando el sistema esté conectado a la red.

Los desarrolladores de software pueden usar los tipos de desencadenadores predefinidos para Windows 7 y las opciones de configuración para habilitar la funcionalidad de inicio de desencadenador. Windows 7SCM expone un nuevo conjunto de API que permiten que un servicio se registre para eventos de desencadenadores personalizados específicos. (Consulte [Administrador de control de servicios](../services/service-control-manager.md)).

## <a name="windows-troubleshooting-platform"></a>Plataforma de solución de problemas de Windows

Windows 7 ofrece una plataforma de solución de problemas completa y extensible que usa un mecanismo basado en PowerShell para solucionar problemas y resolverlos. Los componentes clave de la plataforma de solución de problemas incluyen un paquete de solución de problemas, un motor de solución de problemas y el Asistente para solución de problemas. El módulo de solución de problemas es una colección de scripts de PowerShell y metadatos pertinentes. El motor de solución de problemas inicia un entorno de ejecución de PowerShell para ejecutar un módulo de solución de problemas y expone un conjunto de interfaces para controlar la ejecución del paquete de solución de problemas.

El Asistente para solución de problemas proporciona una experiencia coherente en todos los paquetes de solución de problemas, que se comunica con el motor de solución de problemas para solucionar problemas y resolver los que se especifican en un paquete de solución de problemas. La ejecución de un paquete de solución de problemas también se puede controlar mediante un conjunto de *commandlets* de PowerShell.

La plataforma de solución de problemas se integra perfectamente con el centro de soluciones de Windows 7PC, lo que permite a otras aplicaciones ejecutar diagnósticos de forma similar como parte de su régimen de administración de equipos. Los profesionales de TI pueden configurar la plataforma de solución de problemas a través de *Directiva de grupo* para su uso en la empresa, y también hay disponible un kit de herramientas de solución de problemas de Windows que permite a los desarrolladores crear paquetes de solución de problemas. (Consulte [plataforma de solución de problemas de Windows](/previous-versions/windows/desktop/wintt/windows-troubleshooting-toolkit-portal)).

![solución de problemas de UI de plataforma](images/windows7-devguide-troubleshoot.jpg)

La plataforma de solución de problemas se integra perfectamente con el centro de soluciones de Windows 7PC

 

 
