---
description: El método SetQOSApplicationID establece el identificador de QOS de la aplicación.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'ITQOSApplicationID:: SetQOSApplicationID (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681239"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a><span data-ttu-id="b747a-103">ITQOSApplicationID:: SetQOSApplicationID (método)</span><span class="sxs-lookup"><span data-stu-id="b747a-103">ITQOSApplicationID::SetQOSApplicationID method</span></span>

<span data-ttu-id="b747a-104">\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b747a-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b747a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="b747a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b747a-106">El método **SetQOSApplicationID** establece el identificador de QoS de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b747a-106">The **SetQOSApplicationID** method sets the QOS identifier for the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="b747a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b747a-107">Syntax</span></span>


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a><span data-ttu-id="b747a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b747a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b747a-109">*pApplicationID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b747a-109">*pApplicationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b747a-110">Identificador único para el proceso de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b747a-110">Unique identifier for the application process.</span></span>

</dd> <dt>

<span data-ttu-id="b747a-111">*pApplicationGUID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b747a-111">*pApplicationGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b747a-112">GUID de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b747a-112">Application GUID.</span></span>

</dd> <dt>

<span data-ttu-id="b747a-113">*pSubIDs* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b747a-113">*pSubIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b747a-114">Sub-IDs asociado a la llamada actual.</span><span class="sxs-lookup"><span data-stu-id="b747a-114">Sub-IDs associated with the current call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b747a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b747a-115">Return value</span></span>

<span data-ttu-id="b747a-116">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="b747a-116">This method can return one of these values.</span></span>



| <span data-ttu-id="b747a-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b747a-117">Return code</span></span>                                                                                   | <span data-ttu-id="b747a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b747a-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b747a-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b747a-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b747a-120">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b747a-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b747a-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b747a-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b747a-122">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b747a-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b747a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b747a-123">Requirements</span></span>



| <span data-ttu-id="b747a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b747a-124">Requirement</span></span> | <span data-ttu-id="b747a-125">Value</span><span class="sxs-lookup"><span data-stu-id="b747a-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b747a-126">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="b747a-126">TAPI version</span></span><br/> | <span data-ttu-id="b747a-127">Requiere TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="b747a-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="b747a-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b747a-128">Header</span></span><br/>       | <dl> <span data-ttu-id="b747a-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b747a-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b747a-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b747a-130">Library</span></span><br/>      | <dl> <span data-ttu-id="b747a-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b747a-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="b747a-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b747a-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="b747a-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b747a-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b747a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="b747a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b747a-135">**ITQOSApplicationID**</span><span class="sxs-lookup"><span data-stu-id="b747a-135">**ITQOSApplicationID**</span></span>](itqosapplicationid.md)
</dt> </dl>

 

 




