---
description: Inicia el Asistente de Passport cuando se usa con Rundll32.exe.
title: PassportWizardRunDll función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: a858a36caa4af8095fc7023abae5ad918321f53e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277412"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="102f3-103">PassportWizardRunDll función)</span><span class="sxs-lookup"><span data-stu-id="102f3-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="102f3-104">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="102f3-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="102f3-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="102f3-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="102f3-106">Inicia el Asistente de Passport cuando se usa con Rundll32.exe.</span><span class="sxs-lookup"><span data-stu-id="102f3-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="102f3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="102f3-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="102f3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="102f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="102f3-109">*hwndStub* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="102f3-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="102f3-110">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="102f3-110">Type: **HWND**</span></span>

<span data-ttu-id="102f3-111">Identificador de una ventana propietaria.</span><span class="sxs-lookup"><span data-stu-id="102f3-111">A handle to an owner window.</span></span> <span data-ttu-id="102f3-112">Normalmente, este parámetro se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="102f3-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="102f3-113">*hAppInstance* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="102f3-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="102f3-114">Tipo: **hInstance**</span><span class="sxs-lookup"><span data-stu-id="102f3-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="102f3-115">Identificador del archivo de biblioteca, obtenido como valor devuelto por [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span><span class="sxs-lookup"><span data-stu-id="102f3-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="102f3-116">*lpszCmdLine* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="102f3-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="102f3-117">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="102f3-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="102f3-118">Datos de argumento.</span><span class="sxs-lookup"><span data-stu-id="102f3-118">Argument data.</span></span> <span data-ttu-id="102f3-119">Este valor siempre estará vacío.</span><span class="sxs-lookup"><span data-stu-id="102f3-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="102f3-120">*nCmdShow* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="102f3-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="102f3-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="102f3-121">Type: **int**</span></span>

<span data-ttu-id="102f3-122">Establece el modo de presentación de la ventana.</span><span class="sxs-lookup"><span data-stu-id="102f3-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="102f3-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="102f3-123">Return value</span></span>

<span data-ttu-id="102f3-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="102f3-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="102f3-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="102f3-125">Remarks</span></span>

<span data-ttu-id="102f3-126">El Asistente de Passport se usa para obtener una cuenta de Passport predeterminada para Windows.</span><span class="sxs-lookup"><span data-stu-id="102f3-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="102f3-127">Un pasaporte proporciona al usuario acceso personalizado a todos los sitios web de MSN y otros sitios habilitados para Passport mediante la dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="102f3-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="102f3-128">El uso de **PassportWizardRunDll** como punto de entrada en el archivo Netplwiz.dll a través de un comando Rundll32 le permite iniciar el Asistente de Passport desde una línea de comandos como si fuera un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="102f3-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="102f3-129">**PassportWizardRunDll** se utiliza únicamente en el contexto de un comando Rundll32.exe como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="102f3-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="102f3-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span><span class="sxs-lookup"><span data-stu-id="102f3-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="102f3-131">El uso de una función de punto de entrada con Rundll32.exe no es similar a una llamada de función normal.</span><span class="sxs-lookup"><span data-stu-id="102f3-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="102f3-132">El nombre de la función y el nombre del archivo. dll donde se almacenan solo se usan como parámetros de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="102f3-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="102f3-133">La definición de función mostrada en sintaxis es solo un prototipo estándar para todas las funciones a las que se puede llamar mediante rundll32.</span><span class="sxs-lookup"><span data-stu-id="102f3-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="102f3-134">Los valores específicos de *hwndStub*, *hAppInstance* y *nCmdShow* no son proporcionados por el usuario, sino que se administran en segundo plano mediante rundll32.</span><span class="sxs-lookup"><span data-stu-id="102f3-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="102f3-135">**PassportWizardRunDll** no usa el valor *lpszCmdLine* , por lo que no se requiere ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="102f3-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="102f3-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="102f3-136">Requirements</span></span>



| <span data-ttu-id="102f3-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="102f3-137">Requirement</span></span> | <span data-ttu-id="102f3-138">Value</span><span class="sxs-lookup"><span data-stu-id="102f3-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102f3-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="102f3-139">Minimum supported client</span></span><br/> | <span data-ttu-id="102f3-140">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="102f3-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="102f3-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="102f3-141">Minimum supported server</span></span><br/> | <span data-ttu-id="102f3-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="102f3-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="102f3-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="102f3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="102f3-144"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="102f3-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="102f3-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="102f3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="102f3-146"><dt>Netplwiz.dll (versión 5,60 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="102f3-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
