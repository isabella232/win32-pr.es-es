---
description: Durante el arranque del sistema, el SCM inicia todos los servicios de inicio automático y los servicios de los que dependen. Por ejemplo, si un servicio de inicio automático depende de un servicio de inicio a petición, el servicio de inicio a petición también se inicia automáticamente.
ms.assetid: 8aa60e96-a35e-4670-832c-c045d0903618
title: Inicio automático de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b2e7ef0c65e72ee21145891b6f9598117a7afe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265087"
---
# <a name="automatically-starting-services"></a>Inicio automático de servicios

Durante el arranque del sistema, el SCM inicia todos los servicios de inicio automático y los servicios de los que dependen. Por ejemplo, si un servicio de inicio automático depende de un servicio de inicio a petición, el servicio de inicio a petición también se inicia automáticamente.

El orden de carga viene determinado por lo siguiente:

1.  El orden de los grupos en la lista de grupos de ordenación de carga. Esta información se almacena en el **valor ServiceGroupOrder** en la siguiente clave del Registro:

    **HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ (Control)**

    Para especificar el grupo de ordenación de carga para un servicio, use el parámetro *lpLoadOrderGroup* de la [**función CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) [**o ChangeServiceConfig.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)

2.  El orden de los servicios dentro de un grupo especificado en el vector de orden de etiquetas. Esta información se almacena en el **valor GroupOrderList** de la siguiente clave del Registro:

    **HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ (Control)**

3.  Dependencias enumeradas para cada servicio.

Una vez completado el arranque, el sistema ejecuta el programa de comprobación de arranque especificado por el valor **BootVerificationProgram** de la siguiente clave del Registro: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control**.

De manera predeterminada, este valor no está establecido. El sistema simplemente informa de que el arranque se ha realizado correctamente después de que el primer usuario haya iniciado sesión. Puede proporcionar un programa de comprobación de arranque que comprueba si hay problemas en el sistema e informa del estado de arranque al SCM mediante la [**función NotifyBootConfigStatus.**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)

Después de un arranque correcto, el sistema guarda un clon de la base de datos en la última configuración conocida correcta (L PX). El sistema puede restaurar esta copia de la base de datos si los cambios realizados en la base de datos activa provocan un error en el reinicio del sistema. A continuación se muestra la clave del Registro para esta base de datos:

**HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ ControlSet *XXX* \\ Services**

donde *XXX* es el valor guardado en el siguiente valor del Registro: HKEY LOCAL MACHINE System (Sistema de máquina **local de HKEY), \_ seleccione \_ \\ \\ \\ LastKnownKnown (Últimoconscenario).**

Si no se puede iniciar un servicio de inicio automático con un nivel de control error CRÍTICO DE ERROR DE SERVICIO, el SCM reinicia el equipo mediante \_ \_ la configuración de LNTES. Si ya se está utilizando la configuración L PX, se produce un error en el arranque.

Un servicio de inicio automático se puede configurar como un servicio de inicio automático retrasado mediante una llamada a la función [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) con SERVICE \_ CONFIG \_ DELAYED \_ AUTO START \_ \_ INFO. Este cambio entra en vigor después del siguiente arranque del sistema. Para obtener más información, [**vea SERVICE \_ DELAYED AUTO START \_ \_ \_ INFO**](/windows/desktop/api/Winsvc/ns-winsvc-service_delayed_auto_start_info).

 

 



