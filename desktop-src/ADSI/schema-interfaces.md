---
title: Interfaces de esquema
description: Interfaces de esquema
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- interfaces de esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f414fdea2418fb92a0a3c8c9e8bf88eb6d7f00b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993845"
---
# <a name="schema-interfaces"></a>Interfaces de esquema

El contenedor de esquemas contiene un conjunto de definiciones de esquema que están adjuntas a parte del árbol de espacios de nombres del proveedor. Normalmente, cada instancia de un espacio de nombres tiene su propio esquema. Por ejemplo, en la siguiente ilustración, el proveedor de ejemplo ADSI define un contenedor de esquema en cada uno de los nodos raíz "Seattle" y "Toronto".

![contención de esquemas](images/schemacont.png)

Para crear una implementación de ADSI para un proveedor, debe proporcionar objetos de administración de esquema que reflejen el espacio de nombres subyacente del proveedor y que admitan las interfaces de esquema ADSI. A continuación se muestra una lista de las interfaces de esquema ADSI, que se encuentran en el contenedor de esquemas.

-   [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) representa las clases de servicio de directorio.
-   [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) representa las propiedades del servicio de directorio que tienen uno o varios valores.
-   [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) representa el tipo de variante única.

Las interfaces definidas por ADSI pueden admitir propiedades específicas y sintaxis para el proveedor. Los proveedores pueden elegir ampliar una definición de ADSI mediante los métodos que crean y tienen acceso a las propiedades; por ejemplo, puede usar los métodos de la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) , como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) y [**PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex). Los proveedores también pueden admitir propiedades adicionales mediante interfaces adicionales. Para obtener una lista completa de las interfaces ADSI, consulte [interfaces ADSI](adsi-interfaces.md).

Un componente de proveedor ADSI con un espacio de nombres complejo podría permitir que existan varios esquemas en una instancia de espacio de nombres, cada uno en una parte diferente del árbol. Sin embargo, la propiedad [**IADs:: Schema**](iads-property-methods.md) de un objeto siempre nombra su propia definición de esquema.

 

 




