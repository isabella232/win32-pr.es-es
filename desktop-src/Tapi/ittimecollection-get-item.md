---
description: El \_ método get Item obtiene un elemento de la colección mediante un índice.
ms.assetid: 7401ae21-190d-479c-aebc-51bf8a953b94
title: 'Método ITTimeCollection:: get_Item (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68b9dec40070ff3abddce0e425300f6d805c1cc9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679368"
---
# <a name="ittimecollectionget_item-method"></a><span data-ttu-id="71ce4-103">ITTimeCollection:: get \_ Item (método)</span><span class="sxs-lookup"><span data-stu-id="71ce4-103">ITTimeCollection::get\_Item method</span></span>

<span data-ttu-id="71ce4-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="71ce4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="71ce4-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="71ce4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="71ce4-106">El método **Get \_ Item** obtiene un elemento de la colección mediante un índice.</span><span class="sxs-lookup"><span data-stu-id="71ce4-106">The **get\_Item** method gets an item from the collection using an index.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ce4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71ce4-107">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]  LONG   Index,
  [out] ITTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="71ce4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71ce4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ce4-109">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="71ce4-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71ce4-110">Índice del elemento que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="71ce4-110">Index of the item to get.</span></span>

</dd> <dt>

<span data-ttu-id="71ce4-111">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="71ce4-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71ce4-112">Puntero a la interfaz deseada de [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="71ce4-112">Pointer to [**ITTime**](ittime.md) desired interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ce4-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71ce4-113">Return value</span></span>

<span data-ttu-id="71ce4-114">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="71ce4-114">This method can return one of these values.</span></span>



| <span data-ttu-id="71ce4-115">Value</span><span class="sxs-lookup"><span data-stu-id="71ce4-115">Value</span></span>                                                                                         | <span data-ttu-id="71ce4-116">Significado</span><span class="sxs-lookup"><span data-stu-id="71ce4-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="71ce4-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="71ce4-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="71ce4-118">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="71ce4-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="71ce4-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="71ce4-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="71ce4-120">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="71ce4-120">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="71ce4-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="71ce4-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="71ce4-122">El parámetro de *Índice* no es válido.</span><span class="sxs-lookup"><span data-stu-id="71ce4-122">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="71ce4-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="71ce4-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="71ce4-124">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="71ce4-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="71ce4-125"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="71ce4-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="71ce4-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="71ce4-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="71ce4-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="71ce4-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="71ce4-128">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="71ce4-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="71ce4-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71ce4-129">Remarks</span></span>

<span data-ttu-id="71ce4-130">TAPI llama al método **AddRef** en la interfaz [**ITTime**](ittime.md) devuelta por I **TTimeCollection:: get \_ Item**.</span><span class="sxs-lookup"><span data-stu-id="71ce4-130">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by I **TTimeCollection::get\_Item**.</span></span> <span data-ttu-id="71ce4-131">La aplicación debe llamar a **Release** en la interfaz **ITTime** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="71ce4-131">The application must call **Release** on the **ITTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ce4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71ce4-132">Requirements</span></span>



| <span data-ttu-id="71ce4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="71ce4-133">Requirement</span></span> | <span data-ttu-id="71ce4-134">Value</span><span class="sxs-lookup"><span data-stu-id="71ce4-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71ce4-135">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="71ce4-135">TAPI version</span></span><br/> | <span data-ttu-id="71ce4-136">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="71ce4-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="71ce4-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71ce4-137">Header</span></span><br/>       | <dl> <span data-ttu-id="71ce4-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ce4-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="71ce4-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71ce4-139">Library</span></span><br/>      | <dl> <span data-ttu-id="71ce4-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71ce4-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="71ce4-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71ce4-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="71ce4-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71ce4-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ce4-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="71ce4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ce4-144">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="71ce4-144">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="71ce4-145">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="71ce4-145">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




