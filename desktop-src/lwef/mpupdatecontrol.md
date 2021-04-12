---
title: Función MpUpdateControl (MpClient. h)
description: Permite el control de una operación de actualización de firmas que se inició de forma asincrónica a través de MpUpdateStart.
ms.assetid: 2780E472-6E8D-4839-88EE-46E3448C6BF5
keywords:
- Función MpUpdateControl características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpUpdateControl
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ea28c6ace349fd04fb9241d7eddbe7c1e5fbbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491548"
---
# <a name="mpupdatecontrol-function"></a><span data-ttu-id="dd4cc-104">MpUpdateControl función)</span><span class="sxs-lookup"><span data-stu-id="dd4cc-104">MpUpdateControl function</span></span>

<span data-ttu-id="dd4cc-105">Permite el control de una operación de actualización de firmas que se inició de forma asincrónica a través de [**MpUpdateStart**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="dd4cc-105">Allows the control of a signature update operation that was asynchronously initiated via [**MpUpdateStart**](mpupdatestart.md).</span></span> <span data-ttu-id="dd4cc-106">La llamada a esta función requiere privilegios de administrador, ya que permite la cancelación de una actualización de firmas en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-106">Calling this function requires administrator privilege as it allows the cancellation of a system-wide signature update.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd4cc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd4cc-107">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateControl(
  _In_ MPHANDLE  hUpdateHandle,
  _In_ MPCONTROL UpdateControl
);
```



## <a name="parameters"></a><span data-ttu-id="dd4cc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dd4cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd4cc-109">*hUpdateHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd4cc-109">*hUpdateHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd4cc-110">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="dd4cc-110">Type: **MPHANDLE**</span></span>

<span data-ttu-id="dd4cc-111">Identificador de una operación de actualización de firma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-111">Handle to an asynchronous signature update operation.</span></span> <span data-ttu-id="dd4cc-112">La función [**MpScanStart**](mpscanstart.md) devuelve este identificador.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-112">This handle is returned by the [**MpScanStart**](mpscanstart.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="dd4cc-113">*UpdateControl* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dd4cc-113">*UpdateControl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd4cc-114">Tipo: **MPCONTROL**</span><span class="sxs-lookup"><span data-stu-id="dd4cc-114">Type: **MPCONTROL**</span></span>

<span data-ttu-id="dd4cc-115">Especifica la opción de control de actualización de firmas.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-115">Specifies the signature update control option.</span></span> <span data-ttu-id="dd4cc-116">Debe ser el siguiente valor:</span><span class="sxs-lookup"><span data-stu-id="dd4cc-116">It must be the following value:</span></span>



| <span data-ttu-id="dd4cc-117">Value</span><span class="sxs-lookup"><span data-stu-id="dd4cc-117">Value</span></span>                                                                                                                                                               | <span data-ttu-id="dd4cc-118">Significado</span><span class="sxs-lookup"><span data-stu-id="dd4cc-118">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="MPCONTROL_ABORT"></span><span id="mpcontrol_abort"></span><dl> <span data-ttu-id="dd4cc-119"><dt>**\_anulación de MPCONTROL**</dt></span><span class="sxs-lookup"><span data-stu-id="dd4cc-119"><dt>**MPCONTROL\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="dd4cc-120">Anular la operación de actualización de firma.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-120">Abort the signature update operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd4cc-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dd4cc-121">Return value</span></span>

<span data-ttu-id="dd4cc-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dd4cc-122">Type: **HRESULT**</span></span>

<span data-ttu-id="dd4cc-123">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-123">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="dd4cc-124">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-124">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="dd4cc-125">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="dd4cc-125">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd4cc-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd4cc-126">Requirements</span></span>



| <span data-ttu-id="dd4cc-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd4cc-127">Requirement</span></span> | <span data-ttu-id="dd4cc-128">Value</span><span class="sxs-lookup"><span data-stu-id="dd4cc-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4cc-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd4cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd4cc-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd4cc-130">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="dd4cc-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd4cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd4cc-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd4cc-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd4cc-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dd4cc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd4cc-134"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd4cc-134"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd4cc-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd4cc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd4cc-136"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd4cc-136"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd4cc-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd4cc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4cc-138">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="dd4cc-138">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="dd4cc-139">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="dd4cc-139">**MpScanStart**</span></span>](mpscanstart.md)
</dt> </dl>

 

 





