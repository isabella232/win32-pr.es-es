---
description: El método ReOrderCapabilities establece un nuevo orden para las capacidades de formato.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'ITFormatControl:: ReOrderCapabilities (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680465"
---
# <a name="itformatcontrolreordercapabilities-method"></a><span data-ttu-id="29732-103">ITFormatControl:: ReOrderCapabilities (método)</span><span class="sxs-lookup"><span data-stu-id="29732-103">ITFormatControl::ReOrderCapabilities method</span></span>

<span data-ttu-id="29732-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="29732-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="29732-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="29732-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="29732-106">El método **ReOrderCapabilities** establece un nuevo orden para las capacidades de formato.</span><span class="sxs-lookup"><span data-stu-id="29732-106">The **ReOrderCapabilities** method sets a new order for format capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="29732-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29732-107">Syntax</span></span>


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="29732-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29732-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29732-109">*pdwIndices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29732-109">*pdwIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29732-110">Índice del formato que se va a reordenar.</span><span class="sxs-lookup"><span data-stu-id="29732-110">Index of the format being reordered.</span></span>

</dd> <dt>

<span data-ttu-id="29732-111">*pfEnabled* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29732-111">*pfEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29732-112">Indica si el formato debe estar habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="29732-112">Indicates whether the format should be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="29732-113">*pfPublicize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29732-113">*pfPublicize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29732-114">Indica si el formato debe estar disponible.</span><span class="sxs-lookup"><span data-stu-id="29732-114">Indicates whether the format should be made available.</span></span>

</dd> <dt>

<span data-ttu-id="29732-115">*dwNumIndices* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="29732-115">*dwNumIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29732-116">Nuevo número de índice para el formato.</span><span class="sxs-lookup"><span data-stu-id="29732-116">New index number for the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29732-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29732-117">Return value</span></span>

<span data-ttu-id="29732-118">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="29732-118">This method can return one of these values.</span></span>



| <span data-ttu-id="29732-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="29732-119">Return code</span></span>                                                                                   | <span data-ttu-id="29732-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="29732-120">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="29732-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="29732-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="29732-122">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="29732-122">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="29732-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="29732-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="29732-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="29732-124">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="29732-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29732-125">Remarks</span></span>

<span data-ttu-id="29732-126">Se debe llamar al método [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) antes de usar este método.</span><span class="sxs-lookup"><span data-stu-id="29732-126">The [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) method must be called prior to using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="29732-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29732-127">Requirements</span></span>



| <span data-ttu-id="29732-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="29732-128">Requirement</span></span> | <span data-ttu-id="29732-129">Value</span><span class="sxs-lookup"><span data-stu-id="29732-129">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="29732-130">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="29732-130">TAPI version</span></span><br/> | <span data-ttu-id="29732-131">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="29732-131">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="29732-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29732-132">Header</span></span><br/>       | <dl> <span data-ttu-id="29732-133"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="29732-133"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="29732-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29732-134">Library</span></span><br/>      | <dl> <span data-ttu-id="29732-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29732-135"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="29732-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="29732-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="29732-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29732-137"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29732-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="29732-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29732-139">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="29732-139">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="29732-140">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="29732-140">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




