---
title: Directrices para servicios
description: Los servicios deben cumplir estas directrices para asegurarse de que el administrador de reinicio puede apagar y reiniciar los servicios si es necesario para instalar las actualizaciones. Las aplicaciones pueden usar las directrices que se describen en directrices para las aplicaciones.
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51374c0a4c6fc561b8259aadf15e3d5487e12483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078093"
---
# <a name="guidelines-for-services"></a>Directrices para servicios

Los servicios deben cumplir estas directrices para asegurarse de que el administrador de reinicio puede apagar y reiniciar los servicios si es necesario para instalar las actualizaciones. Las aplicaciones pueden usar las directrices que se describen en [directrices para las aplicaciones](guidelines-for-applications.md).

-   Los servicios deben ser capaces de cerrarse y reiniciarse con el [Administrador de control de servicios](/windows/desktop/Services/service-control-manager) sin necesidad de reiniciar el sistema. Las excepciones a esta directriz son los procesos críticos del sistema que se ejecutan en el contexto de lsass.exe o services.exe.
-   El administrador de reinicio respeta las dependencias de servicio. Cuando un servicio se cierra y se reinicia, sus servicios dependientes se apagan y se reinician.
-   Los servicios deben especificar el intervalo de recuperación y el período de restablecimiento en el [Administrador de control de servicios (SCM)](/windows/desktop/Services/service-control-manager). El intervalo de recuperación es el tiempo, en milisegundos, después del último error que el SCM espera antes de realizar la acción de recuperación. El período de restablecimiento es el tiempo, en segundos, después del último error que el administrador de control de servicios espera antes de restablecer el recuento de errores a 0. Los servicios pueden usar la función [**ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) para cambiar los valores de configuración.

    Los [servicios críticos](critical-system-services.md) deben usar la siguiente configuración de recuperación para especificar que el servicio se reinicie un minuto después del primer error al reiniciar el servicio, se reinicie dos minutos después del segundo error y que el equipo se reinicie un minuto después del tercer error. El recuento de errores se restablece en 0 después de 300 segundos.

    <dl> Acciones de recuperación: restart/60000/restart/120000/reboot/60000 & RESET = 300  
    </dl>

    Los [servicios críticos](critical-system-services.md) deben iniciarse antes que los servicios no críticos. Los servicios que no son críticos deben usar la siguiente configuración de recuperación para especificar que el servicio se reinicie dos minutos después del primer error al reiniciar el servicio. El servicio no se reinicia después del segundo error y es necesario que un administrador intervenga en este caso. El recuento de errores se restablece en 0 después de 900 segundos.

    <dl> Acciones de recuperación: restart/120000/restart/300000/None/0 & RESET = 900  
    </dl>

 

 