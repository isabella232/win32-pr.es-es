---
description: Se recomienda que todas las suscripciones permanentes se compilen en el espacio de nombres de la \\ \\ suscripción raíz.
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: Implementación de suscripciones de eventos permanentes entre espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52771e40d4dfb036354c3b37b562b32edd3034ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716559"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a>Implementación de suscripciones de eventos permanentes entre espacios de nombres

Se recomienda que todas las suscripciones permanentes se compilen en el espacio de nombres de la \\ \\ suscripción raíz. Esto evita la necesidad de compilar el consumidor permanente en cada espacio de nombres que se está usando, lo que significa que solo hay un espacio de nombres para buscar suscripciones permanentes. Use la propiedad **EventNamespace** de [**\_ \_ EventFilter**](--eventfilter.md) para implementar una suscripción entre espacios de nombres.

Cuando se usa [**CommandLineEventConsumer**](commandlineeventconsumer.md), es importante proteger el archivo ejecutable que se está iniciando. Si el archivo ejecutable no está en una ubicación segura o está protegido con una lista de control de acceso (ACL) segura, cualquiera puede reemplazar el ejecutable por uno propio. Para obtener más información acerca de las ACL, vea [crear un descriptor de seguridad para un nuevo objeto en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

En el siguiente ejemplo de código de Managed Object Format (MOF) se muestra una suscripción entre espacios de nombres.

``` syntax
#pragma namespace("\\root\\subscription")

instance of __EventFilter as $FLT
{
  Name = "Filter";
  Query = "SELECT * FROM __InstanceModificationEvent "
          "WHERE TargetInstance ISA \"Win32_LocalTime\" "
          "AND TargetInstance.Hour = 8 "
          "AND TargetInstance.Minute = 0 "
          "AND TargetInstance.Second = 0 "
          "AND TargetInstance.DayOfWeek = 6";
  QueryLanguage = "WQL";
  EventNamespace = "root\\cimv2";
};

instance of CommandLineEventConsumer as $CONS
{
  ExecutablePath = "cmd.exe";
  ShowWindowCommand = 7;
  RunInteractively = true;
};

instance of __FilterToConsumerBinding
{
  Consumer = $CONS;
  Filter = $FLT;
};
```

 

 
