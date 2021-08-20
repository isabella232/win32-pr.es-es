---
title: Directrices para servicios
description: Los servicios deben cumplir estas directrices para asegurarse de que el Administrador de reinicio puede apagar y reiniciar los servicios si es necesario para instalar las actualizaciones. Las aplicaciones pueden usar las directrices que se describen en Directrices para aplicaciones.
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6198da0d4f6f7887aaf37c858d98f3eb48e72c0d7722a1b5785a1cb280c96fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010143"
---
# <a name="guidelines-for-services"></a>Directrices para servicios

Los servicios deben cumplir estas directrices para asegurarse de que el Administrador de reinicio puede apagar y reiniciar los servicios si es necesario para instalar las actualizaciones. Las aplicaciones pueden usar las directrices que se describen en [Directrices para aplicaciones](guidelines-for-applications.md).

-   Los servicios deben ser capaces de apagarse y reiniciarse mediante [Service Control Manager](/windows/desktop/Services/service-control-manager) sin necesidad de reiniciar el sistema. Las excepciones a esta guía son procesos críticos del sistema que se ejecutan en el contexto de lsass.exe o services.exe.
-   El Administrador de reinicio respeta las dependencias del servicio. Cuando se cierra y reinicia un servicio, sus servicios dependientes se apagan y reinician.
-   Los servicios deben especificar el intervalo de recuperación y el período de restablecimiento en [el Administrador de control de servicios (SCM).](/windows/desktop/Services/service-control-manager) El intervalo de recuperación es el tiempo, en ms, después del último error que el SCM espera antes de realizar la acción de recuperación. El período de restablecimiento es el tiempo, en segundos, después del último error que el Administrador de control de servicios espera antes de restablecer el recuento de errores a 0. Los servicios pueden usar [**la función ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) para cambiar los valores de configuración.

    [Los](critical-system-services.md) servicios críticos deben usar la siguiente configuración de recuperación para especificar que el servicio se reinicie un minuto después del primer error al reiniciar el servicio, que se reinicie dos minutos después del segundo error y que el equipo se reinicie un minuto después del tercer error. El número de errores se restablece a 0 después de 300 segundos.

    <dl> Acciones de recuperación: Restart/60000/Restart/120000/Reboot/60000 & Reset =300  
    </dl>

    [Los servicios críticos](critical-system-services.md) deben iniciarse antes que los servicios no críticos. Los servicios que no son servicios críticos deben usar la siguiente configuración de recuperación para especificar que el servicio se reinicie dos minutos después del primer error al reiniciar el servicio. El servicio no se reinicia después del segundo error y un administrador tendría que intervenir en este caso. El número de errores se restablece en 0 después de 900 segundos.

    <dl> Acciones de recuperación: Restart/120000/Restart/300000/None/0 & Reset = 900  
    </dl>

 

 