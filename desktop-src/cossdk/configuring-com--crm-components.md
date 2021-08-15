---
description: Los componentes de CRM se pueden instalar en una aplicación de servidor COM+ o en una aplicación de biblioteca COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configuración de componentes de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c79f8c9716a9a4db2888231c886d3d1a4d929dd1a8dfb9f9f359ab03ec7670b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307454"
---
# <a name="configuring-com-crm-components"></a>Configuración de componentes de COM+ CRM

Los componentes de CRM se pueden instalar en una aplicación de servidor COM+ o en una aplicación de biblioteca COM+. Sin embargo, siempre deben ejecutarse en una aplicación de servidor COM+. Si se instalan en una aplicación de biblioteca COM+, no están disponibles para su uso en procesos de cliente.

Si los componentes de CRM se instalan en una aplicación de biblioteca, están disponibles para más de una aplicación de servidor. Si se instalan en una aplicación de servidor específica, solo están disponibles para esa aplicación de servidor específica.

Para habilitar el uso de crm en una aplicación de servidor, siga estos pasos:

1.  En Servicios de componentes, en la página de propiedades de la aplicación de servidor, haga clic en **la pestaña** Avanzadas.

2.  Seleccione la **opción Habilitar administradores de recursos de** compensación para esa aplicación de servidor. Si no se selecciona esta opción, se producirá un error al intentar usar crm dentro de esta aplicación de servidor.

    > [!Note]  
    > Si se instala en una aplicación de biblioteca, no es necesario seleccionar la opción Habilitar administradores de recursos de compensación para esa aplicación de biblioteca, pero esta opción debe seleccionarse para la aplicación de servidor en la que crm está diseñado para ejecutarse. 

     

Se recomienda instalar los componentes crm worker y CRM Compensator para un CRM específico en la misma aplicación.

La configuración recomendada para los componentes de CRM es la siguiente.



| Componente           | Configuración                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| **CRM Worker**      | transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)     |
| **CRM Compensator** | transaction = disabledsync = disabledJIT = nothreading model = Both (o threading model = Apartment) |



 

> [!Note]  
> Los componentes que usan CRM deben especificar explícitamente un modelo de subprocesos cuando se registran. El valor predeterminado, "Main Thread Apartment", no se admite. Los dos únicos modelos de subprocesos admitidos son Apartment y Both.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de compensación Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



