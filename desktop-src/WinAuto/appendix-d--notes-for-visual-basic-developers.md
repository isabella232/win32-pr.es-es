---
title: Apéndice D Notas para desarrolladores de Visual Basic
description: En esta sección se proporciona información acerca de Microsoft Active Accessibility para desarrolladores de Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994172"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Apéndice D: notas para desarrolladores de Visual Basic

En esta sección se proporciona información acerca de Microsoft Active Accessibility para desarrolladores de Microsoft Visual Basic.

Las aplicaciones escritas en Visual Basic son clientes de Microsoft Active Accessibility. No proporcionan información sobre los elementos de la interfaz de usuario personalizados porque no implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ni ninguna otra interfaz del modelo de objetos componentes (com).

En esta documentación se usan los nombres de C/C++ para las propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ; sin embargo, los nombres de Visual Basic son similares. Por ejemplo, la propiedad [**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) se llamaría **accName** en una aplicación Visual Basic.

## <a name="in-this-section"></a>En esta sección

-   [Notas del método Visual Basic: accName](visual-basic-method-notes--accname.md)
-   [Notas del método Visual Basic: accValue](visual-basic-method-notes--accvalue.md)
-   [Visual Basic programas de ejemplo](visual-basic-sample-programs.md)

 

 




