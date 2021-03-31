---
title: SetDefaultLayoutOrTip función)
description: Establece la distribución de teclado especificada o un servicio de texto como el elemento de entrada predeterminado del usuario actual.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- SetDefaultLayoutOrTip función de servicios de texto
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150050"
---
# <a name="setdefaultlayoutortip-function"></a><span data-ttu-id="70bb5-104">SetDefaultLayoutOrTip función)</span><span class="sxs-lookup"><span data-stu-id="70bb5-104">SetDefaultLayoutOrTip function</span></span>

<span data-ttu-id="70bb5-105">Establece la distribución de teclado especificada o un servicio de texto como el elemento de entrada predeterminado del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="70bb5-105">Sets the specified keyboard layout or a text service as the default input item of the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="70bb5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70bb5-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="70bb5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70bb5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70bb5-108">*PSZ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70bb5-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70bb5-109">Una cadena que representa una lista de distribución de teclado o una lista de perfiles de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="70bb5-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="70bb5-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70bb5-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70bb5-111">Un campo de bits que especifica las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="70bb5-111">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="70bb5-112">Los identificadores siguientes no se definen en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="70bb5-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="70bb5-113">Debe usar el valor hexadecimal o \# definir los identificadores.</span><span class="sxs-lookup"><span data-stu-id="70bb5-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="70bb5-114">Por ejemplo, para usar SDLOT \_ NOAPPLYTOCURRENTSESSION, debe incluir \# la definición \_ de SDLOT NOAPPLYTOCURRENTSESSION 0x00000001 en el código.</span><span class="sxs-lookup"><span data-stu-id="70bb5-114">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="70bb5-115">Value</span><span class="sxs-lookup"><span data-stu-id="70bb5-115">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="70bb5-116">Significado</span><span class="sxs-lookup"><span data-stu-id="70bb5-116">Meaning</span></span>                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="70bb5-117"><dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="70bb5-117"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="70bb5-118">Almacena la configuración en el registro pero no actualiza la configuración de teclado en tiempo de ejecución de la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="70bb5-118">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="70bb5-119">Si la ruta de acceso del registro alternativa está establecida en [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), se debe establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="70bb5-119">If the alternative registry path is set in [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="70bb5-120"><dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="70bb5-120"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="70bb5-121">Aplica la configuración inmediatamente en el subproceso actual.</span><span class="sxs-lookup"><span data-stu-id="70bb5-121">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70bb5-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70bb5-122">Return value</span></span>



| <span data-ttu-id="70bb5-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="70bb5-123">Return code</span></span>                                                                          | <span data-ttu-id="70bb5-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="70bb5-124">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="70bb5-125"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="70bb5-125"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="70bb5-126">La función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="70bb5-126">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="70bb5-127"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="70bb5-127"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="70bb5-128">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="70bb5-128">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="70bb5-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70bb5-129">Remarks</span></span>

<span data-ttu-id="70bb5-130">El formato de cadena de la lista de diseño es:</span><span class="sxs-lookup"><span data-stu-id="70bb5-130">The string format of the layout list is:</span></span>

<span data-ttu-id="70bb5-131"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="70bb5-131"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="70bb5-132">El formato de cadena de la lista de perfiles de servicio de texto es:</span><span class="sxs-lookup"><span data-stu-id="70bb5-132">The string format of the text service profile list is:</span></span>

<span data-ttu-id="70bb5-133"><LangID 1>: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="70bb5-133"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="70bb5-134">El siguiente es un ejemplo de un valor para el parámetro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="70bb5-134">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="70bb5-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="70bb5-135">Examples</span></span>

<span data-ttu-id="70bb5-136">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="70bb5-136">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="70bb5-137">En el ejemplo siguiente se muestra cómo obtener un puntero a esta función.</span><span class="sxs-lookup"><span data-stu-id="70bb5-137">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="70bb5-138">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="70bb5-138">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="70bb5-139">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="70bb5-139">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="70bb5-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70bb5-140">Requirements</span></span>



| <span data-ttu-id="70bb5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="70bb5-141">Requirement</span></span> | <span data-ttu-id="70bb5-142">Value</span><span class="sxs-lookup"><span data-stu-id="70bb5-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="70bb5-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70bb5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="70bb5-144">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70bb5-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="70bb5-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70bb5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="70bb5-146">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="70bb5-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="70bb5-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70bb5-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70bb5-148"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70bb5-148"><dt>Input.dll</dt></span></span> </dl> |



 

