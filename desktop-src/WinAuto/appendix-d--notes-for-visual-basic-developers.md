---
title: Notas del apéndice D para Visual Basic desarrolladores
description: En esta sección se proporciona información sobre Microsoft Active Accessibility para desarrolladores de Visual Basic Microsoft.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a857aeb8e04a0648d991e26913f9a9cf5c35328c62ed3f1ac3903a267e5a4e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122425"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Apéndice D: Notas para desarrolladores de Visual Basic

En esta sección se proporciona información sobre Microsoft Active Accessibility para desarrolladores de Visual Basic Microsoft.

Las aplicaciones escritas en Visual Basic son Microsoft Active Accessibility cliente. No proporcionan información sobre sus elementos de interfaz de usuario personalizados porque no implementan [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ni ninguna otra interfaz de Modelo de objetos componentes (COM).

En esta documentación se usan los nombres de C/C++ para las [**propiedades IAccessible;**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) sin embargo, los Visual Basic son similares. Por ejemplo, la [**propiedad IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) se llamaría **accName** en una Visual Basic aplicación.

## <a name="in-this-section"></a>En esta sección

-   [Visual Basic Notas del método: accName](visual-basic-method-notes--accname.md)
-   [Visual Basic Notas del método: accValue](visual-basic-method-notes--accvalue.md)
-   [Visual Basic Programas de ejemplo](visual-basic-sample-programs.md)

 

 




