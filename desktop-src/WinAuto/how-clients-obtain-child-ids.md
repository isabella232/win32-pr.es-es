---
title: Cómo los clientes obtienen los identificadores secundarios
description: Cómo los clientes obtienen los identificadores secundarios
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791943"
---
# <a name="how-clients-obtain-child-ids"></a>Cómo los clientes obtienen los identificadores secundarios

Los desarrolladores de cliente pueden obtener el identificador secundario de un objeto de las siguientes maneras:

-   Llame a [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren). Esta función recupera una matriz de estructuras [**variantes**](variant-structure.md) .
-   Consulte el objeto para ver si es compatible con la interfaz [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) . Si está presente, use [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) para obtener los identificadores secundarios.
-   Recopile los identificadores secundarios llamando al método [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) del objeto primario.

> [!Note]  
> Es responsabilidad del cliente liberar la memoria que se usa para las estructuras de [**variantes**](variant-structure.md) . Los clientes también deben llamar a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en cualquier interfaz [**IDispatch**](idispatch-interface.md) que se devuelva.

 

 

 