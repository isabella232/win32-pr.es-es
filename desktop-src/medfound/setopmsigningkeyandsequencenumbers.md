---
description: Establece la clave de firma y dos números de secuencia en un objeto de salida protegido.
ms.assetid: 278a80f5-198d-4311-aa43-10b6dc33b3a4
title: SetOPMSigningKeyAndSequenceNumbers función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetOPMSigningKeyAndSequenceNumbers
api_type:
- DllExport
api_location:
- gdi32.dll
ms.openlocfilehash: cbd088b83acd4e93cc186e6c7b5635ad1e3d8346
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275814"
---
# <a name="setopmsigningkeyandsequencenumbers-function"></a><span data-ttu-id="c3414-103">SetOPMSigningKeyAndSequenceNumbers función)</span><span class="sxs-lookup"><span data-stu-id="c3414-103">SetOPMSigningKeyAndSequenceNumbers function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c3414-104">El administrador de protección de [salida](output-protection-manager.md) (OPM) usa esta función para tener acceso a la funcionalidad del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c3414-104">This function is used by [Output Protection Manager](output-protection-manager.md) (OPM) to access functionality in the display driver.</span></span> <span data-ttu-id="c3414-105">Las aplicaciones no deben llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="c3414-105">Applications should not call this function.</span></span>

 

<span data-ttu-id="c3414-106">Establece la clave de firma y dos números de secuencia en un objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="c3414-106">Sets the signing key and two sequence numbers on a protected output object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3414-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c3414-107">Syntax</span></span>


```C++
NTSTATUS WINAPI SetOPMSigningKeyAndSequenceNumbers(
  _In_        OPM_PROTECTED_OUTPUT_HANDLE      opoOPMProtectedOutput,
  _Out_ const DXGKMDT_OPM_ENCRYPTED_PARAMETERS *pParameters
);
```



## <a name="parameters"></a><span data-ttu-id="c3414-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c3414-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3414-109">*opoOPMProtectedOutput* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c3414-109">*opoOPMProtectedOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3414-110">Identificador del objeto de salida protegido.</span><span class="sxs-lookup"><span data-stu-id="c3414-110">A handle to the protected output object.</span></span> <span data-ttu-id="c3414-111">Este identificador se obtiene llamando a [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span><span class="sxs-lookup"><span data-stu-id="c3414-111">This handle is obtained by calling [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3414-112">*pParameters* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c3414-112">*pParameters* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3414-113">Puntero a una estructura [**de \_ \_ \_ parámetros cifrados de OPM de DXGKMDT**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) que contiene una matriz de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="c3414-113">A pointer to a [**DXGKMDT\_OPM\_ENCRYPTED\_PARAMETERS**](/windows-hardware/drivers/ddi/d3dkmdt/ns-d3dkmdt-_dxgkmdt_opm_encrypted_parameters) structure that contains a 256-byte array.</span></span> <span data-ttu-id="c3414-114">Para obtener más información sobre cómo inicializar esta matriz, vea [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span><span class="sxs-lookup"><span data-stu-id="c3414-114">For more information about how to initialize this array, see [DxgkDdiOPMSetSigningKeyAndSequenceNumbers](https://msdn.microsoft.com/library/aa906703.aspx).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3414-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c3414-115">Return value</span></span>

<span data-ttu-id="c3414-116">Si el método se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c3414-116">If the method succeeds, it returns **STATUS\_SUCCESS**.</span></span> <span data-ttu-id="c3414-117">De lo contrario, devuelve un código de error **NTSTATUS** .</span><span class="sxs-lookup"><span data-stu-id="c3414-117">Otherwise, it returns an **NTSTATUS** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3414-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c3414-118">Remarks</span></span>

<span data-ttu-id="c3414-119">Las aplicaciones deben llamar a [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) en lugar de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="c3414-119">Applications should call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) instead of calling this function.</span></span>

<span data-ttu-id="c3414-120">Esta función no tiene ninguna biblioteca de importación asociada.</span><span class="sxs-lookup"><span data-stu-id="c3414-120">This function has no associated import library.</span></span> <span data-ttu-id="c3414-121">Para llamar a esta función, debe utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Gdi32.dll.</span><span class="sxs-lookup"><span data-stu-id="c3414-121">To call this function, you must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Gdi32.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3414-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3414-122">Requirements</span></span>



| <span data-ttu-id="c3414-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3414-123">Requirement</span></span> | <span data-ttu-id="c3414-124">Value</span><span class="sxs-lookup"><span data-stu-id="c3414-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c3414-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3414-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c3414-126">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c3414-126">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c3414-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c3414-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c3414-128">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c3414-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c3414-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c3414-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3414-130"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3414-130"><dt>Gdi32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3414-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="c3414-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3414-132">Funciones de OPM</span><span class="sxs-lookup"><span data-stu-id="c3414-132">OPM Functions</span></span>](opm-functions.md)
</dt> <dt>

[<span data-ttu-id="c3414-133">Administrador de protección de salida</span><span class="sxs-lookup"><span data-stu-id="c3414-133">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 
