---
title: SetDefaultLayoutOrTipUserReg función)
description: Establece la distribución de teclado especificada o un servicio de texto como un elemento de entrada predeterminado del registro de usuario.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- SetDefaultLayoutOrTipUserReg función de servicios de texto
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149962"
---
# <a name="setdefaultlayoutortipuserreg-function"></a><span data-ttu-id="32532-104">SetDefaultLayoutOrTipUserReg función)</span><span class="sxs-lookup"><span data-stu-id="32532-104">SetDefaultLayoutOrTipUserReg function</span></span>

<span data-ttu-id="32532-105">Establece la distribución de teclado especificada o un servicio de texto como un elemento de entrada predeterminado del registro de usuario.</span><span class="sxs-lookup"><span data-stu-id="32532-105">Sets the specified keyboard layout or a text service as a default input item of the user registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="32532-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32532-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="32532-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="32532-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32532-108">*pszUserReg* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="32532-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="32532-109">La ruta de acceso del registro del usuario.</span><span class="sxs-lookup"><span data-stu-id="32532-109">The registry path of the user.</span></span> <span data-ttu-id="32532-110">Si este parámetro es **null**, \_ \_ se utiliza HKEY current user.</span><span class="sxs-lookup"><span data-stu-id="32532-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="32532-111">*pszSystemReg* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="32532-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="32532-112">Ruta de acceso del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="32532-112">The registry path of the system.</span></span> <span data-ttu-id="32532-113">Si este parámetro es **null**, \_ \_ se usa HKEY local Machine \\ System.</span><span class="sxs-lookup"><span data-stu-id="32532-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="32532-114">*pszSoftwareReg* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="32532-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="32532-115">La ruta de acceso del registro del software.</span><span class="sxs-lookup"><span data-stu-id="32532-115">The registry path of the software.</span></span> <span data-ttu-id="32532-116">Si este parámetro es **null**, \_ \_ se utiliza el software del equipo local HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="32532-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="32532-117">*PSZ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32532-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32532-118">Cadena que representa la lista de distribución del teclado o la lista de perfiles de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="32532-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="32532-119">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="32532-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32532-120">Un campo de bits que especifica las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="32532-120">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="32532-121">Los identificadores siguientes no se definen en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="32532-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="32532-122">Debe usar el valor hexadecimal o \# definir los identificadores.</span><span class="sxs-lookup"><span data-stu-id="32532-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="32532-123">Por ejemplo, para usar SDLOT \_ NOAPPLYTOCURRENTSESSION, debe incluir \# la definición \_ de SDLOT NOAPPLYTOCURRENTSESSION 0x00000001 en el código.</span><span class="sxs-lookup"><span data-stu-id="32532-123">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="32532-124">Value</span><span class="sxs-lookup"><span data-stu-id="32532-124">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="32532-125">Significado</span><span class="sxs-lookup"><span data-stu-id="32532-125">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="32532-126"><dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="32532-126"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="32532-127">Almacena la configuración en el registro pero no actualiza la configuración de teclado en tiempo de ejecución de la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="32532-127">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="32532-128">Si la ruta de acceso del registro alternativa está establecida en **SetDefaultLayoutOrTipUserReg**, se debe establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="32532-128">If the alternative registry path is set in **SetDefaultLayoutOrTipUserReg**, this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="32532-129"><dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="32532-129"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="32532-130">Aplica la configuración inmediatamente en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="32532-130">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32532-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="32532-131">Return value</span></span>



| <span data-ttu-id="32532-132">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="32532-132">Return code</span></span>                                                                          | <span data-ttu-id="32532-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="32532-133">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="32532-134"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="32532-134"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="32532-135">La función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="32532-135">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="32532-136"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="32532-136"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="32532-137">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="32532-137">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="32532-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32532-138">Remarks</span></span>

<span data-ttu-id="32532-139">El formato de cadena de la lista de diseño es:</span><span class="sxs-lookup"><span data-stu-id="32532-139">The string format of the layout list is:</span></span>

<span data-ttu-id="32532-140"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="32532-140"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="32532-141">El formato de cadena de la lista de perfiles de servicio de texto es:</span><span class="sxs-lookup"><span data-stu-id="32532-141">The string format of the text service profile list is:</span></span>

<span data-ttu-id="32532-142"><LangID 1>: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="32532-142"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="32532-143">El siguiente es un ejemplo de un valor para el parámetro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="32532-143">The following is an example of a value for the *psz* parameter:</span></span>


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="32532-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="32532-144">Examples</span></span>

<span data-ttu-id="32532-145">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="32532-145">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="32532-146">En el ejemplo siguiente se muestra cómo obtener un puntero a esta función.</span><span class="sxs-lookup"><span data-stu-id="32532-146">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="32532-147">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="32532-147">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="32532-148">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="32532-148">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="32532-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32532-149">Requirements</span></span>



| <span data-ttu-id="32532-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="32532-150">Requirement</span></span> | <span data-ttu-id="32532-151">Value</span><span class="sxs-lookup"><span data-stu-id="32532-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="32532-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32532-152">Minimum supported client</span></span><br/> | <span data-ttu-id="32532-153">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="32532-153">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="32532-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32532-154">Minimum supported server</span></span><br/> | <span data-ttu-id="32532-155">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="32532-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="32532-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32532-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32532-157"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32532-157"><dt>Input.dll</dt></span></span> </dl> |



 

