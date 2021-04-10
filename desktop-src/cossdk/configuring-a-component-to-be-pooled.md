---
description: Puede configurar un componente para que se bloquee solo cuando se escribe correctamente para admitir que se agrupa. Para más información sobre estos requisitos, consulte requisitos de los objetos agrupables.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configuración de un componente que se va a agrupar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153469"
---
# <a name="configuring-a-component-to-be-pooled"></a>Configuración de un componente que se va a agrupar

Puede configurar un componente para que se bloquee solo cuando se escribe correctamente para admitir que se agrupa. Para más información sobre estos requisitos, consulte [requisitos de los objetos agrupables](requirements-for-poolable-objects.md).

> [!Note]  
> De forma predeterminada, un componente no está configurado para ser agrupado.

 

Al configurar un componente que se va a agrupar, puede especificar las siguientes propiedades para determinar cómo mantiene COM+ el Grupo:

-   **Tamaño mínimo del grupo.** Representa el número de objetos que se crean cuando se inicia la aplicación y el número mínimo de objetos que se mantienen en el grupo mientras la aplicación se está ejecutando. Si el número de objetos disponibles en el grupo cae por debajo del mínimo especificado, se crean nuevos objetos para cumplir cualquier solicitud de objeto pendiente y rellenar el grupo. Si el número de objetos disponibles en el grupo es mayor que el número mínimo, esos objetos excedentes se destruyen durante un ciclo de limpieza.
-   **Tamaño máximo del grupo.** Representa el número máximo de objetos agrupados que creará el administrador de agrupación, que los clientes usan activamente y que están inactivos en el grupo. Al crear objetos, el administrador de agrupación comprueba para comprobar que no se ha alcanzado el tamaño máximo del grupo y, si no lo ha hecho, el administrador del grupo crea una nueva instancia del objeto para dispensar al cliente. Si se ha alcanzado el tamaño máximo del grupo, las solicitudes de cliente se pondrán en cola y recibirán el primer objeto disponible del grupo en función del primer servido. Las solicitudes de creación de objetos agotarán el tiempo de espera después de un período especificado.
-   **Tiempo de espera de creación (MS).** Especifica cuánto tiempo esperará un cliente, en milisegundos, para que se devuelva un objeto desde el grupo después de una llamada a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Si la llamada de cliente no se realiza correctamente, se devuelve el tiempo de espera de error E \_ .

**Para establecer las propiedades relacionadas con la agrupación**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .

3.  Para habilitar la agrupación de objetos para el componente, active la casilla **habilitar agrupación de objetos** .

4.  En el cuadro **tamaño mínimo del grupo** , escriba el número mínimo de objetos de este tipo en el grupo. El grupo se mantendrá para tener al menos este número de objetos.

5.  En el cuadro u, escriba el número máximo de objetos de este tipo en el grupo. El número de objetos, tanto activados como desactivados, no superará nunca este valor.

6.  En el cuadro tiempo de **espera de creación (MS)** , escriba la cantidad de tiempo, en milisegundos, que un cliente esperará a un objeto agrupado si uno no está disponible inmediatamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión de estadísticas de objetos](monitoring-object-statistics.md)
</dt> </dl>

 

 
