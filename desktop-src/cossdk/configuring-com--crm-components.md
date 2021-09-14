---
description: Los componentes de CRM se pueden instalar en una aplicación de servidor COM+ o en una aplicación de biblioteca COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configuración de componentes de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358908"
---
# <a name="configuring-com-crm-components"></a>Configuración de componentes de COM+ CRM

Los componentes de CRM se pueden instalar en una aplicación de servidor COM+ o en una aplicación de biblioteca COM+. Sin embargo, siempre deben ejecutarse en una aplicación de servidor COM+. Si se instalan en una aplicación de biblioteca COM+, no están disponibles para su uso en procesos de cliente.

Si los componentes de CRM se instalan en una aplicación de biblioteca, están disponibles para más de una aplicación de servidor. Si se instalan en una aplicación de servidor específica, solo están disponibles para esa aplicación de servidor específica.

Para habilitar el uso de un CRM en una aplicación de servidor, siga estos pasos:

1.  En Servicios de componentes, en la página de propiedades de la aplicación de servidor, haga clic en **la pestaña** Avanzadas.

2.  Seleccione la **opción Habilitar administradores de recursos de** compensación para esa aplicación de servidor. Si no se selecciona esta opción, se producirá un error al intentar usar un CRM dentro de esta aplicación de servidor.

    > [!Note]  
    > Si se instala en una aplicación de biblioteca, no es necesario seleccionar la opción Habilitar administradores de recursos de compensación para esa aplicación de biblioteca, pero esta opción debe seleccionarse para la aplicación de servidor en la que está previsto que se ejecute CRM. 

     

Se recomienda que los componentes De trabajo de CRM y Compensador de CRM para un CRM específico se instalen en la misma aplicación.

La configuración recomendada para los componentes de CRM es la siguiente.



| Componente           | Configuración                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **CRM Worker**      | transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)     |
| **Compensador de CRM** | transaction = disabledsync = disabledJIT = nothreading model = Both (or threading model = Apartment) |



 

> [!Note]  
> Los componentes que usan CRM deben especificar explícitamente un modelo de subprocesos cuando se registran. El valor predeterminado, "Main Thread Apartment", no se admite. Los dos únicos modelos de subprocesamiento admitidos son Apartment y Both.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



