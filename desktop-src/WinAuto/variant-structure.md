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
# <a name="variant-structure"></a><span data-ttu-id="fc845-104">VARIANT (estructura)</span><span class="sxs-lookup"><span data-stu-id="fc845-104">VARIANT Structure</span></span>

<span data-ttu-id="fc845-105">La mayoría de las funciones de Microsoft Active Accessibility y las propiedades y los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) toman una estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) como parámetro.</span><span class="sxs-lookup"><span data-stu-id="fc845-105">Most of the Microsoft Active Accessibility functions and the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods take a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure as a parameter.</span></span> <span data-ttu-id="fc845-106">Esencialmente, la estructura **variante** es un contenedor para una Unión grande que incluye muchos tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="fc845-106">Essentially, the **VARIANT** structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="fc845-107">El valor del primer miembro de la estructura, **VT**, describe cuál de los miembros de la Unión es válido.</span><span class="sxs-lookup"><span data-stu-id="fc845-107">The value in the first member of the structure, **vt**, describes which of the union members is valid.</span></span> <span data-ttu-id="fc845-108">Aunque la estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) admite muchos tipos de datos diferentes, Microsoft Active Accessibility solo usa los siguientes tipos.</span><span class="sxs-lookup"><span data-stu-id="fc845-108">Although the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure supports many different data types, Microsoft Active Accessibility uses only the following types.</span></span>



| <span data-ttu-id="fc845-109">Valor de VT</span><span class="sxs-lookup"><span data-stu-id="fc845-109">vt Value</span></span>     | <span data-ttu-id="fc845-110">Nombre del miembro de valor correspondiente</span><span class="sxs-lookup"><span data-stu-id="fc845-110">Corresponding value member name</span></span> |
|--------------|---------------------------------|
| <span data-ttu-id="fc845-111">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="fc845-111">VT\_I4</span></span>       | <span data-ttu-id="fc845-112">**lVal**</span><span class="sxs-lookup"><span data-stu-id="fc845-112">**lVal**</span></span>                        |
| <span data-ttu-id="fc845-113">distribución de VT \_</span><span class="sxs-lookup"><span data-stu-id="fc845-113">VT\_DISPATCH</span></span> | <span data-ttu-id="fc845-114">**pdispVal**</span><span class="sxs-lookup"><span data-stu-id="fc845-114">**pdispVal**</span></span>                    |
| <span data-ttu-id="fc845-115">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="fc845-115">VT\_BSTR</span></span>     | <span data-ttu-id="fc845-116">**bstrVal**</span><span class="sxs-lookup"><span data-stu-id="fc845-116">**bstrVal**</span></span>                     |
| <span data-ttu-id="fc845-117">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="fc845-117">VT\_EMPTY</span></span>    | <span data-ttu-id="fc845-118">ninguno</span><span class="sxs-lookup"><span data-stu-id="fc845-118">none</span></span>                            |



 

<span data-ttu-id="fc845-119">Cuando reciba información en una estructura [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) , compruebe el miembro **VT** para averiguar qué miembro contiene datos válidos.</span><span class="sxs-lookup"><span data-stu-id="fc845-119">When you receive information in a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure, check the **vt** member to find out which member contains valid data.</span></span> <span data-ttu-id="fc845-120">Del mismo modo, cuando envíe información mediante una estructura **Variant** , establezca siempre **VT** para reflejar el miembro de Unión que contiene la información.</span><span class="sxs-lookup"><span data-stu-id="fc845-120">Similarly, when you send information using a **VARIANT** structure, always set **vt** to reflect the union member that contains the information.</span></span>

<span data-ttu-id="fc845-121">Antes de utilizar la estructura, Inicialícelo mediante una llamada a la función [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) del modelo de objetos componentes (com).</span><span class="sxs-lookup"><span data-stu-id="fc845-121">Before using the structure, initialize it by calling the [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM) function.</span></span> <span data-ttu-id="fc845-122">Cuando termine con la estructura, desactívela antes de que se libere la memoria que contiene la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) llamando a [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span><span class="sxs-lookup"><span data-stu-id="fc845-122">When finished with the structure, clear it before the memory that contains the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) is freed by calling [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).</span></span>

 

 