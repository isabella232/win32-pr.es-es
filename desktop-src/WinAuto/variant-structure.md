---
title: VARIANT (estructura)
description: La mayoría de las Microsoft Active Accessibility y las propiedades y los métodos IAccessible toman una estructura VARIANT como parámetro. Básicamente, la estructura VARIANT es un contenedor para una unión grande que contiene muchos tipos de datos.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063d1e17d998f3cb7d70a0a271e55f02628e7864164e00becb5a708af371e12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563553"
---
# <a name="variant-structure"></a>VARIANT (estructura)

La mayoría de las Microsoft Active Accessibility y las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) toman una [**estructura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) como parámetro. Básicamente, la **estructura VARIANT** es un contenedor para una unión grande que contiene muchos tipos de datos.

El valor del primer miembro de la estructura, **vt**, describe cuál de los miembros de unión es válido. Aunque la [**estructura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) admite muchos tipos de datos diferentes, Microsoft Active Accessibility usa solo los siguientes tipos.



| vt (valor)     | Nombre de miembro de valor correspondiente |
|--------------|---------------------------------|
| VT \_ I4       | **lVal**                        |
| VT \_ DISPATCH | **pdispVal**                    |
| VT \_ BSTR     | **bstrVal**                     |
| VT \_ EMPTY    | ninguno                            |



 

Cuando reciba información en una [**estructura VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) compruebe el **miembro vt** para averiguar qué miembro contiene datos válidos. Del mismo modo, cuando envíe información mediante una **estructura VARIANT,** establezca siempre **vt** para reflejar el miembro de unión que contiene la información.

Antes de usar la estructura , inicialíclice mediante una llamada a la [**función VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM). Cuando termine con la estructura , descálela antes de liberar la memoria que contiene [**variant**](/windows/win32/api/oaidl/ns-oaidl-variant) llamando a [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).

 

 