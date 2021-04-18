---
description: Crea una instancia del motor de captura.
ms.assetid: 4B0C9DD6-135D-4412-A585-7E98A84101B5
title: MFCreateCaptureEngine función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateCaptureEngine
api_type:
- DllExport
api_location:
- MFCaptureEngine.dll
ms.openlocfilehash: a2ff0dbf46ca464c11570c8fe78e0b3dbebe3248
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715372"
---
# <a name="mfcreatecaptureengine-function"></a><span data-ttu-id="de20d-103">MFCreateCaptureEngine función)</span><span class="sxs-lookup"><span data-stu-id="de20d-103">MFCreateCaptureEngine function</span></span>

<span data-ttu-id="de20d-104">\[MFCreateCaptureEngine no se admite y puede modificarse o no estar disponible en el futuro.</span><span class="sxs-lookup"><span data-stu-id="de20d-104">\[MFCreateCaptureEngine is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="de20d-105">\]</span><span class="sxs-lookup"><span data-stu-id="de20d-105">\]</span></span>

<span data-ttu-id="de20d-106">Crea una instancia del motor de captura.</span><span class="sxs-lookup"><span data-stu-id="de20d-106">Creates an instance of the capture engine.</span></span>

## <a name="syntax"></a><span data-ttu-id="de20d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de20d-107">Syntax</span></span>


```C++
HRESULT MFCreateCaptureEngine(
  _Out_ IMFCaptureEngine **ppCaptureEngine
);
```



## <a name="parameters"></a><span data-ttu-id="de20d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de20d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de20d-109">*ppCaptureEngine* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="de20d-109">*ppCaptureEngine* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de20d-110">Recibe un puntero a la interfaz [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) .</span><span class="sxs-lookup"><span data-stu-id="de20d-110">Receives a pointer to the [**IMFCaptureEngine**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine) interface.</span></span> <span data-ttu-id="de20d-111">El llamador debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="de20d-111">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de20d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de20d-112">Return value</span></span>

<span data-ttu-id="de20d-113">Si la función se ejecuta correctamente, devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="de20d-113">If the function succeeds, it returns S\_OK.</span></span> <span data-ttu-id="de20d-114">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de20d-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="de20d-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de20d-115">Remarks</span></span>

<span data-ttu-id="de20d-116">Esta función no tiene asociada ninguna biblioteca de importación y no está declarada en un archivo de encabezado público.</span><span class="sxs-lookup"><span data-stu-id="de20d-116">This function has no associated import library and is not declared in a public header file.</span></span> <span data-ttu-id="de20d-117">Debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a MFCaptureEngine.dll.</span><span class="sxs-lookup"><span data-stu-id="de20d-117">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to MFCaptureEngine.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="de20d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de20d-118">Requirements</span></span>



| <span data-ttu-id="de20d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="de20d-119">Requirement</span></span> | <span data-ttu-id="de20d-120">Value</span><span class="sxs-lookup"><span data-stu-id="de20d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de20d-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de20d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="de20d-122">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="de20d-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="de20d-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="de20d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="de20d-124">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="de20d-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de20d-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="de20d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de20d-126"><dt>MFCaptureEngine.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de20d-126"><dt>MFCaptureEngine.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de20d-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="de20d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de20d-128">Funciones de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="de20d-128">Media Foundation Functions</span></span>](media-foundation-functions.md)
</dt> </dl>

 

 
