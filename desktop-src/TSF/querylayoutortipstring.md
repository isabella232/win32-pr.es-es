---
title: QueryLayoutOrTipString función)
description: Consulta la cadena especificada que representa el formato de una lista de distribución de teclado o de la lista de perfiles de servicios de texto.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- QueryLayoutOrTipString función de servicios de texto
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686136"
---
# <a name="querylayoutortipstring-function"></a><span data-ttu-id="08ab6-104">QueryLayoutOrTipString función)</span><span class="sxs-lookup"><span data-stu-id="08ab6-104">QueryLayoutOrTipString function</span></span>

<span data-ttu-id="08ab6-105">Consulta la cadena especificada que representa el formato de una lista de distribución de teclado o de la lista de perfiles de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="08ab6-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list.</span></span>

## <a name="syntax"></a><span data-ttu-id="08ab6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08ab6-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="08ab6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08ab6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ab6-108">*PSZ* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08ab6-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab6-109">Una cadena que representa una lista de distribución de teclado o una lista de perfiles de servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="08ab6-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="08ab6-110">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="08ab6-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08ab6-111">Debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="08ab6-111">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08ab6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08ab6-112">Return value</span></span>

<span data-ttu-id="08ab6-113">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="08ab6-113">This function can return one of these values.</span></span>



| <span data-ttu-id="08ab6-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="08ab6-114">Return code</span></span>                                                                                  | <span data-ttu-id="08ab6-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="08ab6-115">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08ab6-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="08ab6-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="08ab6-117">Todos los diseños o perfiles definidos en *PSZ* son válidos.</span><span class="sxs-lookup"><span data-stu-id="08ab6-117">All layouts or profiles defined in *psz* are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="08ab6-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="08ab6-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="08ab6-119">Uno o varios de los diseños o perfiles definidos en *PSZ* no son válidos.</span><span class="sxs-lookup"><span data-stu-id="08ab6-119">One or more of the layouts or profiles defined in *psz* are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="08ab6-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08ab6-120">Remarks</span></span>

<span data-ttu-id="08ab6-121">No hay ninguna biblioteca de importación disponible que defina esta función, por lo que es necesario obtener un puntero a esta función mediante [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="08ab6-121">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="08ab6-122">El uso incorrecto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) puede poner en peligro la seguridad de la aplicación mediante la carga de una DLL incorrecta.</span><span class="sxs-lookup"><span data-stu-id="08ab6-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="08ab6-123">Consulte el [orden de búsqueda de la biblioteca de vínculos dinámicos](/windows/desktop/Dlls/dynamic-link-library-search-order) para obtener información sobre cómo cargar correctamente los archivos DLL con diferentes versiones de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="08ab6-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="08ab6-124">El formato de cadena de la lista de diseño es:</span><span class="sxs-lookup"><span data-stu-id="08ab6-124">The string format of the layout list is:</span></span>

<span data-ttu-id="08ab6-125"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="08ab6-125"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="08ab6-126">El formato de cadena de la lista de perfiles de servicio de texto es:</span><span class="sxs-lookup"><span data-stu-id="08ab6-126">The string format of the text service profile list is:</span></span>

<span data-ttu-id="08ab6-127"><LangID 1>: {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX} {xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX};</span><span class="sxs-lookup"><span data-stu-id="08ab6-127"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="08ab6-128">El siguiente es un ejemplo de un valor para el parámetro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="08ab6-128">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="08ab6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08ab6-129">Requirements</span></span>



| <span data-ttu-id="08ab6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="08ab6-130">Requirement</span></span> | <span data-ttu-id="08ab6-131">Value</span><span class="sxs-lookup"><span data-stu-id="08ab6-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="08ab6-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08ab6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="08ab6-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="08ab6-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="08ab6-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08ab6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="08ab6-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="08ab6-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="08ab6-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08ab6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08ab6-137"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08ab6-137"><dt>Input.dll</dt></span></span> </dl> |



 

