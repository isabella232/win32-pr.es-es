---
title: InstallLayoutOrTip función)
description: Habilita las distribuciones de teclado o los servicios de texto especificados.
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- InstallLayoutOrTip función de servicios de texto
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685992"
---
# <a name="installlayoutortip-function"></a><span data-ttu-id="75c3f-104">InstallLayoutOrTip función)</span><span class="sxs-lookup"><span data-stu-id="75c3f-104">InstallLayoutOrTip function</span></span>

<span data-ttu-id="75c3f-105">Habilita las distribuciones de teclado o los servicios de texto especificados.</span><span class="sxs-lookup"><span data-stu-id="75c3f-105">Enables the specified keyboard layouts or text services.</span></span>

## <a name="syntax"></a><span data-ttu-id="75c3f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75c3f-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="75c3f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75c3f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75c3f-108">*PSZ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75c3f-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c3f-109">Cadena que representa la lista de distribución del teclado o la lista de perfiles de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="75c3f-109">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="75c3f-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="75c3f-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75c3f-111">Un campo de bits que especifica las marcas siguientes:</span><span class="sxs-lookup"><span data-stu-id="75c3f-111">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="75c3f-112">Los identificadores siguientes no se definen en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="75c3f-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="75c3f-113">Debe usar el valor hexadecimal o \# definir los identificadores.</span><span class="sxs-lookup"><span data-stu-id="75c3f-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="75c3f-114">Por ejemplo, para usar **la \_ desinstalación de ILOT** , debe incluir `#define ILOT_UNINSTALL 0x00000001` en el código.</span><span class="sxs-lookup"><span data-stu-id="75c3f-114">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="75c3f-115">Value</span><span class="sxs-lookup"><span data-stu-id="75c3f-115">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="75c3f-116">Significado</span><span class="sxs-lookup"><span data-stu-id="75c3f-116">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="75c3f-117"><dt>**ILOT \_ Desinstalar**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-117"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="75c3f-118">Igual que **ILOT \_ deshabilitado**.</span><span class="sxs-lookup"><span data-stu-id="75c3f-118">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="75c3f-119"><dt>**ILOT \_ DEFPROFILE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-119"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="75c3f-120">Establece el diseño o la sugerencia especificados como un elemento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="75c3f-120">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <span data-ttu-id="75c3f-121"><dt>**ILOT \_ DEFUSER4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-121"><dt>**ILOT\_DEFUSER4**</dt> <dt>0x00000004</dt></span></span> </dl>                                              | <span data-ttu-id="75c3f-122">Cambia la configuración de. Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="75c3f-122">Changes the setting of .Default.</span></span><br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <span data-ttu-id="75c3f-123"><dt>**ILOT \_ SYSLOCALE**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-123"><dt>**ILOT\_SYSLOCALE**</dt> <dt>0x00000008</dt></span></span> </dl>                                           | <span data-ttu-id="75c3f-124">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="75c3f-124">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <span data-ttu-id="75c3f-125"><dt>**ILOT \_ NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-125"><dt>**ILOT\_NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="75c3f-126">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="75c3f-126">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="75c3f-127"><dt>**ILOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-127"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="75c3f-128">La configuración se guarda pero no se aplica a la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="75c3f-128">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="75c3f-129"><dt>**ILOT \_ CLEANINSTALL**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-129"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="75c3f-130">Deshabilita todos los servicios de texto y distribuciones de teclado actuales.</span><span class="sxs-lookup"><span data-stu-id="75c3f-130">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="75c3f-131"><dt>**ILOT \_ Deshabilitado**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-131"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="75c3f-132">Deshabilita la distribución del teclado y el servicio de texto especificados.</span><span class="sxs-lookup"><span data-stu-id="75c3f-132">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75c3f-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75c3f-133">Return value</span></span>



| <span data-ttu-id="75c3f-134">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="75c3f-134">Return code</span></span>                                                                          | <span data-ttu-id="75c3f-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="75c3f-135">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="75c3f-136"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-136"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="75c3f-137">La función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="75c3f-137">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="75c3f-138"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-138"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="75c3f-139">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="75c3f-139">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75c3f-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75c3f-140">Remarks</span></span>

<span data-ttu-id="75c3f-141">El formato de cadena de la lista de diseño es:</span><span class="sxs-lookup"><span data-stu-id="75c3f-141">The string format of the layout list is:</span></span>

<span data-ttu-id="75c3f-142"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="75c3f-142"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="75c3f-143">El formato de cadena de la lista de perfiles de servicio de texto es:</span><span class="sxs-lookup"><span data-stu-id="75c3f-143">The string format of the text service profile list is:</span></span>

<span data-ttu-id="75c3f-144"><LangID 1>: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="75c3f-144"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="75c3f-145">El siguiente es un ejemplo de un valor para el parámetro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="75c3f-145">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="75c3f-146">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="75c3f-146">Examples</span></span>

<span data-ttu-id="75c3f-147">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="75c3f-147">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="75c3f-148">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="75c3f-148">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="75c3f-149">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="75c3f-149">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="75c3f-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75c3f-150">Requirements</span></span>



| <span data-ttu-id="75c3f-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="75c3f-151">Requirement</span></span> | <span data-ttu-id="75c3f-152">Value</span><span class="sxs-lookup"><span data-stu-id="75c3f-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="75c3f-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75c3f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="75c3f-154">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="75c3f-154">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="75c3f-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75c3f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="75c3f-156">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="75c3f-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="75c3f-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75c3f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75c3f-158"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75c3f-158"><dt>Input.dll</dt></span></span> </dl> |



 

