---
title: SaveSystemAcctInputSettings función)
description: Aplica la configuración del servicio de texto y la distribución del teclado del usuario al subárbol cuentas del sistema.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- SaveSystemAcctInputSettings función de servicios de texto
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421969"
---
# <a name="savesystemacctinputsettings-function"></a><span data-ttu-id="e8fcc-104">SaveSystemAcctInputSettings función)</span><span class="sxs-lookup"><span data-stu-id="e8fcc-104">SaveSystemAcctInputSettings function</span></span>

<span data-ttu-id="e8fcc-105">Aplica la configuración del servicio de texto y la distribución del teclado del usuario al subárbol cuentas del sistema.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-105">Applies the user keyboard layout and text service setting to the system accounts hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8fcc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8fcc-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="e8fcc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8fcc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8fcc-108">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8fcc-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8fcc-109">Ventana primaria para el cuadro de diálogo de advertencia.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="e8fcc-110">El cuadro de diálogo de advertencia no se muestra siempre y se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="e8fcc-111">Si este parámetro es **null**, no se mostrará el cuadro de diálogo de advertencia.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-111">If this parameter is **NULL**, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="e8fcc-112">*hSourceRegKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e8fcc-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8fcc-113">La clave del Registro raíz de la configuración del usuario que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8fcc-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8fcc-114">Return value</span></span>



| <span data-ttu-id="e8fcc-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e8fcc-115">Return code</span></span>                                                                          | <span data-ttu-id="e8fcc-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8fcc-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e8fcc-117"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="e8fcc-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="e8fcc-118">La función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="e8fcc-119"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="e8fcc-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="e8fcc-120">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e8fcc-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8fcc-121">Remarks</span></span>

<span data-ttu-id="e8fcc-122">El subárbol de la cuenta del sistema es HKEY \_ users \\ . DEFAULT, HKEY \_ users \\ s-1-5-19 y HKEY \_ users \\ s-1-5-20.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-122">The system account hive is HKEY\_USERS\\.DEFAULT, HKEY\_USERS\\S-1-5-19, and HKEY\_USERS\\S-1-5-20.</span></span>

## <a name="examples"></a><span data-ttu-id="e8fcc-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e8fcc-123">Examples</span></span>

<span data-ttu-id="e8fcc-124">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="e8fcc-124">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="e8fcc-125">En el ejemplo siguiente se muestra cómo obtener un puntero a esta función.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-125">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="e8fcc-126">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-126">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="e8fcc-127">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e8fcc-127">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="e8fcc-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8fcc-128">Requirements</span></span>



| <span data-ttu-id="e8fcc-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8fcc-129">Requirement</span></span> | <span data-ttu-id="e8fcc-130">Value</span><span class="sxs-lookup"><span data-stu-id="e8fcc-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8fcc-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8fcc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e8fcc-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e8fcc-132">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e8fcc-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8fcc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e8fcc-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8fcc-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e8fcc-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8fcc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8fcc-136"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8fcc-136"><dt>Input.dll</dt></span></span> </dl> |



 

