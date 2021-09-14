---
title: Cómo obtienen los clientes los iDs secundarios
description: Cómo obtienen los clientes los iDs secundarios
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160554"
---
# <a name="how-clients-obtain-child-ids"></a>Cómo obtienen los clientes los iDs secundarios

Los desarrolladores de cliente pueden obtener el identificador secundario de un objeto de las maneras siguientes:

-   Llame [**a AccessibleChildren.**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) Esta función recupera una matriz de [**estructuras VARIANT.**](variant-structure.md)
-   Consulte el objeto para ver si admite la [**interfaz IEnumVARIANT.**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) Si está presente, use [**IEnumVARIANT::Next para**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) obtener los ID secundarios.
-   Recopile los ID secundarios llamando al método [**IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) del objeto primario.

> [!Note]  
> Es responsabilidad del cliente liberar la memoria usada para las estructuras [**VARIANT.**](variant-structure.md) Los clientes también deben llamar [**a IUnknown::Release en**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) cualquier [**interfaz IDispatch**](idispatch-interface.md) que se devuelva.

 

 

 