---
description: Inicia el Asistente para Passport cuando se usa Rundll32.exe.
title: Función PassportWizardRunDll
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
ms.openlocfilehash: 1678677bcb305b7e5c47d28f5168d1e596ca3e26
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842516"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="133c8-103">Función PassportWizardRunDll</span><span class="sxs-lookup"><span data-stu-id="133c8-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="133c8-104">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="133c8-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="133c8-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="133c8-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="133c8-106">Inicia el Asistente para Passport cuando se usa Rundll32.exe.</span><span class="sxs-lookup"><span data-stu-id="133c8-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="133c8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="133c8-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="133c8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="133c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="133c8-109">*hwndStub* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="133c8-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="133c8-110">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="133c8-110">Type: **HWND**</span></span>

<span data-ttu-id="133c8-111">Identificador de una ventana de propietario.</span><span class="sxs-lookup"><span data-stu-id="133c8-111">A handle to an owner window.</span></span> <span data-ttu-id="133c8-112">Este parámetro se establece normalmente en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="133c8-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="133c8-113">*hAppInstance* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="133c8-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="133c8-114">Tipo: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="133c8-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="133c8-115">Identificador del archivo de biblioteca, obtenido como un valor devuelto de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span><span class="sxs-lookup"><span data-stu-id="133c8-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="133c8-116">*lpszCmdLine* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="133c8-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="133c8-117">Tipo: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="133c8-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="133c8-118">Datos de argumento.</span><span class="sxs-lookup"><span data-stu-id="133c8-118">Argument data.</span></span> <span data-ttu-id="133c8-119">Este valor siempre estará vacío.</span><span class="sxs-lookup"><span data-stu-id="133c8-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="133c8-120">*nCmdShow* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="133c8-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="133c8-121">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="133c8-121">Type: **int**</span></span>

<span data-ttu-id="133c8-122">Establece el modo de presentación de la ventana.</span><span class="sxs-lookup"><span data-stu-id="133c8-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="133c8-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="133c8-123">Return value</span></span>

<span data-ttu-id="133c8-124">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="133c8-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="133c8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="133c8-125">Remarks</span></span>

<span data-ttu-id="133c8-126">El Asistente para Passport se usa para obtener un passport para Windows predeterminado.</span><span class="sxs-lookup"><span data-stu-id="133c8-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="133c8-127">Passport proporciona al usuario acceso personalizado a todos los sitios web de MSN y a otros sitios habilitados para Passport mediante la dirección de correo electrónico del usuario.</span><span class="sxs-lookup"><span data-stu-id="133c8-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="133c8-128">El uso de **PassportWizardRunDll** como punto de entrada en el archivo Netplwiz.dll mediante un comando Rundll32 permite iniciar el Asistente para Passport desde una línea de comandos como si fuera un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="133c8-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="133c8-129">**PassportWizardRunDll** se usa únicamente en el contexto de un Rundll32.exe comando como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="133c8-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="133c8-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span><span class="sxs-lookup"><span data-stu-id="133c8-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="133c8-131">El uso de una función de punto de Rundll32.exe no se parece a una llamada de función normal.</span><span class="sxs-lookup"><span data-stu-id="133c8-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="133c8-132">El nombre de la función y el nombre del archivo .dll donde se almacena solo se usan como parámetros de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="133c8-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="133c8-133">La definición de función que se muestra en Sintaxis es solo un prototipo estándar para todas las funciones a las que se puede llamar mediante Rundll32.</span><span class="sxs-lookup"><span data-stu-id="133c8-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="133c8-134">El usuario no proporciona los valores específicos de *hwndStub,* *hAppInstance* y *nCmdShow,* pero Rundll32 los controla en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="133c8-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="133c8-135">**PassportWizardRunDll** no usa el valor *lpszCmdLine,* por lo que no se requiere ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="133c8-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="133c8-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="133c8-136">Requirements</span></span>



| <span data-ttu-id="133c8-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="133c8-137">Requirement</span></span> | <span data-ttu-id="133c8-138">Value</span><span class="sxs-lookup"><span data-stu-id="133c8-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="133c8-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="133c8-139">Minimum supported client</span></span><br/> | <span data-ttu-id="133c8-140">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="133c8-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="133c8-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="133c8-141">Minimum supported server</span></span><br/> | <span data-ttu-id="133c8-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="133c8-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="133c8-143">Header</span><span class="sxs-lookup"><span data-stu-id="133c8-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="133c8-144"><dt>Ninguno</dt></span><span class="sxs-lookup"><span data-stu-id="133c8-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="133c8-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="133c8-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="133c8-146"><dt>Netplwiz.dll (versión 5.60 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="133c8-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
