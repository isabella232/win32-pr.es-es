---
description: El \_ \_ método get NewEnum devuelve un enumerador para la colección.
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: 'Método ITMediaCollection:: get__NewEnum (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfa5655d70026fe2c481aedad0e76923f4caa646
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690570"
---
# <a name="itmediacollectionget__newenum-method"></a><span data-ttu-id="58d50-103">ITMediaCollection:: get \_ \_ NewEnum (método)</span><span class="sxs-lookup"><span data-stu-id="58d50-103">ITMediaCollection::get\_\_NewEnum method</span></span>

<span data-ttu-id="58d50-104">\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="58d50-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="58d50-105">La API de cliente de RTC proporciona una funcionalidad similar.\]</span><span class="sxs-lookup"><span data-stu-id="58d50-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="58d50-106">El método **Get \_ \_ NewEnum** devuelve un enumerador para la colección.</span><span class="sxs-lookup"><span data-stu-id="58d50-106">The **get\_\_NewEnum** method returns an enumerator for the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d50-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58d50-107">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="58d50-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58d50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58d50-109">*pval* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="58d50-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="58d50-110">Puntero a una interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) en un objeto de enumerador para la colección.</span><span class="sxs-lookup"><span data-stu-id="58d50-110">Pointer to an [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface on an enumerator object for the collection.</span></span>

<span data-ttu-id="58d50-111">Llame al método [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la interfaz **IUnknown** devuelta para obtener un puntero a una interfaz de enumeración [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en la colección.</span><span class="sxs-lookup"><span data-stu-id="58d50-111">Call the [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the returned **IUnknown** interface to obtain a pointer to an [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumeration interface on the collection.</span></span> <span data-ttu-id="58d50-112">**IEnumVARIANT** proporciona varios métodos que puede usar para recorrer en iteración la colección.</span><span class="sxs-lookup"><span data-stu-id="58d50-112">**IEnumVARIANT** provides a number of methods that you can use to iterate through the collection.</span></span>

<span data-ttu-id="58d50-113">Para obtener más información, vea la sección Comentarios que se muestra más adelante.</span><span class="sxs-lookup"><span data-stu-id="58d50-113">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58d50-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58d50-114">Return value</span></span>

<span data-ttu-id="58d50-115">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="58d50-115">This method can return one of these values.</span></span>



| <span data-ttu-id="58d50-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="58d50-116">Return code</span></span>                                                                                   | <span data-ttu-id="58d50-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="58d50-117">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="58d50-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="58d50-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="58d50-119">El método se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="58d50-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="58d50-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="58d50-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="58d50-121">El parámetro *pval* no es un puntero válido.</span><span class="sxs-lookup"><span data-stu-id="58d50-121">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="58d50-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="58d50-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="58d50-123">No hay memoria suficiente para realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="58d50-123">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="58d50-124"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="58d50-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="58d50-125">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="58d50-125">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="58d50-126"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="58d50-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="58d50-127">Este método aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="58d50-127">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="58d50-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58d50-128">Remarks</span></span>

<span data-ttu-id="58d50-129">Este método es intercambiable con [**Get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) , salvo que devuelve **IUnknown** en lugar de [**IEnumMedia**](ienummedia.md).</span><span class="sxs-lookup"><span data-stu-id="58d50-129">This method is interchangeable with [**get\_EnumerationIf**](itmediacollection-get-enumerationif.md) except that it returns **IUnknown** instead of [**IEnumMedia**](ienummedia.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58d50-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58d50-130">Requirements</span></span>



| <span data-ttu-id="58d50-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="58d50-131">Requirement</span></span> | <span data-ttu-id="58d50-132">Value</span><span class="sxs-lookup"><span data-stu-id="58d50-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58d50-133">Versión de TAPI</span><span class="sxs-lookup"><span data-stu-id="58d50-133">TAPI version</span></span><br/> | <span data-ttu-id="58d50-134">Requiere TAPI 3,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="58d50-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="58d50-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58d50-135">Header</span></span><br/>       | <dl> <span data-ttu-id="58d50-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="58d50-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="58d50-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58d50-137">Library</span></span><br/>      | <dl> <span data-ttu-id="58d50-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58d50-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="58d50-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58d50-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="58d50-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58d50-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58d50-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="58d50-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d50-142">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="58d50-142">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

