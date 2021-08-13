---
title: Cómo obtienen los clientes los IDs secundarios
description: Cómo obtienen los clientes los IDs secundarios
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a12dc3f40c2aaa776c1fa8e61713c52ffbdcde554c9f6a1cbca7093998780c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388605"
---
# <a name="how-clients-obtain-child-ids"></a>Cómo obtienen los clientes los IDs secundarios

Los desarrolladores de cliente pueden obtener el identificador secundario de un objeto de las maneras siguientes:

-   Llame [**a AccessibleChildren.**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) Esta función recupera una matriz de [**estructuras VARIANT.**](variant-structure.md)
-   Consulte el objeto para ver si admite la [**interfaz IEnumVARIANT.**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) Si está presente, use [**IEnumVARIANT::Next para**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtener los ID secundarios.
-   Recopile los iD secundarios llamando al método [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) del objeto primario.

> [!Note]  
> Es responsabilidad del cliente liberar la memoria usada para las estructuras [**VARIANT.**](variant-structure.md) Los clientes también deben llamar [**a IUnknown::Release en**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cualquier [**interfaz IDispatch**](idispatch-interface.md) que se devuelva.

 

 

 