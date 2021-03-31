---
description: COM+ administra los subprocesos. Cada componente COM tiene una propiedad ThreadingModel que se puede especificar al desarrollar el componente. Esta propiedad determina cómo se asignan los objetos de componentes a los subprocesos para la ejecución del método.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Atributo del modelo de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91960a753b29ac5f5209a5bafa31c362f3dfe08d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423267"
---
# <a name="threading-model-attribute"></a>Atributo del modelo de subprocesos

COM+ administra los subprocesos. Cada componente COM tiene una propiedad **ThreadingModel** que se puede especificar al desarrollar el componente. Esta propiedad determina cómo se asignan los objetos del componente a los subprocesos para la ejecución del método.

Puede usar la herramienta administrativa Servicios de componentes para ver la propiedad modelo de subprocesos; para ello, haga clic con el botón secundario en un componente de la carpeta **componentes** , haga clic en **propiedades** y, a continuación, haga clic en la pestaña **simultaneidad** . En el **modelo de subprocesos**, los valores posibles son los siguientes:

-   **Apartamento de subproceso principal**
-   **Apartamento de un solo subproceso**
-   **Apartamento de subprocesos libre**
-   **Apartamento neutro**
-   **Cualquier apartamento**

El modelo de subprocesos preferido para COM+ es el [Apartamento neutro](neutral-apartments.md). Sin embargo, si no se especifica un modelo de subprocesos para el componente, COM+ utiliza el apartamento de subproceso principal, que es el valor predeterminado.

> [!Note]  
> Para obtener información más detallada, vea [elegir el modelo de subprocesos](/windows/desktop/com/choosing-the-threading-model).

 

En la tabla siguiente se muestra el modelo de programación para apartamentos en COM+.



| Modelo                     | Procesamiento                                                 | Gratuito                               | Ambos                               | Neutra                      | No especificado                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| Subproceso único, no principal | Creado en el apartamento actual                              | Creado en Apartamento multiproceso | Creado en el apartamento actual       | Creado en Apartamento neutro | Creado en el contenedor principal de subprocesos |
| Subproceso único, principal     | Creado en el apartamento actual                              | Creado en Apartamento multiproceso | Creado en el apartamento actual       | Creado en Apartamento neutro | Creado en el apartamento actual       |
| Multiproceso             | Creado en un contenedor uniproceso de host                 | Creado en Apartamento multiproceso | Creado en Apartamento multiproceso | Creado en Apartamento neutro | Creado en el contenedor principal de subprocesos |
| Neutro (en el subproceso STA)   | Creado en un contenedor uniproceso de host para este subproceso | Creado en Apartamento multiproceso | Creado en Apartamento neutro       | Creado en Apartamento neutro | Creado en el contenedor principal de subprocesos |
| Neutro (en subproceso MTA)   | Creado en un contenedor uniproceso de host                 | Creado en Apartamento multiproceso | Creado en Apartamento neutro       | Creado en Apartamento neutro | Creado en el contenedor principal de subprocesos |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
