---
title: Errores comunes (ADSI)
description: Todos los errores específicos de ADSI tienen una forma hexadecimal de 80005xxx. Los códigos de error más comunes que se encuentran se describen en la tabla siguiente.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "104358600"
---
# <a name="common-errors-adsi"></a><span data-ttu-id="6519c-104">Errores comunes (ADSI)</span><span class="sxs-lookup"><span data-stu-id="6519c-104">Common Errors (ADSI)</span></span>

<span data-ttu-id="6519c-105">Todos los errores específicos de ADSI tienen una forma hexadecimal de 80005xxx.</span><span class="sxs-lookup"><span data-stu-id="6519c-105">All ADSI-specific errors have a hexadecimal form of 80005xxx.</span></span> <span data-ttu-id="6519c-106">Los códigos de error más comunes que se encuentran se describen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6519c-106">The most common error codes encountered are outlined in the following table.</span></span>



| <span data-ttu-id="6519c-107">Código de error hexadecimal ADSI</span><span class="sxs-lookup"><span data-stu-id="6519c-107">ADSI hex error code</span></span> | <span data-ttu-id="6519c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="6519c-108">Description</span></span>                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6519c-109">80005000</span><span class="sxs-lookup"><span data-stu-id="6519c-109">80005000</span></span><br/> | <span data-ttu-id="6519c-110">Se pasó un nombreruta de ADSI no válido.</span><span class="sxs-lookup"><span data-stu-id="6519c-110">An invalid ADSI pathname was passed.</span></span> <span data-ttu-id="6519c-111">Este error se produce al pasar un ADsPath con un formato incorrecto a **GetObject** al enlazar a un objeto.</span><span class="sxs-lookup"><span data-stu-id="6519c-111">This error results from passing a poorly formed ADsPath to **GetObject** when binding to an object.</span></span><br/> |
| <span data-ttu-id="6519c-112">8000500D</span><span class="sxs-lookup"><span data-stu-id="6519c-112">8000500D</span></span><br/> | <span data-ttu-id="6519c-113">No se encuentra la propiedad ADSI en la caché de propiedades.</span><span class="sxs-lookup"><span data-stu-id="6519c-113">The ADSI property cannot be found in the property cache.</span></span><br/>                                                                                 |
| <span data-ttu-id="6519c-114">8000500E</span><span class="sxs-lookup"><span data-stu-id="6519c-114">8000500E</span></span><br/> | <span data-ttu-id="6519c-115">El objeto ADSI existe.</span><span class="sxs-lookup"><span data-stu-id="6519c-115">The ADSI object exists.</span></span> <span data-ttu-id="6519c-116">Si intenta crear un objeto ADSI con el mismo nombre que un objeto ADSI existente, se producirá este error.</span><span class="sxs-lookup"><span data-stu-id="6519c-116">If you attempt to create an ADSI object with the same name as an existing ADSI object, this error will occur.</span></span><br/>    |



 

<span data-ttu-id="6519c-117">Para obtener una lista completa de los códigos de error ADSI, consulte [códigos de error ADSI genéricos](generic-adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6519c-117">For a complete list of ADSI error codes, see [Generic ADSI Error Codes](generic-adsi-error-codes.md).</span></span>

## <a name="com-errors"></a><span data-ttu-id="6519c-118">Errores COM</span><span class="sxs-lookup"><span data-stu-id="6519c-118">COM Errors</span></span>

<span data-ttu-id="6519c-119">Como ADSI se compone de objetos COM, devolverá códigos de error COM estándar.</span><span class="sxs-lookup"><span data-stu-id="6519c-119">Since ADSI is composed of COM objects, it will return standard COM error codes.</span></span> <span data-ttu-id="6519c-120">En la tabla siguiente se enumeran los códigos de error COM que se encuentran normalmente en la programación ADSI.</span><span class="sxs-lookup"><span data-stu-id="6519c-120">The following table lists the COM error codes most commonly encountered in ADSI programming.</span></span>



| <span data-ttu-id="6519c-121">Código de error hexadecimal COM</span><span class="sxs-lookup"><span data-stu-id="6519c-121">COM hex error code</span></span>  | <span data-ttu-id="6519c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6519c-122">Description</span></span>                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6519c-123">80004005</span><span class="sxs-lookup"><span data-stu-id="6519c-123">80004005</span></span><br/> | <span data-ttu-id="6519c-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="6519c-124">Unspecified error.</span></span> <span data-ttu-id="6519c-125">La causa del error del objeto COM es indeterminada en ADSI.</span><span class="sxs-lookup"><span data-stu-id="6519c-125">The cause of the COM object failure is indeterminate by ADSI.</span></span> <br/>                                  |
| <span data-ttu-id="6519c-126">800041E4</span><span class="sxs-lookup"><span data-stu-id="6519c-126">800041E4</span></span><br/> | <span data-ttu-id="6519c-127">Objeto no encontrado.</span><span class="sxs-lookup"><span data-stu-id="6519c-127">Object not found.</span></span> <span data-ttu-id="6519c-128">Este error se produce principalmente debido a la escritura incorrecta de la cadena ADsPath al enlazar con un objeto.</span><span class="sxs-lookup"><span data-stu-id="6519c-128">This error predominantly occurs due to misspelling the ADsPath string when binding to an object.</span></span><br/> |



 

<span data-ttu-id="6519c-129">Consulte [códigos de error com genéricos](generic-com-error-codes.md) para ver algunos ejemplos de errores com que pueden producirse en la programación ADSI.</span><span class="sxs-lookup"><span data-stu-id="6519c-129">See [Generic COM Error Codes](generic-com-error-codes.md) for a few more examples of COM errors that may occur in ADSI programming.</span></span>

## <a name="win32-errors"></a><span data-ttu-id="6519c-130">Errores de Win32</span><span class="sxs-lookup"><span data-stu-id="6519c-130">Win32 Errors</span></span>

<span data-ttu-id="6519c-131">Cualquier código de error del formato hexadecimal 8007xxxx es un código de error estándar de Win32.</span><span class="sxs-lookup"><span data-stu-id="6519c-131">Any error code of the hexadecimal form 8007xxxx is a standard Win32 error code.</span></span> <span data-ttu-id="6519c-132">Si convierte los cuatro últimos dígitos de hexadecimal a decimal, puede tener acceso al error desde la línea de comandos de Windows 2000:</span><span class="sxs-lookup"><span data-stu-id="6519c-132">If you convert the last four digits from hexadecimal to decimal, you can access the error from the Windows 2000 command line:</span></span>

<span data-ttu-id="6519c-133">**net helpmsg <number>**</span><span class="sxs-lookup"><span data-stu-id="6519c-133">**net helpmsg <number>**</span></span>

<span data-ttu-id="6519c-134">En la línea de comandos anterior, " &lt; número &gt; " es el número decimal obtenido al convertir los cuatro últimos dígitos del código de error de hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="6519c-134">In the command line above, "&lt;number&gt;" is the decimal number obtained by converting the last four digits of the error code from hexadecimal.</span></span> <span data-ttu-id="6519c-135">Esta línea de comandos proporcionará una descripción más útil del error de Win32, que puede ser de gran ayuda para depurar el script.</span><span class="sxs-lookup"><span data-stu-id="6519c-135">This command line will provide a more useful description of the Win32 error, which can be of great help in debugging your script.</span></span>

 

 





