---
title: SaveDefaultUserInputSettings función)
description: Aplica la configuración del servicio de texto y la distribución del teclado del usuario al subárbol del usuario predeterminado.
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- SaveDefaultUserInputSettings función de servicios de texto
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422101"
---
# <a name="savedefaultuserinputsettings-function"></a><span data-ttu-id="3e19d-104">SaveDefaultUserInputSettings función)</span><span class="sxs-lookup"><span data-stu-id="3e19d-104">SaveDefaultUserInputSettings function</span></span>

<span data-ttu-id="3e19d-105">Aplica la configuración del servicio de texto y la distribución del teclado del usuario al subárbol del usuario predeterminado.</span><span class="sxs-lookup"><span data-stu-id="3e19d-105">Applies the user keyboard layout and text service setting to the default user hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e19d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e19d-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="3e19d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3e19d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e19d-108">*hwndParent* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e19d-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e19d-109">Ventana primaria para el cuadro de diálogo de advertencia.</span><span class="sxs-lookup"><span data-stu-id="3e19d-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="3e19d-110">El cuadro de diálogo de advertencia no se muestra siempre y se muestra correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e19d-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="3e19d-111">Si este parámetro es NULL, no se mostrará el cuadro de diálogo de advertencia.</span><span class="sxs-lookup"><span data-stu-id="3e19d-111">If this parameter is NULL, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="3e19d-112">*hSourceRegKey* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3e19d-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e19d-113">La clave del Registro raíz de la configuración del usuario que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="3e19d-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e19d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3e19d-114">Return value</span></span>



| <span data-ttu-id="3e19d-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="3e19d-115">Return code</span></span>                                                                          | <span data-ttu-id="3e19d-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e19d-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="3e19d-117"><dt>**REALES**</dt></span><span class="sxs-lookup"><span data-stu-id="3e19d-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="3e19d-118">La función se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3e19d-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="3e19d-119"><dt>**ES**</dt></span><span class="sxs-lookup"><span data-stu-id="3e19d-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="3e19d-120">Se ha producido un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="3e19d-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="3e19d-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3e19d-121">Examples</span></span>

<span data-ttu-id="3e19d-122">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="3e19d-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="3e19d-123">En el ejemplo siguiente se muestra cómo obtener un puntero a esta función.</span><span class="sxs-lookup"><span data-stu-id="3e19d-123">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="3e19d-124">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="3e19d-124">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="3e19d-125">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3e19d-125">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="3e19d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e19d-126">Requirements</span></span>



| <span data-ttu-id="3e19d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e19d-127">Requirement</span></span> | <span data-ttu-id="3e19d-128">Value</span><span class="sxs-lookup"><span data-stu-id="3e19d-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3e19d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e19d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3e19d-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3e19d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3e19d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e19d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3e19d-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e19d-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3e19d-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e19d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e19d-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e19d-134"><dt>Input.dll</dt></span></span> </dl> |



 

