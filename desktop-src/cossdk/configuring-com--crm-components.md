---
description: Los componentes de CRM se pueden instalar en una aplicación de servidor COM+ o en una aplicación de biblioteca COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configuración de componentes de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705378"
---
# <a name="configuring-com-crm-components"></a>Configuración de componentes de COM+ CRM

Los componentes de CRM se pueden instalar en una aplicación de servidor COM+ o en una aplicación de biblioteca COM+. Sin embargo, siempre deben ejecutarse en una aplicación de servidor COM+. Si se instalan en una aplicación de biblioteca COM+, no estarán disponibles para su uso en procesos de cliente.

Si los componentes de CRM están instalados en una aplicación de biblioteca, están disponibles para más de una aplicación de servidor. Si se instala en una aplicación de servidor específica, solo estarán disponibles para esa aplicación de servidor específica.

Para habilitar el uso de un CRM en una aplicación de servidor, siga estos pasos:

1.  En servicios de componentes, en la página Propiedades de la aplicación de servidor, haga clic en la pestaña **Opciones avanzadas** .

2.  Seleccione la opción **habilitar los administradores de compensación de recursos** para esa aplicación de servidor. Si no se selecciona esta opción, se producirá un error en los intentos de usar un CRM dentro de esta aplicación de servidor.

    > [!Note]  
    > Si se instala en una aplicación de biblioteca, no es necesario seleccionar la opción **habilitar los administradores de compensación de recursos** para esa aplicación de biblioteca, pero se debe seleccionar esta opción para la aplicación de servidor en la que se va a ejecutar el CRM.

     

Se recomienda que los componentes de CRM y de compensador de CRM para un CRM específico se instalen en la misma aplicación.

La configuración recomendada para los componentes de CRM es la siguiente.



| Componente           | Configuración                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **Trabajador de CRM**      | Transaction = requiredsync = yesJIT = yesthreading Model = both (o modelo de subprocesos = apartamento)     |
| **Compensator de CRM** | Transaction = disabledsync = disabledJIT = nothreading Model = both (o el modelo de subprocesos = Apartment) |



 

> [!Note]  
> Los componentes que utilizan el CRM deben especificar explícitamente un modelo de subprocesos cuando se registran. No se admite el valor predeterminado "apartamento del subproceso principal". Los únicos dos modelos de subprocesos admitidos son Apartment y both.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de Administrador de recursos de compensación de COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



