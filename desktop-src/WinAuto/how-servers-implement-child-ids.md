---
title: Cómo los servidores implementan identificadores secundarios
description: Los desarrolladores de servidores pueden asignar identificadores secundarios tanto a elementos simples como a objetos accesibles. Sin embargo, el enfoque recomendado es admitir la interfaz de modelo de objetos componentes (COM) estándar IEnumVARIANT en cada objeto accesible que tenga elementos secundarios.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995427"
---
# <a name="how-servers-implement-child-ids"></a>Cómo los servidores implementan identificadores secundarios

Los desarrolladores de servidores pueden asignar identificadores secundarios tanto a elementos simples como a objetos accesibles. Sin embargo, el enfoque recomendado es admitir la interfaz de modelo de objetos componentes (COM) estándar [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en cada objeto accesible que tenga elementos secundarios.

Si implementa [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), debe:

-   Enumera todos los elementos secundarios, tanto los elementos simples como los objetos accesibles. Proporcione los identificadores secundarios de todos los elementos simples y proporcione la [**IDispatch**](idispatch-interface.md) a cada objeto accesible.
-   Para objetos accesibles, establezca el miembro **VT** de la [**variante**](variant-structure.md) en el \_ envío de VT. El miembro **pdispVal** debe contener un puntero a la interfaz [**IDispatch**](idispatch-interface.md) . Tenga en cuenta que el cliente asigna y libera la **variante** .
-   En el caso de los elementos simples, el identificador secundario es cualquier entero positivo de 32 bits. Tenga en cuenta que los enteros negativos y cero están reservados por Microsoft Active Accessibility. Establezca el miembro **VT** de la estructura [**Variant**](variant-structure.md) en VT \_ I4 y el miembro **lVal** en el identificador secundario.

Si no admite [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant), debe asignar los identificadores secundarios y el número de elementos secundarios de cada objeto secuencialmente a partir de uno.

Se recomienda que los clientes usen la función de Microsoft Active Accessibility [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) en lugar de llamar directamente a la interfaz de Server [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .

 

 