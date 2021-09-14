---
title: Selección de objetos secundarios
description: Los clientes llaman al método IAccessible accSelect para modificar la selección o el foco de teclado entre los elementos secundarios de un objeto . Las constantes SELF CONSTANT especificadas con la llamada definen la operación que se debe realizar.
ms.assetid: 5e7ad1e9-b1b2-4e76-93e8-b58251930621
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d6f898f7da7beb047d3e781ad46cf383b3dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070633"
---
# <a name="selecting-child-objects"></a>Selección de objetos secundarios

Los clientes llaman [**al método IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para modificar la selección o el foco de teclado entre los elementos secundarios de un objeto . Las [constantes SELF CONSTANT especificadas](selflag.md) con la llamada definen la operación que se debe realizar.

Si se llama a [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) con la marca [**\_ TAKEFOCUS**](selflag.md) DE SELFANDER en un objeto secundario que tiene un **HWND**, la marca solo surte efecto si el elemento primario del objeto tiene el foco.

## <a name="performing-complex-selection-operations"></a>Realizar operaciones de selección complejas

A continuación se describen los valores SELFCLI que se deben especificar al llamar a [**IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) para realizar operaciones de selección complejas.

**Para simular un clic**

-   [**SELFRET \_ TAKEFOCUS**](selflag.md) \| [ **SELFFOCUS \_ TAKESELECTION**](selflag.md)

**Para seleccionar un elemento de destino simulando CTRL + clic**

-   [**SELFRET \_ TAKEFOCUS**](selflag.md) \| [ **SELFFOCUS \_ ADDSELECTION**](selflag.md)

**Para cancelar la selección de un elemento de destino simulando CTRL + clic**

-   [**SELFRET \_ TAKEFOCUS**](selflag.md) \| [ **SELFENSA \_ REMOVESELECTION**](selflag.md)

**Para simular MAYÚS + clic**

-   [**SELFRET \_ TAKEFOCUS**](selflag.md) \| [ **SELFFOCUS \_ EXTENDSELECTION**](selflag.md)

**Para seleccionar un intervalo de objetos y centrar el foco en el último objeto**

1.  Especifique [**SELFDETERMINA \_ TAKEFOCUS**](selflag.md) en el objeto de inicio para establecer el delimitador de selección.
2.  Llame [**de nuevo a IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) y especifique [**SELFDETERMINA \_ EXTENDSELECTION**](selflag.md) \| [**SELFDETERMINA \_ TAKEFOCUS**](selflag.md) en el último objeto.

**Para anular la selección de todos los objetos**

1.  Especifique [**SELFDETERMINA \_ TAKESELECTION en**](selflag.md) cualquier objeto. Esta marca anula la selección de todos los objetos seleccionados, excepto el que acaba de seleccionar.
2.  Llame [**de nuevo a IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) y especifique [**SELFDETERMINA \_ REMOVESELECTION**](selflag.md) en el objeto restante.

 

 




