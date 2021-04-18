---
title: Obtener acceso a una vista del registro alternativa
description: De forma predeterminada, una aplicación de 32 bits que se ejecuta en WOW64 accede a la vista del Registro de 32 bits, y una aplicación de 64 bits accede a la vista del Registro de 64 bits.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- vistas del registro de la programación de Windows de 64 bits
- La programación de Windows de 64 bits de WOW64, vistas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/09/2021
ms.locfileid: "105707504"
---
# <a name="accessing-an-alternate-registry-view"></a><span data-ttu-id="5dd9f-105">Obtener acceso a una vista del registro alternativa</span><span class="sxs-lookup"><span data-stu-id="5dd9f-105">Accessing an Alternate Registry View</span></span>

<span data-ttu-id="5dd9f-106">De forma predeterminada, una aplicación de 32 bits que se ejecuta en WOW64 accede a la vista del Registro de 32 bits, y una aplicación de 64 bits accede a la vista del Registro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-106">By default, a 32-bit application running on WOW64 accesses the 32-bit registry view and a 64-bit application accesses the 64-bit registry view.</span></span> <span data-ttu-id="5dd9f-107">Los siguientes marcadores permiten a las aplicaciones de 32 bits tener acceso a las claves redirigidas en la vista del registro de 64 bits y las aplicaciones de 64 bits para tener acceso a las claves redirigidas en la vista del registro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-107">The following flags enable 32-bit applications to access redirected keys in the 64-bit registry view and 64-bit applications to access redirected keys in the 32-bit registry view.</span></span> <span data-ttu-id="5dd9f-108">Estas marcas no tienen ningún efecto en las claves del registro compartidas.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-108">These flags have no effect on shared registry keys.</span></span> <span data-ttu-id="5dd9f-109">Para obtener más información, consulte [claves del registro afectadas por WOW64](shared-registry-keys.md).</span><span class="sxs-lookup"><span data-stu-id="5dd9f-109">For more information, see [Registry Keys Affected by WOW64](shared-registry-keys.md).</span></span>



| <span data-ttu-id="5dd9f-110">Nombre del marcador</span><span class="sxs-lookup"><span data-stu-id="5dd9f-110">Flag name</span></span>         | <span data-ttu-id="5dd9f-111">Value</span><span class="sxs-lookup"><span data-stu-id="5dd9f-111">Value</span></span>  | <span data-ttu-id="5dd9f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dd9f-112">Description</span></span>                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5dd9f-113">CLAVE \_ WOW64 \_ 64KEY</span><span class="sxs-lookup"><span data-stu-id="5dd9f-113">KEY\_WOW64\_64KEY</span></span> | <span data-ttu-id="5dd9f-114">0x0100</span><span class="sxs-lookup"><span data-stu-id="5dd9f-114">0x0100</span></span> | <span data-ttu-id="5dd9f-115">Obtenga acceso a una clave de 64 bits desde una aplicación de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-115">Access a 64-bit key from either a 32-bit or 64-bit application.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="5dd9f-116">CLAVE \_ WOW64 \_ 32KEY</span><span class="sxs-lookup"><span data-stu-id="5dd9f-116">KEY\_WOW64\_32KEY</span></span> | <span data-ttu-id="5dd9f-117">0x0200</span><span class="sxs-lookup"><span data-stu-id="5dd9f-117">0x0200</span></span> | <span data-ttu-id="5dd9f-118">Obtenga acceso a una clave de 32 bits desde una aplicación de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-118">Access a 32-bit key from either a 32-bit or 64-bit application.</span></span><br/><span data-ttu-id="5dd9f-119">**Windows 10 en ARM:** Esto hace referencia a la vista del registro de ARM de 32 bits para los procesos ARM de 32 bits y la vista del registro x86 de 32 bits para los procesos de ARM64 de 32 bits x86 y de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-119">**Windows 10 on ARM:** This refers to the 32-bit ARM registry view for 32-bit ARM processes and the 32-bit x86 registry view for 32-bit x86 and 64-bit ARM64 processes.</span></span> |



 

<span data-ttu-id="5dd9f-120">Estas marcas se pueden especificar en el parámetro *samDesired* de las siguientes funciones del registro:</span><span class="sxs-lookup"><span data-stu-id="5dd9f-120">These flags can be specified in the *samDesired* parameter of the following registry functions:</span></span>

