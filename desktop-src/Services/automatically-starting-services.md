---
description: Durante el arranque del sistema, el SCM inicia todos los servicios de inicio automático y los servicios de los que dependen. Por ejemplo, si un servicio de inicio automático depende de un servicio de inicio de petición, el servicio de inicio de petición también se inicia automáticamente.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Inicio automático de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666349"
---
# <a name="automatically-starting-services"></a>Inicio automático de servicios

Durante el arranque del sistema, el SCM inicia todos los servicios de inicio automático y los servicios de los que dependen. Por ejemplo, si un servicio de inicio automático depende de un servicio de inicio de petición, el servicio de inicio de petición también se inicia automáticamente.

El orden de carga está determinado por lo siguiente:

1.  El orden de los grupos en la lista de grupos de orden de carga. Esta información se almacena en el valor **ServiceGroupOrder** en la siguiente clave del registro:

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control**

    Para especificar el grupo de pedidos de carga para un servicio, use el parámetro *lpLoadOrderGroup* de la función [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) o [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .

2.  El orden de los servicios dentro de un grupo especificado en el vector de orden de las etiquetas. Esta información se almacena en el valor **GroupOrderList** en la siguiente clave del registro:

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control**

3.  Las dependencias enumeradas para cada servicio.

Una vez completado el arranque, el sistema ejecuta el programa de comprobación de arranque especificado por el valor **BootVerificationProgram** de la siguiente clave del registro: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control**.

De manera predeterminada, este valor no está establecido. El sistema simplemente informa de que el arranque se realizó correctamente después de que el primer usuario haya iniciado sesión. Puede proporcionar un programa de comprobación de arranque que compruebe si hay problemas en el sistema e informa del estado de arranque al SCM mediante la función [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus) .

Después de un arranque correcto, el sistema guarda un clon de la base de datos en la última configuración buena conocida (válida conocida). El sistema puede restaurar esta copia de la base de datos si los cambios realizados en la base de datos activa provocan un error en el reinicio del sistema. A continuación se encuentra la clave del registro para esta base de datos:

**HKEY \_ local \_ Machine \\ System \\ ControlSet *XXX* \\ Services**

donde *XXX* es el valor que se guarda en el siguiente valor del registro: **HKEY \_ local \_ Machine \\ System \\ SELECT \\ LastKnownGood**.

Si no se puede iniciar un servicio de inicio automático con un error de servicio \_ \_ crítico nivel de control de errores, el SCM reinicia el equipo con la configuración de válida conocida. Si ya se usa la configuración válida conocida, se produce un error en el arranque.

Un servicio de inicio automático se puede configurar como un servicio de inicio automático retrasado mediante una llamada a la función [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) con la \_ información de \_ Inicio automático retrasada de la configuración del servicio \_ \_ \_ . Este cambio surte efecto después del siguiente arranque del sistema. Para obtener más información, [**vea \_ \_ información de \_ Inicio \_ automático retrasado del servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).

 

 



