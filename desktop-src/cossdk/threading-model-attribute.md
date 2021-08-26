---
description: COM+ administra los subprocesos por usted. Cada componente COM tiene una propiedad ThreadingModel que puede especificar al desarrollar el componente. Esta propiedad determina cómo se asignan los objetos de componentes a los subprocesos para la ejecución del método.
ms.assetid: 5fae8475-3d2e-4939-80a7-bc9a677a50b3
title: Atributo de modelo de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dba6ae625e4413516066f7180a4eb6870fe4f90df38947fc2476cfbcc7dfadb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070245"
---
# <a name="threading-model-attribute"></a>Atributo de modelo de subprocesos

COM+ administra los subprocesos por usted. Cada componente COM tiene una **propiedad ThreadingModel** que puede especificar al desarrollar el componente. Esta propiedad determina cómo se asignan los objetos del componente a los subprocesos para la ejecución del método.

Puede usar la herramienta administrativa Servicios de componentes para ver la propiedad  threading-model haciendo clic con el botón derecho en un componente de la carpeta Componentes, haciendo clic en Propiedades y, a continuación, haciendo clic en la pestaña Simultaneidad.  En **Modelo de subprocesos**, los valores posibles son los siguientes:

-   **Main Thread Apartment**
-   **Single Thread Apartment**
-   **Free Thread Apartment**
-   **Apartamento neutro**
-   **Cualquier apartamento**

El modelo de subprocesamiento preferido para COM+ es [el apartamento neutro](neutral-apartments.md). Sin embargo, si no especifica un modelo de subprocesos para el componente, COM+ usa el apartamento del subproceso principal, que es el valor predeterminado.

> [!Note]  
> Para obtener información más detallada, vea [Elegir el modelo de subprocesos](/windows/desktop/com/choosing-the-threading-model).

 

En la tabla siguiente se muestra el modelo de programación para los departamentos en COM+.



| Modelo                     | Apartamento                                                 | Gratis                               | Ambos                               | Neutra                      | No especificado                      |
|---------------------------|-----------------------------------------------------------|------------------------------------|------------------------------------|------------------------------|------------------------------------|
| De un solo subproceso, no principal | Creado en el apartamento actual                              | Creado en un apartamento multiproceso | Creado en el apartamento actual       | Creado en un apartamento neutro | Creado en el apartamento subproceso principal |
| De un solo subproceso, principal     | Creado en el apartamento actual                              | Creado en un apartamento multiproceso | Creado en el apartamento actual       | Creado en un apartamento neutro | Creado en el apartamento actual       |
| Multiproceso             | Creado en el apartamento de un solo subproceso del host                 | Creado en un apartamento multiproceso | Creado en un apartamento multiproceso | Creado en un apartamento neutro | Creado en el apartamento subproceso principal |
| Neutro (en subproceso STA)   | Creado en el apartamento de un solo subproceso del host para este subproceso | Creado en un apartamento multiproceso | Creado en un apartamento neutro       | Creado en un apartamento neutro | Creado en el apartamento subproceso principal |
| Neutro (en subproceso MTA)   | Creado en el apartamento de un solo subproceso del host                 | Creado en un apartamento multiproceso | Creado en un apartamento neutro       | Creado en un apartamento neutro | Creado en el apartamento subproceso principal |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ThreadingModel**](components.md)
</dt> </dl>

 

 
