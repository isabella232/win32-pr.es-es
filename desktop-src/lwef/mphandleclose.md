---
title: Función MpHandleClose (MpClient. h)
description: Cierra el identificador devuelto por MpManagerOpen, MpScanStart, MpThreatOpen o MpUpdateStart.
ms.assetid: 335776E2-7598-4DC1-92AB-B49B35222EF6
keywords:
- Función MpHandleClose características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpHandleClose
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43c937548c8e1d3b98aa2e3d10d7577f8c69c1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535140"
---
# <a name="mphandleclose-function"></a><span data-ttu-id="3d87c-104">MpHandleClose función)</span><span class="sxs-lookup"><span data-stu-id="3d87c-104">MpHandleClose function</span></span>

<span data-ttu-id="3d87c-105">Cierra el identificador devuelto por [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md)o [**MpUpdateStart**](mpupdatestart.md).</span><span class="sxs-lookup"><span data-stu-id="3d87c-105">Closes the handle returned by [**MpManagerOpen**](mpmanageropen.md), [**MpScanStart**](mpscanstart.md), [**MpThreatOpen**](mpthreatopen.md), or [**MpUpdateStart**](mpupdatestart.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3d87c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d87c-106">Syntax</span></span>


```C++
HRESULT WINAPI MpHandleClose(
  _In_ MPHANDLE hMpHandle
);
```



## <a name="parameters"></a><span data-ttu-id="3d87c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d87c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d87c-108">*hMpHandle* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3d87c-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d87c-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="3d87c-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="3d87c-110">Identificador que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="3d87c-110">Handle to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d87c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d87c-111">Return value</span></span>

<span data-ttu-id="3d87c-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3d87c-112">Type: **HRESULT**</span></span>

<span data-ttu-id="3d87c-113">Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3d87c-113">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="3d87c-114">Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo.</span><span class="sxs-lookup"><span data-stu-id="3d87c-114">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="3d87c-115">El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="3d87c-115">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

<span data-ttu-id="3d87c-116">La función puede devolver el siguiente error específico:</span><span class="sxs-lookup"><span data-stu-id="3d87c-116">The following specific error can be returned by the function:</span></span>

| <span data-ttu-id="3d87c-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3d87c-117">Return Code</span></span>             | <span data-ttu-id="3d87c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="3d87c-118">Description</span></span>                      |
|-------------------------|----------------------------------|
| <span data-ttu-id="3d87c-119">E \_ Win \_ identificador no válido \_</span><span class="sxs-lookup"><span data-stu-id="3d87c-119">E\_WIN\_INVALID\_HANDLE</span></span> | <span data-ttu-id="3d87c-120">El identificador especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="3d87c-120">The specified handle is invalid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3d87c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d87c-121">Requirements</span></span>



| <span data-ttu-id="3d87c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d87c-122">Requirement</span></span> | <span data-ttu-id="3d87c-123">Value</span><span class="sxs-lookup"><span data-stu-id="3d87c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d87c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d87c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3d87c-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d87c-125">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3d87c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d87c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3d87c-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d87c-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3d87c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3d87c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d87c-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d87c-129"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d87c-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d87c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d87c-131"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d87c-131"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d87c-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d87c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d87c-133">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="3d87c-133">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="3d87c-134">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="3d87c-134">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="3d87c-135">**MpScanStart**</span><span class="sxs-lookup"><span data-stu-id="3d87c-135">**MpScanStart**</span></span>](mpscanstart.md)
</dt> <dt>

[<span data-ttu-id="3d87c-136">**MpThreatOpen**</span><span class="sxs-lookup"><span data-stu-id="3d87c-136">**MpThreatOpen**</span></span>](mpthreatopen.md)
</dt> </dl>

 

 