-   [<span data-ttu-id="5dd9f-121">**RegCreateKeyEx**</span><span class="sxs-lookup"><span data-stu-id="5dd9f-121">**RegCreateKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [<span data-ttu-id="5dd9f-122">**RegDeleteKeyEx**</span><span class="sxs-lookup"><span data-stu-id="5dd9f-122">**RegDeleteKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [<span data-ttu-id="5dd9f-123">**RegOpenKeyEx**</span><span class="sxs-lookup"><span data-stu-id="5dd9f-123">**RegOpenKeyEx**</span></span>](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

<span data-ttu-id="5dd9f-124">\_Se puede especificar la clave WOW64 \_ 32KEY o la clave \_ WOW64 \_ 64KEY</span><span class="sxs-lookup"><span data-stu-id="5dd9f-124">Either KEY\_WOW64\_32KEY or KEY\_WOW64\_64KEY can be specified.</span></span> <span data-ttu-id="5dd9f-125">Si se especifican ambas marcas, se produce un ERROR en la función con un \_ parámetro no válido \_ .</span><span class="sxs-lookup"><span data-stu-id="5dd9f-125">If both flags are specified, the function fails with ERROR\_INVALID\_PARAMETER.</span></span>

<span data-ttu-id="5dd9f-126">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Si se especifican ambas marcas, el comportamiento de la función es indefinido.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-126">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** If both flags are specified, the function s behavior is undefined.</span></span>

<span data-ttu-id="5dd9f-127">No se puede usar la función [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) para tener acceso a una vista del registro alternativa.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-127">The [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) function cannot be used to access an alternate registry view.</span></span>

<span data-ttu-id="5dd9f-128">A continuación se muestran los procedimientos recomendados para obtener acceso al registro desde una aplicación:</span><span class="sxs-lookup"><span data-stu-id="5dd9f-128">The following are best practices when accessing the registry from an application:</span></span>

-   <span data-ttu-id="5dd9f-129">Una vez que la aplicación ha tenido acceso a una vista del registro alternativa mediante una de las marcas, todas las operaciones subsiguientes (crear, eliminar o abrir) en las claves del registro secundarias deben usar explícitamente la misma marca.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-129">After the application has accessed an alternate registry view using one of the flags, all subsequent operations (create, delete, or open) on child registry keys must explicitly use the same flag.</span></span> <span data-ttu-id="5dd9f-130">De lo contrario, puede haber un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-130">Otherwise, there can be unexpected behavior.</span></span>
-   <span data-ttu-id="5dd9f-131">Para enumerar con precisión todas las claves en ambas vistas, realice la enumeración en dos pasos.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-131">To accurately enumerate all keys in both views, perform the enumeration in two passes.</span></span> <span data-ttu-id="5dd9f-132">El primer paso debe utilizar un identificador abierto con una de las marcas y el otro paso debe usar un identificador abierto con la otra marca.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-132">The first pass should use a handle opened with one of the flags, and the other pass should use a handle opened with the other flag.</span></span>

> [!Note]  
> <span data-ttu-id="5dd9f-133">Las claves **Wow6432Node** y **WowAA32Node** están reservadas.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-133">The **Wow6432Node** and **WowAA32Node** keys are reserved.</span></span> <span data-ttu-id="5dd9f-134">Por compatibilidad, las aplicaciones no deben usar estas claves directamente.</span><span class="sxs-lookup"><span data-stu-id="5dd9f-134">For compatibility, applications should not use these keys directly.</span></span>

 

<span data-ttu-id="5dd9f-135">Para obtener información sobre cómo obtener acceso a la vista del registro alternativa a través de WMI, consulte [solicitar datos WMI en una plataforma de 64 bits](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span><span class="sxs-lookup"><span data-stu-id="5dd9f-135">For information about accessing the alternate registry view through WMI, see [Requesting WMI Data on a 64-bit Platform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dd9f-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5dd9f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dd9f-137">Redirector del registro</span><span class="sxs-lookup"><span data-stu-id="5dd9f-137">Registry Redirector</span></span>](registry-redirector.md)
</dt> <dt>

[<span data-ttu-id="5dd9f-138">Reflexión del registro</span><span class="sxs-lookup"><span data-stu-id="5dd9f-138">Registry Reflection</span></span>](registry-reflection.md)
</dt> </dl>

 

