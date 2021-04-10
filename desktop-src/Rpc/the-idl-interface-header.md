---
title: El encabezado de la interfaz IDL
description: El encabezado de la interfaz IDL especifica información sobre la interfaz en su conjunto. A diferencia de ACF, el encabezado de interfaz contiene atributos que son independientes de la plataforma.
ms.assetid: 667e5228-3ea7-4910-90b9-999e6fd705e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8abce6204fdc09ed74a63a85e9366125dbef8e35
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149594"
---
# <a name="the-idl-interface-header"></a><span data-ttu-id="e171f-104">El encabezado de la interfaz IDL</span><span class="sxs-lookup"><span data-stu-id="e171f-104">The IDL Interface Header</span></span>

<span data-ttu-id="e171f-105">El encabezado de la interfaz IDL especifica información sobre la interfaz en su conjunto.</span><span class="sxs-lookup"><span data-stu-id="e171f-105">The IDL interface header specifies information about the interface as a whole.</span></span> <span data-ttu-id="e171f-106">A diferencia de ACF, el encabezado de interfaz contiene atributos que son independientes de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="e171f-106">Unlike the ACF, the interface header contains attributes that are platform-independent.</span></span>

<span data-ttu-id="e171f-107">Los atributos del encabezado de la interfaz son globales para toda la interfaz.</span><span class="sxs-lookup"><span data-stu-id="e171f-107">Attributes in the interface header are global to the entire interface.</span></span> <span data-ttu-id="e171f-108">Es decir, se aplican a la interfaz y a todas sus partes.</span><span class="sxs-lookup"><span data-stu-id="e171f-108">That is, they apply to the interface and all of its parts.</span></span> <span data-ttu-id="e171f-109">Estos atributos se incluyen entre corchetes al principio de la definición de interfaz.</span><span class="sxs-lookup"><span data-stu-id="e171f-109">These attributes are enclosed in square brackets at the beginning of the interface definition.</span></span> <span data-ttu-id="e171f-110">Un ejemplo se muestra en la siguiente definición de interfaz:</span><span class="sxs-lookup"><span data-stu-id="e171f-110">An example is shown in the following interface definition:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="e171f-111">Observe que el encabezado de la interfaz contiene los **\[** atributos [**UUID**](/windows/desktop/Midl/uuid) **\]** y **\[** [**version**](/windows/desktop/Midl/version) **\]** .</span><span class="sxs-lookup"><span data-stu-id="e171f-111">Notice that the interface header contains the **\[**[**uuid**](/windows/desktop/Midl/uuid)**\]** and **\[**[**version**](/windows/desktop/Midl/version)**\]** attributes.</span></span> <span data-ttu-id="e171f-112">Puesto que representan el UUID y el número de versión de la interfaz, respectivamente, son atributos de toda la interfaz.</span><span class="sxs-lookup"><span data-stu-id="e171f-112">Since these represent the UUID and version number of the interface respectively, they are attributes of the entire interface.</span></span>

<span data-ttu-id="e171f-113">El cuerpo de la interfaz también puede contener atributos.</span><span class="sxs-lookup"><span data-stu-id="e171f-113">The interface body can also contain attributes.</span></span> <span data-ttu-id="e171f-114">Sin embargo, no se aplican a toda la interfaz.</span><span class="sxs-lookup"><span data-stu-id="e171f-114">However, they are not applicable to the entire interface.</span></span> <span data-ttu-id="e171f-115">Hacen referencia a elementos específicos de la interfaz, como los parámetros de procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="e171f-115">They refer to specific items in the interface such as remote procedure parameters.</span></span>

<span data-ttu-id="e171f-116">Para obtener una descripción completa de los atributos del encabezado IDL, vea la [Referencia del lenguaje MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="e171f-116">For a complete discussion of the IDL header attributes, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

 

 