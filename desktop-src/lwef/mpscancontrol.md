---
title: Función MpScanControl (MpClient. h)
description: Permite el control de un examen que se inició de forma asincrónica a través de MpScanStart.
ms.assetid: 00855686-8C46-4B58-829C-AEAB53888704
keywords:
- Función MpScanControl características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpScanControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce74736c4ca8c589e2ffa5570f2b6666838d820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490390"
---
# <a name="mpscancontrol-function"></a><span data-ttu-id="ab399-104">MpScanControl función)</span><span class="sxs-lookup"><span data-stu-id="ab399-104">MpScanControl function</span></span>

<span data-ttu-id="ab399-105">Permite el control de un examen que se inició de forma asincrónica a través de [**MpScanStart**](mpscanstart.md).</span><span class="sxs-lookup"><span data-stu-id="ab399-105">Allows the control of a scan that was asynchronously initiated via [**MpScanStart**](mpscanstart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab399-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab399-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanControl(
  _In_ MPHANDLE  hScanHandle,
  _In_ MPCONTROL ScanControl
);
```



## <a name="parameters"></a><span data-ttu-id="ab399-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab399-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab399-108">*hScanHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab399-108">*hScanHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab399-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="ab399-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="ab399-110">Identificador de una operación de examen asincrónico.</span><span class="sxs-lookup"><span data-stu-id="ab399-110">Handle to an asynchronous scan operation.</span></span> <span data-ttu-id="ab399-111">La función [**MpScanStart**](mpscanstart.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="ab399-111">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span> <span data-ttu-id="ab399-112">Este parámetro también se puede establecer en el identificador de la interfaz del administrador de protección contra malware devuelto por la función [**MpManagerOpen**](mpmanageropen.md) para controlar un examen iniciado por el sistema, en cuyo caso el llamador debe tener privilegios administrativos.</span><span class="sxs-lookup"><span data-stu-id="ab399-112">This parameter can also be set to the malware protection manager interface handle returned by [**MpManagerOpen**](mpmanageropen.md) function to control a system initiated scan, in which case the caller must have administrative privilege.</span></span>

</dd> <dt>

<span data-ttu-id="ab399-113">*ScanControl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab399-113">*ScanControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab399-114">Tipo: **MPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="ab399-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="ab399-115">Especifica una opción de control de exploración.</span><span class="sxs-lookup"><span data-stu-id="ab399-115">Specifies a scan control option.</span></span> <span data-ttu-id="ab399-116">Este parámetro debe ser una de las siguientes opciones de control:</span><span class="sxs-lookup"><span data-stu-id="ab399-116">This parameter must be one of the following control options:</span></span>



| <span data-ttu-id="ab399-117">Value</span><span class="sxs-lookup"><span data-stu-id="ab399-117">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="ab399-118">Significado</span><span class="sxs-lookup"><span data-stu-id="ab399-118">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="ab399-119"><dt>**\_anulación de MPCONTROL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab399-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl>    | <span data-ttu-id="ab399-120">Anular la operación de examen.</span><span class="sxs-lookup"><span data-stu-id="ab399-120">Abort the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_PAUSE"></span><span id="mpcontrol_pause"></span><dl> <span data-ttu-id="ab399-121"><dt>**pausar MPCONTROL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ab399-121"><dt>**MPCONTROL\_PAUSE**</dt></span></span> </dl>    | <span data-ttu-id="ab399-122">Pausar la operación de examen.</span><span class="sxs-lookup"><span data-stu-id="ab399-122">Pause the scan operation.</span></span><br/>         |
| <span id="MPCONTROL_RESUME"></span><span id="mpcontrol_resume"></span><dl> <span data-ttu-id="ab399-123"><dt>**\_reanudación de MPCONTROL**</dt></span><span class="sxs-lookup"><span data-stu-id="ab399-123"><dt>**MPCONTROL\_RESUME**</dt></span></span> </dl> | <span data-ttu-id="ab399-124">Reanude la operación de examen en pausa.</span><span class="sxs-lookup"><span data-stu-id="ab399-124">Resume the paused scan operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab399-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab399-125">Return value</span></span>

<span data-ttu-id="ab399-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ab399-126">Type: **HRESULT**</span></span>

<span data-ttu-id="ab399-127">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ab399-127">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="ab399-128">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="ab399-128">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="ab399-129">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="ab399-129">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab399-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab399-130">Requirements</span></span>



| <span data-ttu-id="ab399-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab399-131">Requirement</span></span> | <span data-ttu-id="ab399-132">Value</span><span class="sxs-lookup"><span data-stu-id="ab399-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab399-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab399-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ab399-134">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab399-134">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="ab399-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab399-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ab399-136">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab399-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab399-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab399-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab399-138"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab399-138"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab399-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab399-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab399-140"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab399-140"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab399-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab399-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab399-142">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="ab399-142">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="ab399-143">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="ab399-143">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="ab399-144">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="ab399-144">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





