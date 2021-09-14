---
description: Puede configurar un componente para que se relame solo cuando se escriba correctamente para admitir la agrupación. Para más información sobre estos requisitos, consulte Requisitos para objetos agrupables.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configuración de un componente que se va a agrupar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358915"
---
# <a name="configuring-a-component-to-be-pooled"></a>Configuración de un componente que se va a agrupar

Puede configurar un componente para que se relame solo cuando se escriba correctamente para admitir la agrupación. Para obtener más información sobre estos requisitos, vea [Requirements for Poolable Objects](requirements-for-poolable-objects.md).

> [!Note]  
> De forma predeterminada, un componente no está configurado para estar agrupado.

 

Al configurar un componente que se va a agrupar, puede especificar las siguientes propiedades para determinar cómo com+ mantiene el grupo:

-   **Tamaño mínimo del grupo.** Representa el número de objetos que se crean cuando se inicia la aplicación y el número mínimo de objetos que se mantienen en el grupo mientras se ejecuta la aplicación. Si el número de objetos disponibles en el grupo cae por debajo del mínimo especificado, se crean nuevos objetos para satisfacer las solicitudes de objetos pendientes y rellenar el grupo. Si el número de objetos disponibles en el grupo es mayor que el número mínimo, esos objetos sobrantes se destruyen durante un ciclo de limpieza.
-   **Tamaño máximo del grupo.** Representa el número máximo de objetos agrupados que creará el administrador de agrupación, tanto usados activamente por los clientes como inactivos en el grupo. Al crear objetos, el administrador de agrupación comprueba que no se ha alcanzado el tamaño máximo del grupo y, si no lo ha hecho, el administrador del grupo crea una nueva instancia del objeto para prescindir del cliente. Si se ha alcanzado el tamaño máximo del grupo, las solicitudes de cliente se pondrán en cola y recibirán el primer objeto disponible del grupo por primera vez. Las solicitudes de creación de objetos se pondrán en espera después de un período especificado.
-   **Tiempo de espera de creación (ms).** Especifica cuánto tiempo esperará un cliente, en milisegundos, a que se devuelva un objeto del grupo después de una llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Si la llamada de cliente no se realiza correctamente, se devuelve el error E \_ TIMEOUT.

**Para establecer propiedades relacionadas con la agrupación**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón derecho en el componente que desea configurar y, a continuación, haga clic en **Propiedades**.

2.  En el cuadro de diálogo Propiedades del componente, haga clic en **la pestaña** Activación.

3.  Para habilitar la agrupación de objetos para el componente, active **la casilla Habilitar agrupación** de objetos.

4.  En el **cuadro Tamaño mínimo del** grupo, escriba el número mínimo de objetos de este tipo en el grupo. El grupo se mantendrá para tener al menos este número de objetos.

5.  En el cuadro u, escriba el número máximo de objetos de este tipo en el grupo. El número de objetos, activados y desactivados, nunca superará este valor.

6.  En el cuadro Tiempo de espera de creación **(ms),** escriba la cantidad de tiempo, en milisegundos, que un cliente esperará un objeto agrupado si no hay uno disponible inmediatamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de estadísticas de objetos](monitoring-object-statistics.md)
</dt> </dl>

 

 
