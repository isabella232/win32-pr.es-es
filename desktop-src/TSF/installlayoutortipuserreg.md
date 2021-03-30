---
title: InstallLayoutOrTipUserReg función)
description: Habilita las distribuciones de teclado o los servicios de texto especificados para el usuario especificado.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- InstallLayoutOrTipUserReg función de servicios de texto
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802371"
---
# <a name="installlayoutortipuserreg-function"></a><span data-ttu-id="bd8f1-104">InstallLayoutOrTipUserReg función)</span><span class="sxs-lookup"><span data-stu-id="bd8f1-104">InstallLayoutOrTipUserReg function</span></span>

<span data-ttu-id="bd8f1-105">Habilita las distribuciones de teclado o los servicios de texto especificados para el usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-105">Enables the specified keyboard layouts or text services for the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd8f1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd8f1-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="bd8f1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd8f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd8f1-108">*pszUserReg* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bd8f1-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8f1-109">La ruta de acceso del registro del usuario.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-109">The registry path of the user.</span></span> <span data-ttu-id="bd8f1-110">Si este parámetro es **null**, \_ \_ se utiliza HKEY current user.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="bd8f1-111">*pszSystemReg* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bd8f1-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8f1-112">Ruta de acceso del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-112">The registry path of the system.</span></span> <span data-ttu-id="bd8f1-113">Si este parámetro es **null**, \_ \_ se usa HKEY local Machine \\ System.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="bd8f1-114">*pszSoftwareReg* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bd8f1-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8f1-115">La ruta de acceso del registro del software.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-115">The registry path of the software.</span></span> <span data-ttu-id="bd8f1-116">Si este parámetro es **null**, \_ \_ se utiliza el software del equipo local HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="bd8f1-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="bd8f1-117">*PSZ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd8f1-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8f1-118">Cadena que representa la lista de distribución del teclado o la lista de perfiles de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="bd8f1-119">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bd8f1-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd8f1-120">Un campo de bits que especifica las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-120">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="bd8f1-121">Los identificadores siguientes no se definen en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="bd8f1-122">Debe usar el valor hexadecimal o \# definir los identificadores.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="bd8f1-123">Por ejemplo, para usar **la \_ desinstalación de ILOT** , debe incluir `#define ILOT_UNINSTALL 0x00000001` en el código.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-123">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="bd8f1-124">Value</span><span class="sxs-lookup"><span data-stu-id="bd8f1-124">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="bd8f1-125">Significado</span><span class="sxs-lookup"><span data-stu-id="bd8f1-125">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="bd8f1-126"><dt>**ILOT \_ Desinstalar**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f1-126"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="bd8f1-127">Igual que **ILOT \_ deshabilitado**.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-127">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="bd8f1-128"><dt>**ILOT \_ DEFPROFILE**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f1-128"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="bd8f1-129">Establece el diseño o la sugerencia especificados como un elemento predeterminado.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-129">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="bd8f1-130"><dt>**ILOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f1-130"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="bd8f1-131">La configuración se guarda pero no se aplica a la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-131">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="bd8f1-132"><dt>**ILOT \_ CLEANINSTALL**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f1-132"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="bd8f1-133">Deshabilita todos los servicios de texto y distribuciones de teclado actuales.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-133">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="bd8f1-134"><dt>**ILOT \_ Deshabilitado**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f1-134"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="bd8f1-135">Deshabilita la distribución del teclado y el servicio de texto especificados.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-135">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd8f1-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd8f1-136">Return value</span></span>



| <span data-ttu-id="bd8f1-137">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bd8f1-137">Return code</span></span>                                                                         | <span data-ttu-id="bd8f1-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd8f1-138">Description</span></span>                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="bd8f1-139"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f1-139"><dt>**TRUE**</dt></span></span> </dl> | <span data-ttu-id="bd8f1-140">La función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-140">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="bd8f1-141"><dt>**FASES**</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f1-141"><dt>**FASE**</dt></span></span> </dl> | <span data-ttu-id="bd8f1-142">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-142">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bd8f1-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd8f1-143">Remarks</span></span>

<span data-ttu-id="bd8f1-144">El formato de cadena de la lista de diseño es:</span><span class="sxs-lookup"><span data-stu-id="bd8f1-144">The string format of the layout list is:</span></span>

<span data-ttu-id="bd8f1-145"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="bd8f1-145"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="bd8f1-146">El formato de cadena de la lista de perfiles de servicio de texto es:</span><span class="sxs-lookup"><span data-stu-id="bd8f1-146">The string format of the text service profile list is:</span></span>

<span data-ttu-id="bd8f1-147"><LangID 1>: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="bd8f1-147"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="bd8f1-148">El siguiente es un ejemplo de un valor para el parámetro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="bd8f1-148">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="bd8f1-149">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bd8f1-149">Examples</span></span>

<span data-ttu-id="bd8f1-150">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="bd8f1-150">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="bd8f1-151">En el ejemplo siguiente se muestra cómo obtener un puntero a esta función.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-151">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="bd8f1-152">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-152">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="bd8f1-153">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="bd8f1-153">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="bd8f1-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd8f1-154">Requirements</span></span>



| <span data-ttu-id="bd8f1-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd8f1-155">Requirement</span></span> | <span data-ttu-id="bd8f1-156">Value</span><span class="sxs-lookup"><span data-stu-id="bd8f1-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bd8f1-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd8f1-157">Minimum supported client</span></span><br/> | <span data-ttu-id="bd8f1-158">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="bd8f1-158">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bd8f1-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd8f1-159">Minimum supported server</span></span><br/> | <span data-ttu-id="bd8f1-160">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd8f1-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bd8f1-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd8f1-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd8f1-162"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd8f1-162"><dt>Input.dll</dt></span></span> </dl> |



 

