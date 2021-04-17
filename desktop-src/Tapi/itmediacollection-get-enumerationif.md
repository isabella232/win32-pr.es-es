---
description: El \_ método get EnumerationIf obtiene un puntero a una interfaz de enumeración multimedia.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'Método ITMediaCollection:: get_EnumerationIf (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a7e7d85c1f7a433a31360fabc8b5dac71e68ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690625"
---
# <a name="itmediacollectionget_enumerationif-method"></a><span data-ttu-id="60fde-103">ITMediaCollection:: get \_ EnumerationIf (método)</span><span class="sxs-lookup"><span data-stu-id="60fde-103">ITMediaCollection::get\_EnumerationIf method</span></span>

<span data-ttu-id="60fde-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="60fde-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="60fde-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="60fde-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="60fde-106">El método **Get \_ EnumerationIf** obtiene un puntero a una interfaz de enumeración multimedia.</span><span class="sxs-lookup"><span data-stu-id="60fde-106">The **get\_EnumerationIf** method gets a pointer to a media enumeration interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="60fde-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60fde-107">Syntax</span></span>


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="60fde-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60fde-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60fde-109">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="60fde-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60fde-110">Puntero a la interfaz [**IEnumMedia**](ienummedia.md) para el elemento deseado.</span><span class="sxs-lookup"><span data-stu-id="60fde-110">Pointer to the [**IEnumMedia**](ienummedia.md) interface for the desired item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60fde-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60fde-111">Return value</span></span>

<span data-ttu-id="60fde-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="60fde-112">This method can return one of these values.</span></span>



| <span data-ttu-id="60fde-113">Value</span><span class="sxs-lookup"><span data-stu-id="60fde-113">Value</span></span>                                                                                         | <span data-ttu-id="60fde-114">Significado</span><span class="sxs-lookup"><span data-stu-id="60fde-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="60fde-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="60fde-116">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="60fde-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="60fde-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="60fde-118">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="60fde-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="60fde-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="60fde-120">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="60fde-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="60fde-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="60fde-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="60fde-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="60fde-123"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="60fde-124">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="60fde-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="60fde-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60fde-125">Remarks</span></span>

<span data-ttu-id="60fde-126">Este método es intercambiable con [**Get \_ \_ NewEnum**](itmediacollection-get--newenum.md) , salvo que devuelve [**IEnumMedia**](ienummedia.md) en lugar de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="60fde-126">This method is interchangeable with [**get\_\_NewEnum**](itmediacollection-get--newenum.md) except that it returns [**IEnumMedia**](ienummedia.md) instead of **IUnknown**.</span></span>

<span data-ttu-id="60fde-127">TAPI llama al método **AddRef** en la interfaz [**IEnumMedia**](ienummedia.md) devuelta por **ITMediaCollection:: get \_ Enumerationlf**.</span><span class="sxs-lookup"><span data-stu-id="60fde-127">TAPI calls the **AddRef** method on the [**IEnumMedia**](ienummedia.md) interface returned by **ITMediaCollection::get\_Enumerationlf**.</span></span> <span data-ttu-id="60fde-128">La aplicación debe llamar a **Release** en la interfaz **IEnumMedia** para liberar recursos asociados a ella.</span><span class="sxs-lookup"><span data-stu-id="60fde-128">The application must call **Release** on the **IEnumMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="60fde-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60fde-129">Requirements</span></span>



| <span data-ttu-id="60fde-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="60fde-130">Requirement</span></span> | <span data-ttu-id="60fde-131">Value</span><span class="sxs-lookup"><span data-stu-id="60fde-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60fde-132">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="60fde-132">TAPI version</span></span><br/> | <span data-ttu-id="60fde-133">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="60fde-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="60fde-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60fde-134">Header</span></span><br/>       | <dl> <span data-ttu-id="60fde-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="60fde-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60fde-136">Library</span></span><br/>      | <dl> <span data-ttu-id="60fde-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="60fde-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60fde-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="60fde-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60fde-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="60fde-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fde-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="60fde-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> <dt>

[<span data-ttu-id="60fde-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="60fde-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




