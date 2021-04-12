---
title: VARIANT (estructura)
description: La mayoría de las funciones de Microsoft Active Accessibility y las propiedades y los métodos IAccessible toman una estructura VARIANT como parámetro. Esencialmente, la estructura variante es un contenedor para una Unión grande que incluye muchos tipos de datos.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149388"
---
# <a name="variant-structure"></a>VARIANT (estructura)

La mayoría de las funciones de Microsoft Active Accessibility y las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) toman una estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) como parámetro. Esencialmente, la estructura **variante** es un contenedor para una Unión grande que incluye muchos tipos de datos.

El valor del primer miembro de la estructura, **VT**, describe cuál de los miembros de la Unión es válido. Aunque la estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) admite muchos tipos de datos diferentes, Microsoft Active Accessibility solo usa los siguientes tipos.



| Valor de VT     | Nombre del miembro de valor correspondiente |
|--------------|---------------------------------|
| VT \_ I4       | **lVal**                        |
| distribución de VT \_ | **pdispVal**                    |
| VT \_ BSTR     | **bstrVal**                     |
| VT \_ vacío    | ninguno                            |



 

Cuando reciba información en una estructura [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) , compruebe el miembro **VT** para averiguar qué miembro contiene datos válidos. Del mismo modo, cuando envíe información mediante una estructura **Variant** , establezca siempre **VT** para reflejar el miembro de Unión que contiene la información.

Antes de utilizar la estructura, Inicialícelo mediante una llamada a la función [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) del modelo de objetos componentes (com). Cuando termine con la estructura, desactívela antes de que se libere la memoria que contiene la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) llamando a [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).

 

 