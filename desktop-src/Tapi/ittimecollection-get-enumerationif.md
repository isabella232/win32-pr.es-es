---
description: El \_ método get EnumerationIf devuelve la interfaz de enumeración IEnumTime que enumera ITTime.
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'Método ITTimeCollection:: get_EnumerationIf (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690235"
---
# <a name="ittimecollectionget_enumerationif-method"></a><span data-ttu-id="8411a-103">ITTimeCollection:: get \_ EnumerationIf (método)</span><span class="sxs-lookup"><span data-stu-id="8411a-103">ITTimeCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="8411a-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8411a-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8411a-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="8411a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8411a-106">El método **Get \_ EnumerationIf** devuelve la interfaz de enumeración [**IEnumTime**](ienumtime.md) que enumera [**ITTime**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="8411a-106">The **get\_EnumerationIf** method returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8411a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8411a-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8411a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8411a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8411a-109">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8411a-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8411a-110">Puntero a la interfaz [**IEnumTime**](ienumtime.md) .</span><span class="sxs-lookup"><span data-stu-id="8411a-110">Pointer to the [**IEnumTime**](ienumtime.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8411a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8411a-111">Return value</span></span>

<span data-ttu-id="8411a-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="8411a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8411a-113">Value</span><span class="sxs-lookup"><span data-stu-id="8411a-113">Value</span></span>                                                                                         | <span data-ttu-id="8411a-114">Significado</span><span class="sxs-lookup"><span data-stu-id="8411a-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8411a-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8411a-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8411a-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8411a-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8411a-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="8411a-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8411a-118">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="8411a-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="8411a-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8411a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8411a-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8411a-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8411a-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="8411a-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8411a-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8411a-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8411a-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="8411a-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8411a-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="8411a-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="8411a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8411a-125">Remarks</span></span>

<span data-ttu-id="8411a-126">Este método es intercambiable con [**Get \_ \_ NewEnum**](ittimecollection-get--newenum.md) , salvo que devuelve [**IEnumTime**](ienumtime.md) en lugar de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="8411a-126">This method is interchangeable with [**get\_\_NewEnum**](ittimecollection-get--newenum.md) except that it returns [**IEnumTime**](ienumtime.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="8411a-127">TAPI llama al método **AddRef** en la interfaz [**IEnumTime**](ienumtime.md) devuelta por **ITTimeCollection:: get \_ EnumerationIf**.</span><span class="sxs-lookup"><span data-stu-id="8411a-127">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **ITTimeCollection::get\_EnumerationIf**.</span></span> <span data-ttu-id="8411a-128">La aplicación debe llamar a **Release** en la interfaz [**IEnumTime**](ienumtime.md) para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="8411a-128">The application must call **Release** on the [**IEnumTime**](ienumtime.md) interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="8411a-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8411a-129">Requirements</span></span>



| <span data-ttu-id="8411a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8411a-130">Requirement</span></span> | <span data-ttu-id="8411a-131">Value</span><span class="sxs-lookup"><span data-stu-id="8411a-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8411a-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="8411a-132">TAPI version</span></span><br/> | <span data-ttu-id="8411a-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="8411a-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8411a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8411a-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8411a-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8411a-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8411a-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8411a-136">Library</span></span><br/>      | <dl> <span data-ttu-id="8411a-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8411a-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8411a-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8411a-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="8411a-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8411a-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8411a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="8411a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8411a-141">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="8411a-141">**IEnumTime**</span></span>](ienumtime.md)
</dt> <dt>

[<span data-ttu-id="8411a-142">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="8411a-142">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="8411a-143">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="8411a-143">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




