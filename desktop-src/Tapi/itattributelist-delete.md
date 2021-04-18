---
description: El método Delete elimina el atributo en el índice especificado.
ms.assetid: 6bc6f3d2-d630-4a00-9d74-fb5fa7626e3f
title: ITAttributeList::D método iminar (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 729dd79b88198f671949aeb79caf06289abd9a75
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681070"
---
# <a name="itattributelistdelete-method"></a><span data-ttu-id="ec73d-103">ITAttributeList::D iminar (método)</span><span class="sxs-lookup"><span data-stu-id="ec73d-103">ITAttributeList::Delete method</span></span>

<span data-ttu-id="ec73d-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ec73d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ec73d-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="ec73d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ec73d-106">El método **Delete** elimina el atributo en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="ec73d-106">The **Delete** method deletes the attribute at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec73d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec73d-107">Syntax</span></span>


```C++
HRESULT Delete(
  [in] LONG Index
);
```



## <a name="parameters"></a><span data-ttu-id="ec73d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ec73d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec73d-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ec73d-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec73d-110">Índice del atributo que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="ec73d-110">Index of the attribute to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec73d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec73d-111">Return value</span></span>

<span data-ttu-id="ec73d-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="ec73d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="ec73d-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ec73d-113">Return code</span></span>                                                                                   | <span data-ttu-id="ec73d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec73d-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ec73d-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="ec73d-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ec73d-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ec73d-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ec73d-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ec73d-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ec73d-118">El parámetro de *Índice* no es válido.</span><span class="sxs-lookup"><span data-stu-id="ec73d-118">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="ec73d-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ec73d-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ec73d-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="ec73d-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ec73d-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="ec73d-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ec73d-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="ec73d-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ec73d-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="ec73d-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ec73d-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="ec73d-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="ec73d-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec73d-125">Requirements</span></span>



| <span data-ttu-id="ec73d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec73d-126">Requirement</span></span> | <span data-ttu-id="ec73d-127">Value</span><span class="sxs-lookup"><span data-stu-id="ec73d-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec73d-128">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="ec73d-128">TAPI version</span></span><br/> | <span data-ttu-id="ec73d-129">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="ec73d-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ec73d-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec73d-130">Header</span></span><br/>       | <dl> <span data-ttu-id="ec73d-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec73d-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec73d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ec73d-132">Library</span></span><br/>      | <dl> <span data-ttu-id="ec73d-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec73d-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ec73d-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ec73d-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="ec73d-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec73d-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec73d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec73d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec73d-137">**ITAttributeList**</span><span class="sxs-lookup"><span data-stu-id="ec73d-137">**ITAttributeList**</span></span>](itattributelist.md)
</dt> </dl>

 

 




