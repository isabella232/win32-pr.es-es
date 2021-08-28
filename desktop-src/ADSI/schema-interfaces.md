---
title: Interfaces de esquema
description: Interfaces de esquema
ms.assetid: b3427202-352b-4b35-877e-d28fb3d3906a
ms.tgt_platform: multiple
keywords:
- interfaces de esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dfa22a32a4d93c36a7419d48ea6127c2345ffdea62686147d1ba08c41ea7992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770564"
---
# <a name="schema-interfaces"></a>Interfaces de esquema

El contenedor de esquemas contiene un conjunto de definiciones de esquema que se adjuntan a parte del árbol de espacio de nombres del proveedor. Normalmente, cada instancia de un espacio de nombres tiene su propio esquema. Por ejemplo, en la ilustración siguiente, el proveedor de ejemplo ADSI define un contenedor de esquema en cada uno de los nodos raíz "Seattle" y "Toronto".

![contención del esquema](images/schemacont.png)

Para crear una implementación adsi para un proveedor, debe proporcionar objetos de administración de esquemas que reflejen el espacio de nombres subyacente del proveedor y que admitan interfaces de esquema ADSI. A continuación se muestra una lista de las interfaces de esquema ADSI, que se encuentran en el contenedor de esquemas.

-   [**IADsClass representa las**](/windows/desktop/api/Iads/nn-iads-iadsclass) clases de servicio de directorio.
-   [**IADsProperty representa**](/windows/desktop/api/Iads/nn-iads-iadsproperty) las propiedades del servicio de directorio que tienen uno o varios valores.
-   [**IADsSyntax representa**](/windows/desktop/api/Iads/nn-iads-iadssyntax) el tipo VARIANT único.

Las interfaces definidas por ADSI pueden admitir propiedades y sintaxis específicas para el proveedor. Los proveedores pueden optar por ampliar una definición adsi mediante los métodos que crean y acceden a las propiedades; por ejemplo, puede usar los métodos de la interfaz [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**GetEx,**](/windows/desktop/api/Iads/nf-iads-iads-getex) [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put) y [**PutEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex) Los proveedores también pueden admitir propiedades adicionales a través de interfaces adicionales. Para obtener una lista completa de las interfaces ADSI, vea [Interfaces ADSI](adsi-interfaces.md).

Un componente de proveedor ADSI con un espacio de nombres complejo podría permitir que existan varios esquemas en una instancia de espacio de nombres, cada uno en una parte diferente del árbol. Sin embargo, la propiedad [**IADs::Schema**](iads-property-methods.md) de un objeto siempre asigna un nombre a su propia definición de esquema.

 

 




