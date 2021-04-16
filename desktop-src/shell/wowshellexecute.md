---
description: Realiza una operación en un archivo especificado.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: WOWShellExecute función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: ae50ad570211303cdfb7aa8e86908593ab48537d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187806"
---
# <a name="wowshellexecute-function"></a><span data-ttu-id="6f485-103">WOWShellExecute función)</span><span class="sxs-lookup"><span data-stu-id="6f485-103">WOWShellExecute function</span></span>

<span data-ttu-id="6f485-104">\[Esta función está disponible a través de Windows XP con Service Pack 2 (SP2) y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6f485-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="6f485-105">Podría modificarse o no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6f485-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="6f485-106">Realiza una operación en un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6f485-106">Performs an operation on a specified file.</span></span> <span data-ttu-id="6f485-107">**WOWShellExecute** solo existe para su uso con la máquina virtual dos de Microsoft Windows NT (Ntvdm.exe), que permite que el sistema operativo de disco (dos) y el software de 16 bits se ejecuten en un sistema de Windows y no debe usarlos nadie más.</span><span class="sxs-lookup"><span data-stu-id="6f485-107">**WOWShellExecute** exists only for use with the Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe), which allows disk operating system (DOS) and 16-bit software to run on a Windows system, and should not be used by anyone else.</span></span> <span data-ttu-id="6f485-108">En su lugar, use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="6f485-108">Use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f485-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f485-109">Syntax</span></span>


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a><span data-ttu-id="6f485-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f485-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f485-111">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f485-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f485-112">Tipo: **hWnd**</span><span class="sxs-lookup"><span data-stu-id="6f485-112">Type: **HWND**</span></span>

<span data-ttu-id="6f485-113">Identificador de la ventana propietaria que se usa para mostrar una interfaz de usuario o mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="6f485-113">A handle to the owner window used for displaying a UI or error messages.</span></span> <span data-ttu-id="6f485-114">Este valor puede ser **null** si la operación no está asociada a una ventana.</span><span class="sxs-lookup"><span data-stu-id="6f485-114">This value can be **NULL** if the operation is not associated with a window.</span></span>

</dd> <dt>

<span data-ttu-id="6f485-115">*lpOperation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f485-115">*lpOperation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f485-116">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="6f485-116">Type: **LPCTSTR**</span></span>

<span data-ttu-id="6f485-117">Puntero a una cadena terminada en **null**, a la que se hace referencia en este caso como *verbo*, que especifica la acción que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="6f485-117">A pointer to a **null**-terminated string, referred to in this case as a *verb*, that specifies the action to be performed.</span></span> <span data-ttu-id="6f485-118">El conjunto de verbos disponibles depende del archivo o la carpeta determinados.</span><span class="sxs-lookup"><span data-stu-id="6f485-118">The set of available verbs depends on the particular file or folder.</span></span> <span data-ttu-id="6f485-119">Por lo general, las acciones disponibles en el menú contextual de un objeto son verbos disponibles.</span><span class="sxs-lookup"><span data-stu-id="6f485-119">Generally, the actions available from an object's shortcut menu are available verbs.</span></span> <span data-ttu-id="6f485-120">Para obtener más información sobre los verbos y su disponibilidad, vea la sección *verbos de objetos* de [Launching Applications](launch.md).</span><span class="sxs-lookup"><span data-stu-id="6f485-120">For more information about verbs and their availability, see the *Object Verbs* section of [Launching Applications](launch.md).</span></span> <span data-ttu-id="6f485-121">Vea [extender menús contextuales](context.md) para obtener más información sobre los menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="6f485-121">See [Extending Shortcut Menus](context.md) for further discussion of shortcut menus.</span></span> <span data-ttu-id="6f485-122">Normalmente se utilizan los siguientes verbos.</span><span class="sxs-lookup"><span data-stu-id="6f485-122">The following verbs are commonly used.</span></span>

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span data-ttu-id="6f485-123"><span id="edit"></span><span id="EDIT"></span>**editar**</span><span class="sxs-lookup"><span data-stu-id="6f485-123"><span id="edit"></span><span id="EDIT"></span>**edit**</span></span>


</dt> <dd>

<span data-ttu-id="6f485-124">Inicia un editor y abre el documento para su edición.</span><span class="sxs-lookup"><span data-stu-id="6f485-124">Launches an editor and opens the document for editing.</span></span> <span data-ttu-id="6f485-125">Si *lpFile* no es un archivo de documento, se producirá un error en la función.</span><span class="sxs-lookup"><span data-stu-id="6f485-125">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span data-ttu-id="6f485-126"><span id="explore"></span><span id="EXPLORE"></span>**visite**</span><span class="sxs-lookup"><span data-stu-id="6f485-126"><span id="explore"></span><span id="EXPLORE"></span>**explore**</span></span>


</dt> <dd>

<span data-ttu-id="6f485-127">Explora la carpeta especificada por *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="6f485-127">Explores the folder specified by *lpFile*.</span></span>

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span data-ttu-id="6f485-128"><span id="find"></span><span id="FIND"></span>**localización**</span><span class="sxs-lookup"><span data-stu-id="6f485-128"><span id="find"></span><span id="FIND"></span>**find**</span></span>


</dt> <dd>

<span data-ttu-id="6f485-129">Inicia una búsqueda a partir del directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="6f485-129">Initiates a search starting from the specified directory.</span></span>

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span data-ttu-id="6f485-130"><span id="open"></span><span id="OPEN"></span>**Ábra**</span><span class="sxs-lookup"><span data-stu-id="6f485-130"><span id="open"></span><span id="OPEN"></span>**open**</span></span>


</dt> <dd>

<span data-ttu-id="6f485-131">Abre el archivo especificado por el parámetro *lpFile* .</span><span class="sxs-lookup"><span data-stu-id="6f485-131">Opens the file specified by the *lpFile* parameter.</span></span> <span data-ttu-id="6f485-132">El archivo puede ser un archivo ejecutable, un archivo de documento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="6f485-132">The file can be an executable file, a document file, or a folder.</span></span>

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="6f485-133"><span id="print"></span><span id="PRINT"></span>**imprime**</span><span class="sxs-lookup"><span data-stu-id="6f485-133"><span id="print"></span><span id="PRINT"></span>**print**</span></span>


</dt> <dd>

<span data-ttu-id="6f485-134">Imprime el archivo de documento especificado por *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="6f485-134">Prints the document file specified by *lpFile*.</span></span> <span data-ttu-id="6f485-135">Si *lpFile* no es un archivo de documento, se producirá un error en la función.</span><span class="sxs-lookup"><span data-stu-id="6f485-135">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span data-ttu-id="6f485-136"><span id="NULL"></span><span id="null"></span>**ACEPTA**</span><span class="sxs-lookup"><span data-stu-id="6f485-136"><span id="NULL"></span><span id="null"></span>**NULL**</span></span>


</dt> <dd>

<span data-ttu-id="6f485-137">En sistemas anteriores a Windows 2000, se utiliza el verbo predeterminado si es válido y está disponible en el registro.</span><span class="sxs-lookup"><span data-stu-id="6f485-137">For systems prior to Windows 2000, the default verb is used if it is valid and available in the registry.</span></span> <span data-ttu-id="6f485-138">Si no es así, se utiliza el verbo "abrir".</span><span class="sxs-lookup"><span data-stu-id="6f485-138">If not, the "open" verb is used.</span></span>

<span data-ttu-id="6f485-139">En el caso de los sistemas Windows 2000 y versiones posteriores, se utiliza el verbo predeterminado si está disponible.</span><span class="sxs-lookup"><span data-stu-id="6f485-139">For Windows 2000 and later systems, the default verb is used if available.</span></span> <span data-ttu-id="6f485-140">Si no es así, se utiliza el verbo "abrir".</span><span class="sxs-lookup"><span data-stu-id="6f485-140">If not, the "open" verb is used.</span></span> <span data-ttu-id="6f485-141">Si no hay ningún verbo disponible, el sistema utiliza el primer verbo enumerado en el registro.</span><span class="sxs-lookup"><span data-stu-id="6f485-141">If neither verb is available, the system uses the first verb listed in the registry.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6f485-142">*lpFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f485-142">*lpFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f485-143">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="6f485-143">Type: **LPCTSTR**</span></span>

<span data-ttu-id="6f485-144">Puntero a una cadena terminada en **null** que especifica el archivo o el objeto en el que se va a ejecutar el verbo especificado.</span><span class="sxs-lookup"><span data-stu-id="6f485-144">A pointer to a **null**-terminated string that specifies the file or object on which to execute the specified verb.</span></span> <span data-ttu-id="6f485-145">Para especificar un objeto de espacio de nombres de Shell, pase el nombre de análisis completo.</span><span class="sxs-lookup"><span data-stu-id="6f485-145">To specify a Shell namespace object, pass the fully qualified parse name.</span></span> <span data-ttu-id="6f485-146">Tenga en cuenta que no todos los verbos se admiten en todos los objetos.</span><span class="sxs-lookup"><span data-stu-id="6f485-146">Note that not all verbs are supported on all objects.</span></span> <span data-ttu-id="6f485-147">Por ejemplo, no todos los tipos de documentos admiten el verbo "Imprimir".</span><span class="sxs-lookup"><span data-stu-id="6f485-147">For example, not all document types support the "print" verb.</span></span>

</dd> <dt>

<span data-ttu-id="6f485-148">*lpParameters* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f485-148">*lpParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f485-149">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="6f485-149">Type: **LPCTSTR**</span></span>

<span data-ttu-id="6f485-150">Si el parámetro *lpFile* especifica un archivo ejecutable, *lpParameters* es un puntero a una cadena terminada en **null** que especifica los parámetros que se van a pasar a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6f485-150">If the *lpFile* parameter specifies an executable file, *lpParameters* is a pointer to a **null**-terminated string that specifies the parameters to be passed to the application.</span></span> <span data-ttu-id="6f485-151">El formato de esta cadena viene determinado por el verbo que se va a invocar.</span><span class="sxs-lookup"><span data-stu-id="6f485-151">The format of this string is determined by the verb that is to be invoked.</span></span> <span data-ttu-id="6f485-152">Si *lpFile* especifica un archivo de documento, *LpParameters* debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="6f485-152">If *lpFile* specifies a document file, *lpParameters* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6f485-153">*lpDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f485-153">*lpDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f485-154">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="6f485-154">Type: **LPCTSTR**</span></span>

<span data-ttu-id="6f485-155">Puntero a una cadena terminada en **null** que especifica el directorio predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6f485-155">A pointer to a **null**-terminated string that specifies the default directory.</span></span>

</dd> <dt>

<span data-ttu-id="6f485-156">*nShowCmd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6f485-156">*nShowCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f485-157">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="6f485-157">Type: **INT**</span></span>

<span data-ttu-id="6f485-158">Marcas que especifican cómo se va a mostrar una aplicación cuando se abre.</span><span class="sxs-lookup"><span data-stu-id="6f485-158">The flags that specify how an application is to be displayed when it is opened.</span></span> <span data-ttu-id="6f485-159">Si *lpFile* especifica un archivo de documento, la marca simplemente se pasa a la aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="6f485-159">If *lpFile* specifies a document file, the flag is simply passed to the associated application.</span></span> <span data-ttu-id="6f485-160">Depende de la aplicación decidir cómo controlarla.</span><span class="sxs-lookup"><span data-stu-id="6f485-160">It is up to the application to decide how to handle it.</span></span> <span data-ttu-id="6f485-161">Puede ser cualquiera de los valores que se pueden especificar en el parámetro *nCmdShow* para la función [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="6f485-161">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="6f485-162">*lpfnCBWinExec*</span><span class="sxs-lookup"><span data-stu-id="6f485-162">*lpfnCBWinExec*</span></span> 
</dt> <dd>

<span data-ttu-id="6f485-163">Tipo: **void \***</span><span class="sxs-lookup"><span data-stu-id="6f485-163">Type: **void\***</span></span>

<span data-ttu-id="6f485-164">Función de devolución de llamada que se usa para llamar a [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) en el kernel de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6f485-164">Callback function used to call [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in the 16-bit kernel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f485-165">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f485-165">Return value</span></span>

<span data-ttu-id="6f485-166">Tipo: **hInstance**</span><span class="sxs-lookup"><span data-stu-id="6f485-166">Type: **HINSTANCE**</span></span>

<span data-ttu-id="6f485-167">Devuelve un valor mayor que 32 si es correcto, o un valor de error menor o igual que 32 en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6f485-167">Returns a value greater than 32 if successful, or an error value that is less than or equal to 32 otherwise.</span></span> <span data-ttu-id="6f485-168">En la tabla siguiente se enumeran los valores de error.</span><span class="sxs-lookup"><span data-stu-id="6f485-168">The following table lists the error values.</span></span> <span data-ttu-id="6f485-169">El valor devuelto se convierte en un HINSTANCE para la compatibilidad con versiones anteriores de aplicaciones Windows de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6f485-169">The return value is cast as an HINSTANCE for backward compatibility with 16-bit Windows applications.</span></span> <span data-ttu-id="6f485-170">Sin embargo, no es un HINSTANCE verdadero.</span><span class="sxs-lookup"><span data-stu-id="6f485-170">It is not a true HINSTANCE, however.</span></span> <span data-ttu-id="6f485-171">Lo único que se puede hacer con el HINSTANCE devuelto es convertirlo en un **int** y compararlo con el valor 32 o con uno de los códigos de error siguientes.</span><span class="sxs-lookup"><span data-stu-id="6f485-171">The only thing that can be done with the returned HINSTANCE is to cast it to an **int** and compare it with the value 32 or one of the error codes below.</span></span>



| <span data-ttu-id="6f485-172">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6f485-172">Return code</span></span>                                                                                             | <span data-ttu-id="6f485-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f485-173">Description</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f485-174"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-174"><dt>**0**</dt></span></span> </dl>                        | <span data-ttu-id="6f485-175">El sistema operativo no tiene memoria o recursos.</span><span class="sxs-lookup"><span data-stu-id="6f485-175">The operating system is out of memory or resources.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="6f485-176"><dt>**\_ \_ no \_ se encontró el archivo de error**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-176"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="6f485-177">No se encontró el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6f485-177">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="6f485-178"><dt>**\_ \_ no \_ se encontró la ruta de error**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-178"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="6f485-179">No se encontró la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="6f485-179">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="6f485-180"><dt>**ERROR \_ de \_ formato incorrecto**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-180"><dt>**ERROR\_BAD\_FORMAT**</dt></span></span> </dl>       | <span data-ttu-id="6f485-181">El archivo. exe no es válido (no es Win32. exe o error en la imagen. exe).</span><span class="sxs-lookup"><span data-stu-id="6f485-181">The .exe file is invalid (non-Win32 .exe or error in .exe image).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="6f485-182"><dt>**\_error de \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-182"><dt>**SE\_ERR\_ACCESSDENIED**</dt></span></span> </dl>    | <span data-ttu-id="6f485-183">El sistema operativo denegó el acceso al archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6f485-183">The operating system denied access to the specified file.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="6f485-184"><dt>**\_error de \_ ASSOCINCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-184"><dt>**SE\_ERR\_ASSOCINCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="6f485-185">La Asociación de nombre de archivo está incompleta o no es válida.</span><span class="sxs-lookup"><span data-stu-id="6f485-185">The file name association is incomplete or invalid.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="6f485-186"><dt>**\_error de \_ DDEBUSY**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-186"><dt>**SE\_ERR\_DDEBUSY**</dt></span></span> </dl>         | <span data-ttu-id="6f485-187">No se pudo completar la transacción DDE porque se estaban procesando otras transacciones DDE.</span><span class="sxs-lookup"><span data-stu-id="6f485-187">The DDE transaction could not be completed because other DDE transactions were being processed.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="6f485-188"><dt>**\_error de \_ DDEFAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-188"><dt>**SE\_ERR\_DDEFAIL**</dt></span></span> </dl>         | <span data-ttu-id="6f485-189">Error en la transacción DDE.</span><span class="sxs-lookup"><span data-stu-id="6f485-189">The DDE transaction failed.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="6f485-190"><dt>**\_error de \_ DDETIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-190"><dt>**SE\_ERR\_DDETIMEOUT**</dt></span></span> </dl>      | <span data-ttu-id="6f485-191">No se pudo completar la transacción DDE porque se agotó el tiempo de espera de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f485-191">The DDE transaction could not be completed because the request timed out.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="6f485-192"><dt>**\_error de \_ DLLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-192"><dt>**SE\_ERR\_DLLNOTFOUND**</dt></span></span> </dl>     | <span data-ttu-id="6f485-193">No se encontró la DLL especificada.</span><span class="sxs-lookup"><span data-stu-id="6f485-193">The specified DLL was not found.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="6f485-194"><dt>**\_error de \_ FNF**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-194"><dt>**SE\_ERR\_FNF**</dt></span></span> </dl>             | <span data-ttu-id="6f485-195">No se encontró el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="6f485-195">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="6f485-196"><dt>**SE ha $ \_ \_ Assoc**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-196"><dt>**SE\_ERR\_NOASSOC**</dt></span></span> </dl>         | <span data-ttu-id="6f485-197">No hay ninguna aplicación asociada a la extensión de nombre de archivo especificada.</span><span class="sxs-lookup"><span data-stu-id="6f485-197">There is no application associated with the given file name extension.</span></span> <span data-ttu-id="6f485-198">También se devolverá este error si intenta imprimir un archivo que no se puede imprimir.</span><span class="sxs-lookup"><span data-stu-id="6f485-198">This error will also be returned if you attempt to print a file that is not printable.</span></span><br/> |
| <dl> <span data-ttu-id="6f485-199"><dt>**\_error de \_ OOM**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-199"><dt>**SE\_ERR\_OOM**</dt></span></span> </dl>             | <span data-ttu-id="6f485-200">No había memoria suficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="6f485-200">There was not enough memory to complete the operation.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="6f485-201"><dt>**SE \_ Err error \_ PNF**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-201"><dt>**SE\_ERR\_PNF**</dt></span></span> </dl>             | <span data-ttu-id="6f485-202">No se encontró la ruta de acceso especificada.</span><span class="sxs-lookup"><span data-stu-id="6f485-202">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="6f485-203"><dt>**\_recurso compartido de error se \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-203"><dt>**SE\_ERR\_SHARE**</dt></span></span> </dl>           | <span data-ttu-id="6f485-204">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="6f485-204">A sharing violation occurred.</span></span><br/>                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="6f485-205">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f485-205">Remarks</span></span>

<span data-ttu-id="6f485-206">**WOWShellExecute** no se incluye en un archivo de encabezado o. lib.</span><span class="sxs-lookup"><span data-stu-id="6f485-206">**WOWShellExecute** is not included in a header or .lib file.</span></span> <span data-ttu-id="6f485-207">Se exporta desde Shell32.dll por nombre.</span><span class="sxs-lookup"><span data-stu-id="6f485-207">It is exported from Shell32.dll by name.</span></span>

<span data-ttu-id="6f485-208">Este método permite ejecutar cualquier comando en el menú contextual de una carpeta o almacenarlo en el registro.</span><span class="sxs-lookup"><span data-stu-id="6f485-208">This method allows you to execute any commands in a folder's shortcut menu or stored in the registry.</span></span>

<span data-ttu-id="6f485-209">Si *lpOperation* es **null**, la función abre el archivo especificado por *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="6f485-209">If *lpOperation* is **NULL**, the function opens the file specified by *lpFile*.</span></span> <span data-ttu-id="6f485-210">Si *lpOperation* es "Open" o "Explore", la función intenta abrir o explorar la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6f485-210">If *lpOperation* is "open" or "explore", the function attempts to open or explore the folder.</span></span>

<span data-ttu-id="6f485-211">Para obtener información sobre la aplicación que se inicia como resultado de llamar a **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="6f485-211">To obtain information about the application that is launched as a result of calling **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

> [!Note]  
> <span data-ttu-id="6f485-212">Las **ventanas de la carpeta de inicio en una configuración de proceso independiente** en opciones de carpeta afectan a **WOWShellExecute**.</span><span class="sxs-lookup"><span data-stu-id="6f485-212">The **Launch folder windows in a separate process** setting in Folder Options affects **WOWShellExecute**.</span></span> <span data-ttu-id="6f485-213">Si esa opción está deshabilitada (la configuración predeterminada), **WOWShellExecute** usa una ventana de explorador abierta en lugar de iniciar una nueva.</span><span class="sxs-lookup"><span data-stu-id="6f485-213">If that option is disabled (the default setting), **WOWShellExecute** uses an open Explorer window rather than launch a new one.</span></span> <span data-ttu-id="6f485-214">Si no hay ninguna ventana del explorador abierta, **WOWShellExecute** inicia una nueva.</span><span class="sxs-lookup"><span data-stu-id="6f485-214">If no Explorer window is open, **WOWShellExecute** launches a new one.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f485-215">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f485-215">Requirements</span></span>



| <span data-ttu-id="6f485-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f485-216">Requirement</span></span> | <span data-ttu-id="6f485-217">Value</span><span class="sxs-lookup"><span data-stu-id="6f485-217">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f485-218">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f485-218">Minimum supported client</span></span><br/> | <span data-ttu-id="6f485-219">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6f485-219">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6f485-220">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6f485-220">Minimum supported server</span></span><br/> | <span data-ttu-id="6f485-221">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6f485-221">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6f485-222">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6f485-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f485-223"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f485-223"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f485-224">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6f485-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f485-225">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="6f485-225">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
