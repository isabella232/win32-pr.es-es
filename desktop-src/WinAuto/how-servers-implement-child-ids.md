---
title: Cómo implementan los servidores los IDs secundarios
description: Los desarrolladores de servidores pueden asignar los ID secundarios a elementos simples y objetos accesibles. Sin embargo, el enfoque recomendado es admitir la interfaz estándar del modelo de objetos componentes (COM) IEnumVARIANT en todos los objetos accesibles que tienen elementos secundarios.
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160553"
---
# <a name="how-servers-implement-child-ids"></a>Cómo implementan los servidores los IDs secundarios

Los desarrolladores de servidores pueden asignar los ID secundarios a elementos simples y objetos accesibles. Sin embargo, el enfoque recomendado es admitir la interfaz estándar del modelo de objetos componentes (COM) [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en todos los objetos accesibles que tienen elementos secundarios.

Si implementa [IEnumVARIANT,](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)debe:

-   Enumera todos los elementos secundarios, tanto elementos simples como objetos accesibles. Proporcione los ID secundarios para todos los elementos simples y proporcione [**el IDispatch**](idispatch-interface.md) a cada objeto accesible.
-   Para objetos accesibles, establezca **el miembro vt** de [**VARIANT**](variant-structure.md) en VT \_ DISPATCH. El **miembro pdispVal** debe contener un puntero a la [**interfaz IDispatch.**](idispatch-interface.md) Tenga en cuenta **que el** cliente asigna y libera variant.
-   Para los elementos simples, el identificador secundario es cualquier entero positivo de 32 bits. Tenga en cuenta que los enteros cero y negativos están reservados por Microsoft Active Accessibility. Establezca el [**miembro vt**](variant-structure.md) de la estructura **VARIANT** en VT \_ I4 y el **miembro lVal** en el identificador secundario.

Si no admite [IEnumVARIANT,](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)debe asignar los identificaciónes secundarios y numerar los elementos secundarios de cada objeto secuencialmente a partir de uno.

Se recomienda que los clientes usen la Microsoft Active Accessibility [**accesibleChildren en**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) lugar de llamar directamente a la [interfaz IEnumVARIANT del](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) servidor.

 

 