---
title: El encabezado ACF
description: El encabezado ACF contiene atributos específicos de la plataforma que se aplican a la interfaz en conjunto. Los atributos que se aplican a tipos y funciones individuales en el cuerpo ACF invalidan los atributos del encabezado ACF. No se requiere ningún atributo en el encabezado ACF.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078031"
---
# <a name="the-acf-header"></a><span data-ttu-id="ae0ef-105">El encabezado ACF</span><span class="sxs-lookup"><span data-stu-id="ae0ef-105">The ACF Header</span></span>

<span data-ttu-id="ae0ef-106">El encabezado ACF contiene atributos específicos de la plataforma que se aplican a la interfaz en conjunto.</span><span class="sxs-lookup"><span data-stu-id="ae0ef-106">The ACF header contains platform-specific attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="ae0ef-107">Los atributos que se aplican a tipos y funciones individuales en el cuerpo ACF invalidan los atributos del encabezado ACF.</span><span class="sxs-lookup"><span data-stu-id="ae0ef-107">Attributes applied to individual types and functions in the ACF body override the attributes in the ACF header.</span></span> <span data-ttu-id="ae0ef-108">No se requiere ningún atributo en el encabezado ACF.</span><span class="sxs-lookup"><span data-stu-id="ae0ef-108">No attributes are required in the ACF header.</span></span>

<span data-ttu-id="ae0ef-109">El encabezado ACF puede incluir uno de los siguientes atributos: **\[** [**\_ identificador automático**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**\_ identificador implícito**](/windows/desktop/Midl/implicit-handle) **\]** o [**\_ identificador explícito**](/windows/desktop/Midl/explicit-handle) **\]** .</span><span class="sxs-lookup"><span data-stu-id="ae0ef-109">The ACF header can include one of the following attributes: **\[**[**auto\_handle**](/windows/desktop/Midl/auto-handle)**\]**, **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]**, or [**explicit\_handle**](/windows/desktop/Midl/explicit-handle)**\]**.</span></span> <span data-ttu-id="ae0ef-110">Si se usa el **\[ \_ identificador \] automático** o el **\[ \_ identificador \] implícito** , especifica el tipo de identificador de enlace que se utilizará para el enlace cuando una función remota no tenga un parámetro de identificador de enlace explícito.</span><span class="sxs-lookup"><span data-stu-id="ae0ef-110">If **\[auto\_handle\]** or **\[implicit\_handle\]** is used, it specifies the type of binding handle that will be used for binding when a remote function does not have an explicit binding-handle parameter.</span></span> <span data-ttu-id="ae0ef-111">Cuando el ACF no está presente o no especifica un identificador de enlace automático, implícito o explícito, MIDL usa el **\[ \_ identificador \] automático** para el enlace implícito.</span><span class="sxs-lookup"><span data-stu-id="ae0ef-111">When the ACF is not present or does not specify an automatic, implicit, or explicit binding handle, MIDL uses **\[auto\_handle\]** for implicit binding.</span></span>

<span data-ttu-id="ae0ef-112">**\[** [](/windows/desktop/Midl/code) **\]** Puede aparecer código o **\[** [**nocode**](/windows/desktop/Midl/nocode) **\]** en el encabezado de la interfaz, pero el que elija solo puede aparecer una vez.</span><span class="sxs-lookup"><span data-stu-id="ae0ef-112">Either **\[**[**code**](/windows/desktop/Midl/code)**\]** or **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]** can appear in the interface header, but the one you choose can appear only once.</span></span> <span data-ttu-id="ae0ef-113">Cuando no hay ningún atributo, el compilador utiliza el **\[ código \]** como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ae0ef-113">When neither attribute is present, the compiler uses **\[code\]** as a default.</span></span>

<span data-ttu-id="ae0ef-114">Para obtener más información, consulte [atributos ACF](/windows/desktop/Midl/acf-attributes).</span><span class="sxs-lookup"><span data-stu-id="ae0ef-114">For more information, see [ACF Attributes](/windows/desktop/Midl/acf-attributes).</span></span>

 

 