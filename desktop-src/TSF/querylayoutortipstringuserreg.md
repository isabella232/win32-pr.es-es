---
title: QueryLayoutOrTipStringUserReg función)
description: Consulta la cadena especificada que representa el formato de una lista de distribución de teclado o una lista de perfiles de servicios de texto de la ruta de acceso del registro especificada.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- QueryLayoutOrTipStringUserReg función de servicios de texto
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686135"
---
# <a name="querylayoutortipstringuserreg-function"></a><span data-ttu-id="45eee-104">QueryLayoutOrTipStringUserReg función)</span><span class="sxs-lookup"><span data-stu-id="45eee-104">QueryLayoutOrTipStringUserReg function</span></span>

<span data-ttu-id="45eee-105">Consulta la cadena especificada que representa el formato de una lista de distribución de teclado o una lista de perfiles de servicios de texto de la ruta de acceso del registro especificada.</span><span class="sxs-lookup"><span data-stu-id="45eee-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list of the specified registry path.</span></span>

## <a name="syntax"></a><span data-ttu-id="45eee-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45eee-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="45eee-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45eee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45eee-108">*pszUserReg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45eee-108">*pszUserReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45eee-109">La ruta de acceso del registro del usuario.</span><span class="sxs-lookup"><span data-stu-id="45eee-109">The registry path of the user.</span></span> <span data-ttu-id="45eee-110">Si este parámetro es **null**, \_ \_ se utiliza HKEY current user.</span><span class="sxs-lookup"><span data-stu-id="45eee-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="45eee-111">*pszSystemReg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45eee-111">*pszSystemReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45eee-112">Ruta de acceso del registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="45eee-112">The registry path of the system.</span></span> <span data-ttu-id="45eee-113">Si este parámetro es **null**, \_ \_ se usa HKEY local Machine \\ System.</span><span class="sxs-lookup"><span data-stu-id="45eee-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="45eee-114">*pszSoftwareReg* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45eee-114">*pszSoftwareReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45eee-115">La ruta de acceso del registro del software.</span><span class="sxs-lookup"><span data-stu-id="45eee-115">The registry path of the software.</span></span> <span data-ttu-id="45eee-116">Si este parámetro es **null**, \_ \_ se utiliza el software del equipo local HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="45eee-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="45eee-117">*PSZ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45eee-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45eee-118">Una cadena que representa una lista de distribución de teclado o una lista de perfiles de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="45eee-118">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="45eee-119">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="45eee-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45eee-120">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="45eee-120">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45eee-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45eee-121">Return value</span></span>

<span data-ttu-id="45eee-122">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="45eee-122">This function can return one of these values.</span></span>



| <span data-ttu-id="45eee-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="45eee-123">Return code</span></span>                                                                                  | <span data-ttu-id="45eee-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="45eee-124">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45eee-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="45eee-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="45eee-126">Todos los diseños o perfiles definidos en **PSZ** son válidos.</span><span class="sxs-lookup"><span data-stu-id="45eee-126">All layouts or profiles defined in **psz** are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="45eee-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="45eee-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="45eee-128">Uno o varios de los diseños o perfiles definidos en **PSZ** no son válidos.</span><span class="sxs-lookup"><span data-stu-id="45eee-128">One or more of the layouts or profiles defined in **psz** are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="45eee-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45eee-129">Remarks</span></span>

<span data-ttu-id="45eee-130">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="45eee-130">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="45eee-131">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="45eee-131">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="45eee-132">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="45eee-132">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="45eee-133">El formato de cadena de la lista de diseño es:</span><span class="sxs-lookup"><span data-stu-id="45eee-133">The string format of the layout list is:</span></span>

<span data-ttu-id="45eee-134"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="45eee-134"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="45eee-135">El formato de cadena de la lista de perfiles de servicio de texto es:</span><span class="sxs-lookup"><span data-stu-id="45eee-135">The string format of the text service profile list is:</span></span>

<span data-ttu-id="45eee-136"><LangID 1>: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="45eee-136"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="45eee-137">El siguiente es un ejemplo de un valor para el parámetro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="45eee-137">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="45eee-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45eee-138">Requirements</span></span>



| <span data-ttu-id="45eee-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="45eee-139">Requirement</span></span> | <span data-ttu-id="45eee-140">Value</span><span class="sxs-lookup"><span data-stu-id="45eee-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="45eee-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45eee-141">Minimum supported client</span></span><br/> | <span data-ttu-id="45eee-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="45eee-142">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="45eee-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45eee-143">Minimum supported server</span></span><br/> | <span data-ttu-id="45eee-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="45eee-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="45eee-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45eee-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45eee-146"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45eee-146"><dt>Input.dll</dt></span></span> </dl> |



 

