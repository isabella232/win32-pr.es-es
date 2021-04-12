---
title: Seleccionar objetos secundarios
description: Los clientes llaman al método IAccessible accSelect para modificar la selección o el foco del teclado entre los elementos secundarios de un objeto. Las constantes SELFLAG especificadas con la llamada definen la operación que se va a realizar.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356831"
---
# <a name="selecting-child-objects"></a>Seleccionar objetos secundarios

Los clientes llaman al método [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para modificar la selección o el foco del teclado entre los elementos secundarios de un objeto. Las [constantes SELFLAG](selflag.md) especificadas con la llamada definen la operación que se va a realizar.

Si se llama a [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) con la marca [**\_ TAKEFOCUS de SELFLAG**](selflag.md) en un objeto secundario que tiene un **hWnd**, la marca solo surte efecto si el elemento primario del objeto tiene el foco.

## <a name="performing-complex-selection-operations"></a>Realización de operaciones de selección complejas

A continuación se describen los valores de SELFLAG que se especifican al llamar a [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para realizar operaciones de selección complejas.

**Para simular un clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ TAKESELECTION**](selflag.md)

**Para seleccionar un elemento de destino simulando CTRL + clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ ADDSELECTION**](selflag.md)

**Para cancelar la selección de un elemento de destino simulando CTRL + clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ REMOVESELECTION**](selflag.md)

**Para simular Mayús + clic**

-   [**SELFLAG \_ TAKEFOCUS**](selflag.md) \| [ **SELFLAG \_ EXTENDSELECTION**](selflag.md)

**Para seleccionar un intervalo de objetos y colocar el foco en el último objeto**

1.  Especifique [**SELFLAG \_ TAKEFOCUS**](selflag.md) en el objeto de inicio para establecer el delimitador de selección.
2.  Vuelva a llamar a [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) y especifique [**SELFLAG \_ EXTENDSELECTION**](selflag.md) \| [**SELFLAG \_ TAKEFOCUS**](selflag.md) en el último objeto.

**Para anular la selección de todos los objetos**

1.  Especifique [**SELFLAG \_ TAKESELECTION**](selflag.md) en cualquier objeto. Esta marca anula la selección de todos los objetos seleccionados excepto el que acaba de seleccionar.
2.  Vuelva a llamar a [**IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) y especifique [**SELFLAG \_ REMOVESELECTION**](selflag.md) en el objeto restante.

 

 




