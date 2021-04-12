---
description: Configura un objeto de salida protegido.
ms.assetid: d22a378e-2d4e-4ff4-a18e-136932c24d2b
title: ConfigureOPMProtectedOutput función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureOPMProtectedOutput
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: d72f3d8bbb7d3063fe6982c6d1de99b2f721f005
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423567"
---
# <a name="configureopmprotectedoutput-function"></a><span data-ttu-id="e0d91-103">ConfigureOPMProtectedOutput función)</span><span class="sxs-lookup"><span data-stu-id="e0d91-103">ConfigureOPMProtectedOutput function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0d91-104">El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e0d91-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="e0d91-105">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="e0d91-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="e0d91-106">Configura un objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="e0d91-106">Configures a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0d91-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0d91-107">Syntax</span></span>


```C++
NTSTATUS WINAPI ConfigureOPMProtectedOutput(
  _In_       OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _In_ const DXGKMDT_OPM_CONFIGURE_PARAMETERS *pParameters,
  _In_       ULONG                            ulAdditionalParametersSize,
  _In_ const BYTE                             *pbAdditionalParameters
);
```



## <a name="parameters"></a><span data-ttu-id="e0d91-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0d91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0d91-109">*opoOPMProtectedOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0d91-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d91-110">Identificador del objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="e0d91-110">A handle to the protected output object.</span></span> <span data-ttu-id="e0d91-111">Este identificador se obtiene llamando a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="e0d91-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0d91-112">*pParameters* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0d91-112">*pParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d91-113">Un puntero a una estructura de **\_ \_ \_ parámetros** de configuración de DXGKMDT OPM que contiene el comando de configuración.</span><span class="sxs-lookup"><span data-stu-id="e0d91-113">A pointer to a **DXGKMDT\_OPM\_CONFIGURE\_PARAMETERS** structure that contains the configuration command.</span></span>

</dd> <dt>

<span data-ttu-id="e0d91-114">*ulAdditionalParametersSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0d91-114">*ulAdditionalParametersSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d91-115">Tamaño del búfer de *pbAdditionalParameters* , en bytes.</span><span class="sxs-lookup"><span data-stu-id="e0d91-115">The size of the *pbAdditionalParameters* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e0d91-116">*pbAdditionalParameters* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0d91-116">*pbAdditionalParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0d91-117">Un puntero a un búfer que contiene información adicional para el comando.</span><span class="sxs-lookup"><span data-stu-id="e0d91-117">A pointer to a buffer that contains additional information for the command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0d91-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0d91-118">Return value</span></span>

<span data-ttu-id="e0d91-119">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="e0d91-119">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="e0d91-120">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="e0d91-120">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d91-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0d91-121">Remarks</span></span>

<span data-ttu-id="e0d91-122">Las aplicaciones deben llamar a [**IOPMVideoOutput:: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="e0d91-122">Applications should call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) instead of calling this function.</span></span>

<span data-ttu-id="e0d91-123">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="e0d91-123">This function has no associated import library.</span></span> <span data-ttu-id="e0d91-124">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="e0d91-124">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d91-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0d91-125">Requirements</span></span>



| <span data-ttu-id="e0d91-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0d91-126">Requirement</span></span> | <span data-ttu-id="e0d91-127">Value</span><span class="sxs-lookup"><span data-stu-id="e0d91-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d91-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0d91-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d91-129">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="e0d91-129">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e0d91-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0d91-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d91-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="e0d91-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e0d91-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0d91-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0d91-133"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0d91-133"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0d91-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0d91-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d91-135">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="e0d91-135">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="e0d91-136">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="e0d91-136">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
