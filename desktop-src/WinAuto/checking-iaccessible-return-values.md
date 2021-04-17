---
title: Comprobar los valores devueltos de IAccessible
description: Los desarrolladores de cliente no deben confiar en las macros del modelo de objetos componentes (COM) correctas y no pudieron probar los valores devueltos del IAccessible, ya que los valores que no \_ son correctos se consideran correctos.
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714417"
---
# <a name="checking-iaccessible-return-values"></a><span data-ttu-id="51a4c-103">Comprobar los valores devueltos de IAccessible</span><span class="sxs-lookup"><span data-stu-id="51a4c-103">Checking IAccessible Return Values</span></span>

<span data-ttu-id="51a4c-104">Los desarrolladores de cliente no deben confiar en las macros del modelo de objetos componentes (COM) [**correctas**](/windows/desktop/api/winerror/nf-winerror-succeeded) y [**no pudieron**](/windows/desktop/api/winerror/nf-winerror-failed) probar los valores devueltos del [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , ya que los valores que no \_ son correctos se consideran correctos.</span><span class="sxs-lookup"><span data-stu-id="51a4c-104">Client developers should not rely on the Component Object Model (COM) macros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) to test [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) return values, because values other than S\_OK are considered a success.</span></span> <span data-ttu-id="51a4c-105">Por ejemplo, un método puede devolver S \_ false, lo que se considera que es correcto por la macro **Succeeded** , pero sigue recibiendo un puntero **null** en un parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="51a4c-105">For example, a method can return S\_FALSE, which is considered a success by the **SUCCEEDED** macro, but still receive a **NULL** pointer in an output parameter.</span></span>

<span data-ttu-id="51a4c-106">Los desarrolladores de cliente deben protegerse frente a la posibilidad de que algunos servidores devuelvan códigos de error distintos de los valores documentados.</span><span class="sxs-lookup"><span data-stu-id="51a4c-106">Client developers must guard against the possibility that some servers return error codes other than the documented values.</span></span> <span data-ttu-id="51a4c-107">Para que sea seguro, debe asegurarse de que todos los parámetros de salida contienen información válida y cumplen los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="51a4c-107">To be safe, you must ensure that all the output parameters contain valid information and meet the following criteria:</span></span>

-   <span data-ttu-id="51a4c-108">Todos los punteros no son **null**.</span><span class="sxs-lookup"><span data-stu-id="51a4c-108">All pointers are non-**NULL**.</span></span>
-   <span data-ttu-id="51a4c-109">El miembro **VT** de cualquier estructura [Variant](/windows/win32/api/oaidl/ns-oaidl-variant) no es igual a VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="51a4c-109">The **vt** member of any [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) structure is not equal to VT\_EMPTY.</span></span>

 

 