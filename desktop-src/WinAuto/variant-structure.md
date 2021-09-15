---
title: VARIANT (estructura)
description: La mayoría de las Microsoft Active Accessibility y las propiedades y los métodos IAccessible toman una estructura VARIANT como parámetro. Básicamente, la estructura VARIANT es un contenedor para una unión grande que contiene muchos tipos de datos.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579372"
---
# <a name="variant-structure"></a>VARIANT (estructura)

La mayoría de las Microsoft Active Accessibility y las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) toman una [**estructura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) como parámetro. Básicamente, la **estructura VARIANT** es un contenedor para una unión grande que contiene muchos tipos de datos.

El valor del primer miembro de la estructura, **vt**, describe cuál de los miembros de unión es válido. Aunque la [**estructura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) admite muchos tipos de datos diferentes, Microsoft Active Accessibility solo los tipos siguientes.



| vt (Valor)     | Nombre de miembro de valor correspondiente |
|--------------|---------------------------------|
| VT \_ I4       | **lVal**                        |
| VT \_ DISPATCH | **pdispVal**                    |
| VT \_ BSTR     | **bstrVal**                     |
| VT \_ EMPTY    | ninguno                            |



 

Cuando reciba información en una estructura [**VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) compruebe el **miembro vt** para averiguar qué miembro contiene datos válidos. De forma similar, al enviar información mediante una **estructura VARIANT,** establezca siempre **vt** para reflejar el miembro de unión que contiene la información.

Antes de usar la estructura , inicialíicela llamando a la función Modelo de objetos componentes [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) (COM). Cuando termine con la estructura , descálela antes de que se libera la memoria que contiene [**variant**](/windows/win32/api/oaidl/ns-oaidl-variant) mediante una llamada [**a VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).

 

 